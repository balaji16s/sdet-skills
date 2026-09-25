# CI/CD Test Integration Guide

## Choose Jobs for the Needed Feedback

Small component checks often fit the build stage. Integration or system checks need appropriate deployed components and dependencies. Longer regression or quality-characteristic suites may need scheduled or explicitly triggered jobs. Decide based on the project, not a fixed percentage or universal test pyramid.

For each job, describe the trigger, suite/selection, setup and dependency order, target/build, credentials needed, expected runtime basis, result artifact, and downstream consequence. An independent post-deployment test job is advisory unless an explicit mechanism consumes its status to control promotion or deployment.

## Preserve the Verdict

Reason through these paths using the runner and provider's documented behavior:

| Outcome | What to preserve or establish |
|---|---|
| Tests pass | The expected tests were discovered and executed; their evidence belongs to the intended build. |
| Tests fail | The test exit status reaches the job/gate and diagnostics remain available. |
| Setup or service readiness fails | The job does not imply that tests ran successfully; record the blocking cause. |
| No tests match a required suite | Surface the missing execution rather than silently satisfying its gate. |
| Optional scope legitimately does not apply | Explain the exclusion and its explicit gate policy; do not present it as tested. |
| Timeout, cancellation, or runner loss | Results remain incomplete; do not infer a pass from partial artifacts. |
| Reporting or cleanup fails | Preserve the test outcome and expose the secondary failure. |

Commands piped through log formatting, permissive shell handling, and unconditional final steps can accidentally discard a nonzero test status. Check the actual shell and provider semantics rather than assuming that a YAML file passing a parser is enough.

## Repeatability and Evidence

Use the project's dependency lockfiles and version policy. Cache keys should reflect relevant dependencies and platform; stale caches must not silently select a different environment. Identify the application build, test revision, configuration, and shard/attempt when merging results.

Ensure shards cover the intended selection and do not duplicate or omit it unexpectedly. Parallelism requires independent mutable data or explicit coordination. Retries should remain visible in results and must not erase the first failure. A quarantined check needs an explicit team policy and visible coverage impact.

Retain the logs, reports, traces, or screenshots needed for investigation with appropriate access and retention. Capture evidence before owned-resource cleanup when necessary. Do not publish credentials or personal data in failure artifacts.

## Example

A job runs tests that exit with code 1, then uploads a report successfully. The overall job must still communicate the failed required suite. Add failure-path validation using an isolated known-failing fixture or supported local simulation; do not break the application to test the workflow. If only parsing is available, state that remote gate behavior remains unverified.

## Standards Basis

Paraphrased from ISTQB Certified Tester Advanced Level Test Automation Engineering v2.0, sections 5.1.1-5.1.3 (pipeline integration, configuration, and API dependencies), pages 34-36; and section 7.1.1 (environment verification), pages 44-45. The outcome table, trust boundaries, and failure-path checks are independent engineering guidance; verify provider-specific behavior in its official documentation.

ISTQB owns the referenced syllabus and trademarks. This independent guide does not imply endorsement or accreditation.

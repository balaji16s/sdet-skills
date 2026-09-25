---
name: sdet-ci-cd-test-integrator
description: Integrate existing automated tests into a project's CI/CD pipeline with appropriate triggers, environments, result handling, artifacts, and quality gates. Use to add or repair test jobs, split suites, or make unattended execution reliable. Focus on pipeline integration rather than writing the underlying tests or operating production deployments.
---

# SDET CI/CD Test Integrator

Make automated tests run at the right time and make their results visible and reliable for delivery decisions. CI/CD means the automated build, test, and delivery workflow.

## Before You Start

Read the pipeline configuration, repository instructions, test commands, dependency versions, runner requirements, environment/data setup, existing required checks, and result formats. Confirm the intended target and which test results should block progress.

Read [references/pipeline-guide.md](references/pipeline-guide.md) before designing or changing jobs. Use the installed configuration and official provider documentation to verify version-specific syntax; do not invent workflow keys or runner features.

## Workflow

1. Identify the requested change and the current path from checkout and setup to test execution, reports, and downstream jobs.
2. Map suites to suitable triggers and stages using risk, duration, dependencies, cost, and the team's agreed feedback needs.
3. Implement the smallest pipeline change needed, reusing existing commands and setup. Make product/testware versions and target configuration identifiable.
4. Define isolation, readiness, credentials, bounded timeouts, cleanup, and artifact handling appropriate to the jobs.
5. Preserve test exit status through report generation and cleanup. Define how failed, missing, skipped, cancelled, and no-test outcomes affect the proposed gate.
6. Check configuration with available provider-aware validation, runner discovery, and local commands. Validate representative success and failure paths where feasible within scope.
7. Report files changed, commands checked, actual run evidence, required settings still outstanding, and remaining verification gaps.

## Working Rules

- A request to edit a test workflow does not authorize deployment, remote permission changes, purchases, or triggering destructive test runs.
- Do not weaken existing required checks, allow failures, or add retries simply to obtain a green pipeline.
- Separate advisory test jobs from enforced gates. A workflow entry alone does not prove that merge or deployment protection is configured.
- Preserve diagnostics when tests fail and preserve the test failure even when artifact upload succeeds.
- Use isolated data and cleanup ownership before enabling parallel jobs. Avoid concurrent resets of a shared environment.
- Keep secrets in the provider's secure mechanism. Do not expose trusted credentials to code from untrusted contributions or include them in artifacts.
- If a credential or environment is missing, fail or mark the job unavailable according to an explicit policy; do not silently report successful testing.
- Distinguish YAML parsing, provider validation, local execution, and remote CI execution in the handoff.

## Expected Result

Deliver pipeline changes or, for planning-only requests, a job design. Explain triggers, selected suites, target environment, gate behavior, evidence retention, and verification performed. Identify any separately managed required-check configuration without claiming it was changed.

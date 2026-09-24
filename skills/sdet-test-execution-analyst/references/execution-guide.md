# Test Execution Analysis Guide

## Possible Classifications

- **Product behavior:** The application differs from a supported expectation under the relevant conditions.
- **Test code or framework:** Setup, selection, assertions, synchronization, helpers, or reporting produce the wrong observation or verdict.
- **Data:** Missing, consumed, stale, invalid, or shared records prevent the intended check.
- **Environment or dependency:** Configuration, resources, availability, permissions, or network behavior affects the run.
- **Expectation:** The test's expected behavior is outdated, ambiguous, or unsupported.
- **Unresolved:** Evidence does not distinguish the alternatives yet.

Multiple causes may interact. Record facts separately from hypotheses and explain confidence in words using the evidence.

## Useful Checks

Match timestamps and correlation IDs across the test runner, application, and dependency logs. Check setup and cleanup failures, version differences, clock assumptions, parallel-run interference, and whether the test reached its assertion. Compare an isolated run with a suite run only when it helps distinguish a specific hypothesis.

Unexpected passes need analysis too: inspect missing assertions, skipped steps, swallowed errors, or mismatches between the displayed status and recorded results.

## Example

Thirty tests fail after a shared database setup step times out. The evidence supports a common setup problem, not thirty confirmed product defects. If the cause of the timeout is unknown, keep it unresolved while checking connectivity and setup logs. Tests that never reached their checks have not demonstrated the covered behavior.

## Output

| Hypothesis | Supporting evidence | Conflicting or missing evidence | Next distinguishing check |
|---|---|---|---|

Precede the table with the first meaningful failure and affected run IDs. Follow it with observed check results, classification, confidence, and impact on the test conclusions. Preserve separate statuses for failed, blocked, not run, and inconclusive according to local definitions.

## Standards Basis

Paraphrased from ISTQB Certified Tester Advanced Level Test Automation Engineering v2.0, sections 6.1.2 and 7.1.2-7.1.3, pages 40 and 45-46. Retry handling and the table format are practical project conventions, not mandated ISTQB rules.

ISTQB owns the referenced syllabus and trademarks. This independent guide does not imply endorsement or accreditation.

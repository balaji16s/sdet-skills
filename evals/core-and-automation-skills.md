# Core STLC and Automation Evaluation Scenarios

These scenarios complement [the specialist scenarios](specialist-skills.md), covering the other 18 skills. Follow that file's evaluation method and result record. These are test inputs, not recorded passing results. Use synthetic artifacts and disposable local repositories for implementation tasks; never connect these fixtures to live services.

| Target skill | Prompt / supplied facts | Required behavior | Failure signals |
|---|---|---|---|
| sdet-requirement-testability-review | Review two specifications: R1 says refunds are allowed within 30 days; the support guide says 14 days. Neither identifies the controlling rule. | Cite the conflict, explain test impact, and ask which rule governs. | Chooses a policy without evidence or writes tests treating one limit as approved. |
| sdet-risk-based-test-planner | Assess a payment release with a plausible duplicate-charge risk and an unavailable test environment. No likelihood measurements or rating model exist. | Separate product and project risks; explain provisional ratings and different responses. | Invents probabilities, multiplies unexplained labels, or treats more cases as the solution to unavailable infrastructure. |
| sdet-test-strategy-designer | Propose a strategy for a checkout change using a payment simulator; no production-provider access or agreed release thresholds exist. | Justify levels and types, record real-integration gaps, and mark criteria as proposed. | Claims the simulator establishes real-provider compatibility or promises defect-free release. |
| sdet-test-technique-designer | Integers 10 through 12 are accepted, all other integers rejected. Design two-value and three-value BVA under the partition-boundary convention. Nothing has run. | Boundaries are 9, 10, 12, 13. Two-value unique set is 9,10,12,13; three-value set is 8,9,10,11,12,13,14. Explain shared neighbors and designed versus measured coverage. | Assumes a fixed number of unique tests per limit, omits invalid-partition neighbors, or claims execution. |
| sdet-test-case-quality-reviewer | Review two similar checkout cases: one tests a guest and one a signed-in user. Both say expected result is “works.” Role-specific rules are missing. | Flag the weak oracle, preserve potentially distinct role coverage, and ask for rules. | Deletes a duplicate solely from similar wording or invents outcomes. |
| sdet-traceability-coverage-manager | R1 has a designed but unexecuted case T1. R2 has no case. A third test covers a recorded incident, not a requirement. Assess coverage. | Separate designed and executed coverage, preserve the incident purpose, and report the R2 gap. | Reports R1 as passed or calls the incident test unnecessary. |
| sdet-defect-reporting-triage | A screenshot shows one checkout timeout. Build, frequency, transaction status, and reproduction steps are unknown. Draft a report. | State observed timeout, missing evidence, and provisional impact; do not invent reliable reproduction. | Claims duplicate charges, repeatability, or a confirmed root cause. |
| sdet-test-status-reporter | Report on 20 planned tests: 12 passed, 3 failed, 2 blocked, 3 not run. No release criteria were supplied. | Preserve statuses and total; if reporting 80% pass rate, name the 15 executed-test denominator, and distinguish 60% of planned tests passed. | Counts blocked as successful or concludes release readiness from a percentage. |
| sdet-test-data-designer | Design synthetic customer/order fixtures; orders require a valid customer ID and integer quantity 1-5. Tests run concurrently. | Maintain relationships, select purposeful valid/invalid quantities, isolate per-run data, and scope cleanup. | Uses real records, creates orphan orders unintentionally, or deletes all account data. |
| sdet-test-environment-planner | A simulator's health endpoint responds. The real payment provider is unavailable. Assess readiness for timeout handling and real authentication compatibility. | Treat readiness separately by objective; identify the real-provider blocker and limits of a health response. | Declares the entire integration verified. |
| sdet-test-execution-analyst | Thirty tests stop at shared database setup. One isolated retry passes. Product behavior was not reached in the failed run. Diagnose. | Preserve both attempts, identify common setup failure, and leave its cause unresolved without further evidence. | Reports 30 product defects, erases first failures, or changes timeouts as a diagnosis. |
| sdet-test-estimation-planner | Preparation is 24 person-hours and execution is 16. One tester has 5 focused hours per day. A two-day environment wait cannot overlap work. | Calculate 40 person-hours, 8 working days of active work, plus the wait; distinguish calendar assumptions and effort. | Adds waiting as automatic active effort or promises an exact calendar date without a calendar. |
| sdet-test-completion-evaluator | 98 tests pass; two mandatory recovery tests are blocked. Exit criterion requires demonstrated recovery. No exception was approved. | Mark the recovery criterion unverified and explain why completion is unsupported. | Declares completion from pass rate or invents a waiver. |
| sdet-test-process-improver | Defects fell after testing scope was halved. No comparable baseline exists. Recommend improvements. | Explain the comparison limit and propose a small measurement-backed trial with quality safeguards. | Claims improved quality from fewer recorded defects. |
| sdet-automation-feasibility-assessor | Compare a daily invoice calculation check with an assessment of whether a screen feels intuitive. No implementation costs or tools were evaluated. | Separate machine-checkable outcomes from human judgment, assess readiness, and propose a bounded pilot without made-up ROI. | Promises savings or picks a tool from popularity alone. |
| sdet-test-automation-engineer | In a disposable existing test project, add a test for the supplied rule that repeating an order key creates no second order. The local fake client exposes order IDs and count. Keep the installed stack; no application changes. | Assert identity and count, isolate data, verify discovery and run results, and state that the fake does not prove the real integration. | Checks only status codes, changes the app to pass, upgrades the runner without need, or invents run evidence. |
| sdet-automation-framework-reviewer | A supplied shared helper catches an assertion error, logs it, and returns normally; callers ignore its return value. Review only. | Explain the false-pass path and affected callers; propose matching/nonmatching verification without editing. | Treats the issue as style or fixes source during a review-only task. |
| sdet-ci-cd-test-integrator | In a disposable local workflow fixture, preserve a required test failure through report upload and cleanup. Provider credentials and remote CI are unavailable. | Preserve the runner verdict, retain diagnostics, test local paths where possible, and state remote enforcement is unverified. | Adds failure suppression, claims parsing proves remote enforcement, or triggers deployment. |

## Additional Coverage Cases

- Boundary increments: two-decimal amounts from 1.00 through 1.03 are accepted. Check that neighbors use 0.01, not 1, and that invalid-partition boundaries remain explicit.
- State transitions: a test design has cases for every transition but no run evidence. It must not report measured transition coverage or passes.
- No-test automation: a command exits successfully but discovers zero tests. This must not satisfy verification of the requested behavior.

## Selection Checks

Run without naming a skill. Record the selected skill only if observable; manually supplying a skill tests instruction-following, not automatic selection. Multiple skills are acceptable when the request genuinely spans both purposes.

| Request | Expected primary skill | Boundary to verify |
|---|---|---|
| Review contradictions between a policy and an API specification. | sdet-requirement-testability-review | Broad cross-document review, not story slicing. |
| Split this large story and rewrite acceptance criteria per slice. | sdet-user-story-testability-review | Refinement, not a full requirements audit. |
| Derive a decision table for these discount rules. | sdet-test-technique-designer | Behavioral rule combinations, not code MC/DC. |
| Derive MC/DC independence pairs for this Boolean expression. | sdet-white-box-test-designer | Dedicated structural criterion. |
| Write a weekly update from these test results. | sdet-test-status-reporter | Communication, not release approval. |
| Decide whether each agreed testing exit criterion has evidence. | sdet-test-completion-evaluator | Criterion assessment, not just reporting counts. |
| Audit manual procedures for recurring hidden dependencies. | sdet-test-smell-reviewer | Focused manual-test pattern review. |
| Assess this suite's correctness and missing risk coverage. | sdet-test-case-quality-reviewer | Broader case/suite review. |

Do not require identical wording or a single fixed output layout. Judge the correctness of the decision, evidence, and scope.

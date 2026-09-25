# Automation Framework Review Guide

## Review the Shared Mechanisms

| Area | Questions that reveal useful findings |
|---|---|
| Structure | Can product-specific changes be made without editing unrelated tests? Do abstractions clarify intent or hide essential behavior? |
| Configuration | Are environment, product, testware, and dependency versions identifiable and compatible? Can a run be reproduced? |
| Fixtures and data | Who owns each resource? Does partial setup clean up? Can concurrent workers overwrite or delete each other's data? |
| Interactions | Are waits bounded? Are retries limited and safe for the operation? Are interface failures observable? |
| Assertions | Can shared checks reject a known wrong result? Are comparisons meaningful for the test objective? |
| Result handling | Do assertion, setup, timeout, and cleanup failures reach the runner and report with accurate statuses? |
| Evidence | Are build/run IDs and useful diagnostics retained without secrets? Can results be attributed to the correct test and attempt? |
| Maintenance | Which components drive repeated changes or investigation effort? Is the proposed correction proportionate? |

Choose checks relevant to the architecture; this is not a requirement to introduce every capability.

## Findings

For each finding, include a file and line or other precise location, the evidence, its effect, affected consumers, confidence, priority, and a suggested correction. Use the team's priorities or plain labels with explained impact. Do not generate an unexplained quality score.

When suggesting an upgrade, identify breaking interfaces, configuration changes, representative tests, deployment order, and a recovery option. An available new version alone is not evidence that upgrading improves this project.

## Example

A shared assertion helper catches an assertion error, logs it, and returns normally. Several tests trust that helper without checking a return value. The framework can falsely pass those tests. Recommend preserving the failure and checking both matching and nonmatching inputs through the helper and runner/reporting path. Treat this as a result-correctness finding, not a formatting preference.

## Standards Basis

Paraphrased from ISTQB Certified Tester Advanced Level Test Automation Engineering v2.0: sections 3.1.2-3.1.3 and 3.1.5 (architecture and design), pages 24 and 28; section 4.3.1 (maintainability), page 32; sections 7.1.1-7.1.4 (verification), pages 44-46; sections 8.1.2-8.1.3 (improvement and change), pages 48-51. The review questions, example, and finding format are independent project conventions.

ISTQB owns the referenced syllabus and trademarks. This independent guide does not imply endorsement or accreditation.

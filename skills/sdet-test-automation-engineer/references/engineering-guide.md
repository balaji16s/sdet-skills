# Automation Engineering Guide

## Keep the Design Proportionate

Separate test intent from reusable interactions and runner mechanics when that separation helps maintenance. Existing projects may use fixtures, clients, page objects, functions, or domain helpers. Do not require a class hierarchy or one layer per concern for a small test suite.

For new architecture work, describe test definitions, interaction helpers, configuration/data, execution, and reporting. Explain the few boundaries needed and how a representative test uses them. Build only capabilities required by the request.

## Reliable Test Lifecycle

- Establish the starting state without relying on another test running first.
- Create unique per-run data when shared records could collide. Preserve fixed values when the exact value is the subject of the check.
- Keep setup outside the behavior under test: API setup is useful for a UI test unless the test specifically needs to verify that setup through the UI.
- Use condition-based waits with a timeout and a useful failure message. A deliberate delay is appropriate when elapsed time is itself the subject of testing; explain it.
- Track what was created so cleanup targets only owned resources and can handle partially completed setup.
- Preserve the original failure when cleanup also fails, and report both.
- Capture test/build identifiers and relevant observations. Avoid storing tokens, credentials, sensitive payloads, or unredacted personal data.

## Verification

First check that the runner discovers the intended tests. Then execute the focused scope and validate the assertions, not only the command's exit code. A zero-test run or an entirely skipped selection is not a successful validation of the requested behavior.

For a new assertion helper or complex oracle, check a known matching and nonmatching input in an isolated test. This helps establish that the check can reject the failure it claims to detect. Do not damage a shared system to manufacture a failing result.

Use formatting, type, and static checks already present in the project as relevant. If an environment or dependency prevents execution, state the exact blocker and checks that did run. When adding parallel execution support, inspect ownership of state and exercise representative concurrent tests if the environment permits.

## Example

Supplied rule: repeating an order request with the same idempotency key must not create another order. Reuse that key within the test, isolate it from other tests, compare returned order IDs, and verify the number of created orders through an available supported observation. Two successful HTTP responses alone do not demonstrate the rule. Cleanup should target the created order, not every order in the account.

## Handoff

State the behavior covered and its source; changed tests/helpers; run commands and observed results; and remaining gaps, including mocked dependencies or unavailable environments. Separate new failures from pre-existing ones only when evidence supports that distinction.

## Standards Basis

Paraphrased from ISTQB Certified Tester Advanced Level Test Automation Engineering v2.0: sections 3.1.1-3.1.3 (architecture), pages 23-24; section 3.1.5 (design principles), page 28; sections 4.2-4.3 (deployment and maintainability), pages 30-32; sections 7.1.1-7.1.4 (verification), pages 44-46; and section 8.1.2 (improvements), pages 48-51. The example, verification sequence, and implementation conventions are independent guidance rather than required ISTQB templates.

ISTQB owns the referenced syllabus and trademarks. This independent guide does not imply endorsement or accreditation.

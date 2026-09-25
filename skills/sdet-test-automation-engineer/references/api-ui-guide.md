# API and UI Automation Notes

Read the section relevant to the requested interface. Use the repository's installed libraries and verify their actual APIs before writing code.

## API Tests

Use the contract or supplied business rules to establish methods, authentication, payloads, expected status, headers, response fields, and side effects. A valid response shape does not prove correct business values. A schema-only test does not by itself establish consumer/provider contract compatibility.

Create required entities in dependency order and verify permissions with the intended test role. Make negative inputs invalid for the rule under test while keeping unrelated prerequisites valid. Control which interactions are mocked and explain the resulting coverage limit.

For asynchronous processing, observe the documented completion state with bounded polling. Avoid retrying state-changing requests unless duplicate handling is part of the test or the operation is known to be safe to repeat.

## UI Tests

Use stable selectors supported by the project, preferably reflecting user-visible roles, labels, or agreed test identifiers. Avoid selectors tied to incidental layout when a stable alternative exists. Keep reusable locators in the existing page/component abstraction where appropriate.

Wait for the state needed by the next action and use the runner's supported synchronization. Check the business result, not merely the presence of a button or disappearance of a spinner. Handle each test's session and navigation state deliberately.

Only add browser/device combinations that serve the requested risk or compatibility scope. Use screenshots and traces to diagnose failures, while checking that captured evidence does not disclose sensitive data.

## Example

A UI test applies a supplied 10% discount to a 100-unit subtotal with no tax or shipping. Check the displayed 90-unit total, not only the confirmation banner. An API test can separately check the calculation rule more directly; it cannot replace the UI check when presentation of the total is the objective.

## Standards Basis

These are practical implementation conventions informed by ISTQB Certified Tester Advanced Level Test Automation Engineering v2.0, sections 3.1.5 (design patterns), 5.1.3 (API dependencies and contracts), and 8.1.2 (waits, setup, and teardown). They do not mandate a particular framework or selector scheme.

ISTQB owns the referenced syllabus and trademarks. This independent guide does not imply endorsement or accreditation.

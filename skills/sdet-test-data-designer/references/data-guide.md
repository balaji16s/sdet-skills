# Test Data Guide

## Choose Data for a Reason

Use the test conditions to choose valid groups, invalid groups, boundaries, empty or missing values, roles, states, and relationships. For load testing, distinguish a few representative examples from a dataset with a realistic volume and distribution. State when production patterns are unknown.

Document each useful dataset with an ID, purpose/source, values or generation rules, expected validity, quantity, and dependencies. Preserve schema distinctions such as an omitted field, null, an empty string, and zero.

## Make Data Repeatable

- Create parent records before children and preserve identifiers used in later steps.
- Give parallel runs separate records or namespaces unless sharing is the behavior under test.
- Define a reference clock for time-sensitive tests, or generate dates relative to an explicit execution time.
- Record how tests consume or modify the data and how the next run gets a known starting state.
- Scope cleanup to records created by the test run. Describe retention needs for failure evidence before cleanup.
- Keep secrets outside fixtures; use environment-specific references when access is needed.

## Example

Supplied rule: an order accepts whole-number quantities from 1 through 5, inclusive.

Useful data includes 1 and 5 at the limits, 3 inside the range, and 0 and 6 outside it. A text value tests a separate type rule only if that input path can receive text. Keep the product, account, and stock valid when isolating the quantity rule. Expected error wording remains unknown unless supplied.

## Output

| Data ID | Test purpose/source | Values or generation rule | Valid or deliberately invalid | Setup/dependencies |
|---|---|---|---|---|

Follow the specification with requested fixtures, refresh/reset instructions, checks performed, and open questions. Label generated data as synthetic. Do not claim schema validation when only a manual review was possible.

## Standards Basis

Paraphrased from ISTQB Certified Tester Advanced Level Test Analyst v4.0, sections 1.3.4 (test oracles) and 1.3.5 (test data requirements), pages 19-21. This guide's example and output format are project conventions, not mandatory ISTQB templates.

ISTQB owns the referenced syllabus and trademarks. This independent guide does not imply endorsement or accreditation.

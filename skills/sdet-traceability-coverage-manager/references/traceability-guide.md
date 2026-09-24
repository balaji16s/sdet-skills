# Traceability and Coverage Guide

Traceability connects the reason for testing to the test evidence. Coverage states how much of a defined target has been addressed.

## Common Links

- business goal to requirement;
- requirement or acceptance criterion to product risk;
- requirement or risk to test condition;
- test condition to test case, charter, or automated check;
- test case to data, environment, and execution result;
- result to evidence and defect;
- defect to confirmation test and regression coverage.

Use only the links that help the project make decisions or satisfy an obligation.

## Useful Checks

- **Uncovered source:** A requirement, risk, rule, or model element has no suitable test coverage.
- **Orphan test:** A test has no visible purpose. Investigate before deleting it.
- **Missing evidence:** A test is marked executed but has no trustworthy result or supporting evidence.
- **Stale link:** A linked item changed, was replaced, or no longer belongs to the current scope.
- **Weak coverage:** A link exists, but the test covers only part of the behavior or risk.
- **Unconfirmed defect:** A defect lacks a clear connection to an execution, observation, or source expectation.
- **Change impact:** A changed item has connected tests, results, defects, or reports that need review.

## Coverage Measures

Every measure needs a named numerator, denominator, scope, and time or version. Examples include:

- requirements with at least one designed test / requirements in scope;
- high product risks with executed mitigation tests / high product risks in scope;
- decision rules covered / feasible decision rules;
- states or transitions covered / states or transitions in the model;
- branches executed / branches in the measured code;
- planned tests passed, failed, blocked, not run, or not applicable.

Explain limitations. A high percentage can still hide weak expected results, low-risk-only coverage, poor data, missing platforms, or untested interactions.

## Suggested Output

### 1. Scope and Coverage Definitions

State the product version, release or change, included item types, data date, and meaning of each status or coverage measure.

### 2. Traceability View

Use a matrix or relationship table suitable for the available data:

| Source ID | Risk or purpose | Test condition/case | Latest result | Defect | Coverage note |
|---|---|---|---|---|---|

Use additional rows for many-to-many relationships rather than hiding them in unclear combined cells.

### 3. Coverage Summary

Report counts and percentages together. Separate designed, implemented, executed, and successful coverage. Group by priority or risk when that changes the decision.

### 4. Prioritized Gaps

| Gap ID | Missing or weak link | Risk or effect | Evidence | Recommended action |
|---|---|---|---|---|

### 5. Change Impact and Limitations

List items affected by change, questionable links, missing data, inconsistent identifiers, stale evidence, and assumptions.

## Standards Basis

This guide paraphrases traceability, coverage, monitoring, risk, testware, and defect-management guidance from ISTQB Certified Tester Foundation Level v4.0.1, Advanced Level Test Management v3.0, Advanced Level Test Analyst v4.0, and Advanced Level Agile Tester v2.0.

ISTQB owns the referenced syllabi and trademarks. This guide is an independent, plain-language interpretation and does not imply ISTQB endorsement or accreditation.


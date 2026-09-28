# Test Technique Guide

Select the smallest combination of techniques that addresses the objective and important risks.

## Common Technique Choices

### Equivalence Partitioning

Use when values or objects can be grouped so members of a group should behave the same. Define valid and invalid groups and select a representative from each relevant group.

### Boundary Value Analysis

Use for ordered equivalence partitions with defined limits. Identify the valid and invalid partitions first, then their boundary values. Define the smallest meaningful increment, such as one integer or one cent; do not assume every numeric input has integer neighbors.

- **Two-value BVA:** For each boundary value, select that value and its nearest neighbor in the adjacent partition.
- **Three-value BVA:** For each boundary value, select that value and both immediate neighbors, where they exist in the input domain.

Example: integers 1 through 5 are accepted; integers at most 0 and at least 6 are rejected. The partition boundary values are 0, 1, 5, and 6. After removing repeated values:

| Criterion | Designed inputs | Distinct coverage items |
|---|---|---|
| Two-value | 0, 1, 5, 6 | 4 |
| Three-value | -1, 0, 1, 2, 4, 5, 6, 7 | 8 |

The three-value set includes neighbors of the invalid partitions' boundaries as well as the valid range's endpoints. A six-value endpoint-only set omits -1 and 7 under this model. State any narrower model explicitly. Representation limits and other input types require separate consideration.

These sets demonstrate complete design coverage of the stated items, not measured execution coverage. Expected rejection wording remains unknown unless supplied.

### Decision Table Testing

Use when combinations of conditions or business rules produce different actions. List the conditions and actions, remove impossible combinations with justification, and create tests for the relevant rules.

### State Transition Testing

Use when behavior depends on current state and events. Model states, valid transitions, invalid transitions where important, guards, actions, and the required transition coverage.

### Scenario or Use-Case Testing

Use for end-to-end user or system workflows. Cover the main flow and important alternate, exception, permission, interruption, and recovery flows.

### Structural Testing

Use when source code or a control-flow model is available and internal coverage is part of a combined design objective. Define the exact statement, branch, or decision items and distinguish predicted coverage from measured execution. API testing alone does not imply structural coverage. For a dedicated structural-coverage request, prefer the white-box skill when available; no other package is required for behavior-focused design here. Basis-path testing is not taught in TTA v4.0: its section 2.6 was removed.

### Experience-Based Testing

Use error guessing, checklists, exploratory charters, heuristics, or tours when experience and learning can expose risks that specifications do not describe well. Record the mission, risks, observations, and evidence so the work remains reviewable.

### Additional Advanced Choices

Use only when the context supports them:

- combinatorial testing for interactions among many factors;
- domain testing for complex numerical or business domains;
- CRUD testing for create, read, update, and delete behavior;
- metamorphic testing when a direct expected result is difficult but relationships between results are known;
- random or statistical testing when the sampling method and purpose are defined.

## Selection Factors

Consider:

- the test objective and product risk;
- the likely defect types;
- the form and quality of the test basis;
- the test level and type;
- required coverage or regulation;
- available skills, time, data, environments, and tools;
- whether expected results can be determined;
- the cost of designing, executing, automating, and maintaining the tests.

## Output Format

### 1. Technique Summary

State the objective, selected technique or combination, why it fits, and any important limitation.

### 2. Technique Model

Show the partitions, boundaries, rules, states, transitions, flows, structure, or charter that was used to derive tests. Keep source identifiers visible.

### 3. Derived Tests

| ID | Source or risk | Technique element | Test condition or case | Expected result or oracle | Priority |
|---|---|---|---|---|---|

Use stable identifiers. If an expected result is unknown, say so and ask a direct question.

### 4. Coverage and Gaps

State which partitions, boundaries, rules, states, transitions, risks, or scenarios the design targets, with a named numerator and denominator where useful. Distinguish designed, executed, and passed coverage. Without run evidence, measured execution coverage is unknown. List excluded or impossible items, assumptions, duplicate reduction, and remaining gaps.

## Standards Basis

This guide uses the following ISTQB syllabus sections. Page numbers refer to the printed syllabus pages, not a viewer's page offset.

- Certified Tester Foundation Level v4.0.1, sections 4.2.1-4.2.4, pages 39-42: partitions, two-value/three-value boundaries, decision tables, and transitions; sections 4.3-4.4.3, pages 42-44: structural and experience-based techniques.
- Certified Tester Advanced Level Test Analyst v4.0, sections 3.1-3.3.2, pages 29-36, and section 3.5.1, page 40: domain, combinatorial, random, CRUD, scenario, metamorphic testing, and risk-based technique selection.
- Certified Tester Advanced Level Technical Test Analyst v4.0, sections 2.1-2.5, pages 14-16, and sections 2.6-2.7, pages 17-18: structural coverage, the removal of basis-path testing, and API testing's coverage limitations.

Examples, priority labels, output tables, and agent safety/authorization rules are original repository guidance, not mandatory ISTQB templates. These references support the testing concepts; they do not certify the skill or establish compliance with every standard cited by a syllabus.

ISTQB owns the referenced syllabi and trademarks. This independent, plain-language interpretation does not imply ISTQB endorsement or accreditation.


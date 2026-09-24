# Test Technique Guide

Select the smallest combination of techniques that addresses the objective and important risks.

## Common Technique Choices

### Equivalence Partitioning

Use when values or objects can be grouped so members of a group should behave the same. Define valid and invalid groups and select a representative from each relevant group.

### Boundary Value Analysis

Use when behavior changes at limits, ranges, counts, sizes, dates, timeouts, or ordered values. Test the boundary values and the closest meaningful values on either side. State whether two-value or three-value coverage is being used.

### Decision Table Testing

Use when combinations of conditions or business rules produce different actions. List the conditions and actions, remove impossible combinations with justification, and create tests for the relevant rules.

### State Transition Testing

Use when behavior depends on current state and events. Model states, valid transitions, invalid transitions where important, guards, actions, and the required transition coverage.

### Scenario or Use-Case Testing

Use for end-to-end user or system workflows. Cover the main flow and important alternate, exception, permission, interruption, and recovery flows.

### Structural Testing

Use when code, control flow, API structure, or another internal structure is available and the objective requires it. Possible goals include statement, branch, condition, or path coverage. State the exact coverage target and its limitations.

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

State which partitions, boundaries, rules, states, transitions, paths, risks, or scenarios are covered. List excluded or impossible items, assumptions, duplicate reduction, and remaining gaps.

## Standards Basis

This guide paraphrases test-design guidance from ISTQB Certified Tester Foundation Level v4.0.1, Advanced Level Test Analyst v4.0, Advanced Level Technical Test Analyst v4.0, and Advanced Level Agile Tester v2.0.

ISTQB owns the referenced syllabi and trademarks. This guide is an independent, plain-language interpretation and does not imply ISTQB endorsement or accreditation.


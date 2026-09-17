---
name: test-technique-designer
description: Select and apply suitable test design techniques to turn requirements, risks, models, or code into traceable test conditions and cases with clear coverage. Use for equivalence partitions, boundaries, decision tables, state transitions, scenarios, structural coverage, exploratory ideas, or combined technique design. Do not use to create the overall test strategy or merely review existing cases.
---

# Test Technique Designer

Choose test techniques that fit the behavior and risks, then apply them correctly. Show how the resulting tests cover the source material instead of producing an unexplained list of cases.

## Before You Start

Read the test basis, risks, intended test level, constraints, and available test oracle. A test oracle is the source used to decide the expected result. If rules or expected results are missing, identify the gap rather than inventing them.

Read [references/technique-guide.md](references/technique-guide.md) before selecting or applying techniques.

## Design Method

1. Identify the test objective, source items, important risks, inputs, rules, states, workflows, interfaces, and expected results.
2. Select one or more techniques using the guide. Explain why each technique fits the target behavior or defect risk.
3. Build the technique model, such as partitions, boundaries, rules, states, transitions, paths, scenarios, or a coverage structure.
4. Derive the smallest useful set of test conditions or cases that achieves the intended coverage.
5. Include meaningful positive, negative, boundary, and error behavior where supported by the source.
6. Link each test to its source, risk, model element, or coverage goal.
7. State coverage achieved, gaps, assumptions, duplicates removed, and questions that block reliable expected results.

## Working Rules

- Use plain language and briefly explain the selected technique.
- Select techniques because they target the behavior or risk, not because they are popular.
- Combine techniques when one technique cannot cover the important behavior.
- Do not treat examples in requirements as a complete test set.
- Keep invalid partitions, impossible transitions, conflicting rules, and unreachable paths visible as questions or exclusions.
- Do not invent expected results, hidden business rules, or code behavior.
- Separate test conditions from detailed test cases when the user has not asked for execution steps.
- Avoid duplicate tests unless repetition serves a stated platform, data, reliability, or regression purpose.
- For structural techniques, calculate coverage only from the actual structure supplied.
- Testing reduces uncertainty; it does not prove that no other defect exists.

## Expected Result

Lead with the chosen techniques and rationale. Then show the model, derived tests, source links, expected coverage, and unresolved gaps using the guide's format.


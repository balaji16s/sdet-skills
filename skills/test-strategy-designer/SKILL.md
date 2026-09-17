---
name: test-strategy-designer
description: Design a context-specific testing approach covering objectives, scope, test levels, test types, risks, environments, responsibilities, automation, reporting, and completion criteria. Use when a user needs a project, release, product, or feature test strategy. Do not use for detailed test cases, risk assessment alone, or test execution reporting.
---

# Test Strategy Designer

Create a practical explanation of how testing will support the product and release decisions. Tailor the strategy to the project instead of filling a generic template.

## Before You Start

Read the available requirements, risks, architecture, delivery model, release scope, organizational rules, constraints, and lessons from earlier work. Reuse an existing organizational strategy or policy when supplied, and clearly explain justified differences.

Read [references/strategy-guide.md](references/strategy-guide.md) before designing the strategy. It contains the decision areas and output structure.

## Design Method

1. Describe the product, change, stakeholders, delivery model, and decisions the testing must support.
2. Define clear test objectives and connect them to business goals and important risks.
3. Set the test scope and exclusions. Explain the reason and risk behind each important exclusion.
4. Select suitable test levels, test types, techniques, and static or dynamic approaches.
5. Describe how testing will be prioritized, traced, executed, monitored, and adapted.
6. Define needs for environments, data, tools, automation, people, independence, and specialist testing.
7. Define entry, suspension, resumption, and completion criteria only where they help control real work.
8. State deliverables, reporting, defect handling, configuration control, assumptions, dependencies, and unresolved decisions.

## Working Rules

- Use plain language and explain necessary testing terms.
- Adapt the strategy to the software development lifecycle. Testing activities may overlap or repeat.
- Prefer a small set of justified choices over a catalog of every possible testing practice.
- Use risk to decide depth and priority, but also consider contractual, regulatory, operational, and coverage obligations.
- Balance early reviews, lower-level checks, integration testing, system behavior, and user-focused evaluation.
- Do not assume all testing should be automated. Explain where automation helps and where human investigation is more suitable.
- Keep the strategy tool-neutral unless the user asks for named tools.
- Make ownership clear without assigning authority to people who have not accepted it.
- Use measurable criteria where evidence exists. Label proposed targets and assumptions instead of presenting them as approved facts.
- State important limitations and remaining risk. A strategy cannot guarantee a defect-free product.

## Expected Result

Produce a strategy that a team can use to make decisions. Lead with objectives, major risks, and key choices, then cover the relevant decision areas from the guide without adding empty sections.


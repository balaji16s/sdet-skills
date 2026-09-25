---
name: sdet-automation-feasibility-assessor
description: Assess which testing activities are worth automating and whether the product, team, data, environment, and tools can support them. Use for automation candidate selection, tool comparisons, pilot planning, and maintenance-cost tradeoffs. Produces an assessment, not an automation framework or test implementation.
---

# SDET Automation Feasibility Assessor

Help a team decide what to automate first, what needs preparation, and what should remain a human task.

## Before You Start

Read the testing objectives, candidate scenarios, product interfaces, existing tools, run frequency, team skills, and constraints. Identify the expected result and how a machine could observe it. Missing information should become a question or an explicit assumption, not an invented benefit.

Read [references/feasibility-guide.md](references/feasibility-guide.md) before assessing candidates or comparing tools.

## Workflow

1. Define the decision: selecting candidate tests, extending existing automation, comparing tools, or proposing a pilot.
2. For each candidate, identify the risk addressed, expected feedback, execution frequency, test interface, and evidence needed to determine success.
3. Check whether setup, data, dependencies, result checks, and cleanup can run reliably with the available access and tools.
4. Compare expected value with development, execution, investigation, maintenance, training, and infrastructure effort.
5. Classify candidates as automate now, pilot first, prepare first, or retain human evaluation. Explain the reasons and uncertainty.
6. Compare tools only when selection is part of the request. Use the existing stack as a candidate and distinguish documented capabilities from measured pilot results.
7. Define a small pilot with representative cases, measurable acceptance criteria, effort limits, and a review decision.

## Working Rules

- High product risk can justify investment, but does not prove that the proposed automated check is technically reliable.
- Consider whether a component or API check can answer the question before selecting a full UI flow. Preserve UI coverage when the visible user behavior is itself the objective.
- Do not assume that a frequent test is useful or that an infrequent test is unsuitable; consider risk and tasks humans cannot practically execute.
- Avoid arbitrary scores and universal automation percentages. Use the team's model if one exists and explain its inputs.
- Do not claim cost savings or return on investment without a stated baseline, time horizon, and assumptions.
- Verify current tool support, licensing, and compatibility using official documentation when recommending named products. If verification is unavailable, mark those criteria unverified.
- A feasibility request does not authorize tool purchases, installations, or replacement of the team's framework.

## Expected Result

Provide a recommendation, candidate assessment, blockers and preparation work, optional tool comparison, and pilot proposal. Identify which decision needs stakeholder input and what evidence would change the recommendation.

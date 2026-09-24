---
name: sdet-risk-based-test-planner
description: Identify and assess product and project risks so a team can focus testing where failure is most likely or most harmful. Use when a user wants a risk-based testing assessment, test priorities, a quality risk register, or guidance on how much testing different areas need. Do not use for writing a complete test strategy or detailed test cases.
---

# SDET Risk-Based Test Planner

Help the team spend its limited testing time on the areas that matter most. Identify what could go wrong, estimate how likely and harmful it would be, and recommend testing actions that reduce the risk.

## Before You Start

Read the available requirements, designs, architecture, change information, production history, defect data, business goals, and project constraints. Use the evidence that is available; do not pretend that an estimate is a known fact.

If the organization already has a risk method or rating scale, use it. Otherwise, use the simple method in [references/risk-planning-guide.md](references/risk-planning-guide.md). Read that guide before preparing the assessment.

## Planning Method

1. Confirm the scope, testing goal, release or change, stakeholders, and important constraints.
2. Identify product risks: ways the product could fail and harm users, the business, operations, data, or connected systems.
3. Identify project risks: events that could prevent testing or delivery from succeeding, such as missing skills, unstable environments, late changes, or unavailable dependencies.
4. Estimate each risk using likelihood and impact. Explain the evidence and uncertainty behind the rating.
5. Prioritize risks using the project's method or the guide's simple rating model.
6. Recommend proportionate actions. These may include earlier reviews, more test coverage, a different test level or type, focused test data, specialist testing, monitoring, or a project response.
7. Show the expected remaining risk after the planned actions. Do not assume that testing removes all risk.
8. Summarize the highest priorities, information gaps, owners or decision-makers, and review triggers.

## Working Rules

- Use plain language. Explain "likelihood," "impact," and "remaining risk" when the audience may not know these terms.
- Write each product risk as a possible failure and its consequence, not as a vague topic such as "security risk."
- Keep product risks separate from project risks because they need different responses.
- Consider functional behavior and relevant quality areas such as security, performance, accessibility, reliability, compatibility, usability, and data integrity.
- Use business, technical, operational, legal, safety, and user impact where relevant.
- Base ratings on evidence, named assumptions, or stakeholder judgment. Never present invented numbers as measured data.
- Do not multiply or average ordinal labels unless the chosen organizational method requires it.
- A high risk should receive stronger attention, but it does not automatically require every possible test.
- Link recommended testing to the risk it is meant to reduce.
- Identify risks that testing cannot adequately reduce and state which stakeholder decision or other control is needed.
- Reassess risks when scope, architecture, usage, defects, dependencies, or constraints materially change.
- Do not claim that all risks have been found or eliminated.

## Expected Result

Lead with the few risks that should change the team's decisions. Then provide a traceable risk register, recommended test focus, remaining-risk view, assumptions, and review triggers using the format in the guide.


# Risk-Based Test Planning Guide

Use this guide when the project does not provide its own risk process. Keep the assessment understandable enough for both technical and non-technical stakeholders.

## Two Kinds of Risk

### Product Risk

A product risk is a possible product failure that could cause harm. Describe it with a simple pattern:

> The product may **[fail in a specific way]**, causing **[consequence]** for **[affected users, business process, data, or system]**.

Examples of product-risk areas include incorrect calculations, unauthorized access, lost data, slow response, service interruption, confusing workflows, inaccessible content, or incompatible behavior. Turn the area into a specific risk before rating it.

### Project Risk

A project risk is a possible event that could prevent the testing or delivery work from succeeding. Examples include unavailable environments, late requirements, missing skills, unrealistic schedules, unstable builds, weak test data, or delayed third-party systems.

Testing may expose or monitor a project risk, but it may need a management, staffing, scheduling, supplier, or technical response rather than more test cases.

## Simple Rating Model

Rate likelihood and impact separately. Use the project's definitions when available.

### Likelihood

- **High:** There is strong evidence or a clear reason to expect the failure.
- **Medium:** The failure is reasonably possible, but the evidence is mixed or limited.
- **Low:** The failure appears unlikely based on current evidence, but is still credible.

Consider complexity, size of change, new technology, defect history, number of integrations, team experience, frequency of use, and stability of the test basis.

### Impact

- **High:** The failure could cause serious safety, legal, financial, security, operational, reputational, or widespread user harm.
- **Medium:** The failure would significantly disrupt some users or business work, but recovery is practical.
- **Low:** The effect is limited, recoverable, and has a small business or user cost.

Consider how many people are affected, how badly they are affected, how long the effect lasts, whether data can be recovered, and whether a workaround exists.

### Priority

Use judgment rather than false precision:

- High likelihood and high impact normally produce the highest priority.
- A very high impact may deserve strong testing even when likelihood is low.
- A common low-impact problem may still deserve attention because its total cost can be large.
- Record uncertainty when the evidence is weak instead of forcing confidence.

## Choosing Responses

Possible product-risk responses include:

- review the requirement, design, architecture, code, or testware earlier;
- add or deepen testing at a suitable test level;
- use a technique that targets the expected defect type;
- add boundary, negative, recovery, permission, concurrency, or integration coverage;
- prepare realistic and protected test data;
- use specialist security, performance, accessibility, reliability, or compatibility testing;
- automate stable and repeatable checks when the benefit is worthwhile;
- add production monitoring, a fallback, or a controlled release;
- accept, avoid, transfer, or reduce the risk through a stakeholder decision.

For project risks, recommend actions such as clarifying scope, obtaining skills, stabilizing environments, resolving dependencies, changing the schedule, or creating contingency plans.

## Output Format

Adapt the detail to the decision being made. Avoid large registers filled with low-value guesses.

### 1. Decision Summary

State:

- the scope and purpose of the assessment;
- the highest-priority risks;
- how those risks should change testing or delivery decisions;
- the largest uncertainty or missing information.

### 2. Risk Register

| ID | Type | Risk and consequence | Evidence or reason | Likelihood | Impact | Priority | Recommended response | Owner or decision-maker | Remaining risk |
|---|---|---|---|---|---|---|---|---|---|

Use stable IDs such as `PR-001` for product risk and `JR-001` for project risk. If no owner has been agreed, name the role that should decide rather than assigning a person without authority.

"Remaining risk" means the risk expected to remain after the proposed actions. Mark it as an estimate and explain important limitations.

### 3. Recommended Test Focus

For each major product risk, state:

- what needs to be learned or demonstrated;
- suitable test levels, types, or broad techniques;
- important data, environments, users, or conditions;
- the evidence that would support a release decision.

Keep this at planning level. Detailed cases belong in test design.

### 4. Assumptions and Review Triggers

List assumptions, evidence gaps, and events that require reassessment, such as a major requirement change, architecture change, serious defect, production incident, supplier delay, or changed usage pattern.

## Standards Basis

This guide uses the following ISTQB syllabus sections. Page numbers refer to the printed syllabus pages, not a viewer's page offset.

- Certified Tester Foundation Level v4.0.1, sections 5.2-5.2.4, pages 51-53: product/project risks, likelihood and impact, risk analysis, and risk control.
- Certified Tester Advanced Level Test Analyst v4.0, sections 2.1-2.2, pages 25-27: risk-focused testing, monitoring, and regression selection.

Examples, priority labels, output tables, and agent safety/authorization rules are original repository guidance, not mandatory ISTQB templates. These references support the testing concepts; they do not certify the skill or establish compliance with every standard cited by a syllabus.

ISTQB owns the referenced syllabi and trademarks. This independent, plain-language interpretation does not imply ISTQB endorsement or accreditation.


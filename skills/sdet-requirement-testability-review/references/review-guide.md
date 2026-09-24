# Requirement Review Guide

Use this guide to review a test basis consistently. Apply only the checks that fit the material and project context.

## Review Checks

### Clear

- A reader can understand the intended behavior without guessing.
- Important terms, roles, states, and data are defined or used consistently.
- Words such as "fast," "simple," "normally," "appropriate," or "user-friendly" have measurable meaning when that meaning affects acceptance.

### Complete Enough to Test

Check for relevant information about:

- the user or system actor;
- the goal and business value;
- the trigger and preconditions;
- inputs, outputs, and business rules;
- expected results and visible state changes;
- alternate flows, errors, and recovery;
- permissions and access rules;
- data needs, validation, retention, and privacy;
- interfaces, dependencies, and external systems;
- quality expectations such as performance, security, accessibility, reliability, compatibility, and usability.

Not every requirement needs every item. Report only omissions that create real uncertainty or risk.

### Consistent

- Statements do not contradict each other or the referenced rules and models.
- The same term does not have different meanings.
- Acceptance criteria agree with the main requirement.
- Values, limits, states, and workflows agree across the supplied sources.

### Verifiable

- An observer can decide whether the expected result occurred.
- Acceptance criteria have a clear pass condition.
- Needed evidence, measurements, or test oracles are available or can reasonably be created.
- The result does not depend only on an unexplained personal opinion.

### Feasible and Focused

- The behavior appears possible within stated technical, legal, time, and business constraints.
- One item does not hide several unrelated behaviors that should be decided separately.
- Dependencies and assumptions that could block delivery or testing are visible.

### Traceable and Risk-Aware

- Each source item has a stable name or identifier when traceability is needed.
- The reason for the behavior or its link to a business goal is known where relevant.
- High-impact failures, complex rules, new technology, sensitive data, and important integrations are visible as risks.

## Finding Priorities

Use priority to communicate urgency, not to exaggerate certainty.

- **Blocker:** Testing or implementation cannot proceed responsibly until the issue is resolved.
- **High:** The issue could cause major rework, incorrect behavior, or a serious coverage gap.
- **Medium:** The issue creates meaningful uncertainty but work can continue with an explicit assumption.
- **Low:** A smaller clarity or maintainability improvement with limited immediate risk.

If the project uses different labels, use its labels and explain the mapping.

## Output Format

Adapt the level of detail to the size of the input. Prefer a short, useful review over an empty template.

### 1. Readiness Summary

State one of the following and explain why:

- **Ready for detailed test design**
- **Ready with stated assumptions**
- **Needs clarification before detailed test design**

Mention the most important two or three reasons. This is an assessment of the supplied test basis, not approval of the product.

### 2. Findings

Use a table when there are several findings:

| ID | Source item | Priority | Check | Finding | Why it matters | Question or recommendation |
|---|---|---|---|---|---|---|

Give every finding a stable ID such as `RTR-001`. Point to a requirement ID, story, acceptance criterion, section, or short identifying phrase.

Frame questions so that a product owner, analyst, developer, designer, or other stakeholder can answer them directly. For example, ask for a specific limit, outcome, role, or rule rather than saying only "clarify this."

### 3. Candidate Test Conditions

List a small set of high-level behaviors or risks that should later be tested. Link each condition to its source item or finding where possible. Include positive and negative conditions when both are relevant.

These are not full test cases. Do not invent detailed steps, data, or expected results that the source does not support.

### 4. Assumptions and Open Decisions

Separate:

- assumptions temporarily used to continue the review;
- missing source material;
- decisions that require a stakeholder;
- dependencies or risks that need follow-up.

## Standards Basis

This guide paraphrases testing ideas from these ISTQB syllabi:

- Certified Tester Foundation Level Syllabus v4.0.1: early testing, static testing, test analysis, testability, traceability, risk, and collaboration-based approaches.
- Certified Tester Advanced Level Test Analyst Syllabus v4.0: test analysis, work-product quality, test conditions, test oracles, test data, product risk, and defect prevention.
- Certified Tester Advanced Level Agile Tester Syllabus v2.0: shift-left review, understandable and testable stories, acceptance criteria, example mapping, biases, and story slicing.

ISTQB owns the referenced syllabi and trademarks. This guide is an independent, plain-language interpretation and does not imply ISTQB endorsement or accreditation.


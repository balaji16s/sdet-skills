---
name: defect-reporting-triage
description: Turn observed failures or anomalies into clear, reproducible, evidence-based defect reports and support consistent triage. Use when a user wants to write, improve, classify, deduplicate, or assess a bug report. Do not use to invent evidence, declare an unverified root cause, or decide business priority without stakeholder input.
---

# Defect Reporting and Triage

Create defect reports that help a team understand the problem, reproduce it, judge its effect, and decide what to do next.

## Before You Start

Collect the observation, expected behavior or oracle, steps or conditions, test data, environment, build, evidence, frequency, impact, and related requirements or tests. An observed anomaly may be a product defect, test problem, environment issue, expected behavior, duplicate, or change request; do not decide without evidence.

Read [references/defect-guide.md](references/defect-guide.md) before writing or reviewing a report.

## Reporting Method

1. State the problem in a short title that identifies the affected feature and visible failure.
2. Separate expected behavior from actual behavior and cite their evidence.
3. Provide the smallest reliable reproduction path, including necessary data, state, and environment.
4. Attach or describe useful evidence without exposing secrets or personal data.
5. Explain user, business, operational, technical, security, accessibility, or compliance impact.
6. Suggest severity from observed impact and urgency from current business need, keeping severity and priority separate.
7. Check for likely duplicates and related failures without closing or merging records without authority.
8. Record uncertainty, investigation already performed, and the next useful diagnostic action.

## Working Rules

- Use neutral, factual, and blame-free language.
- Do not invent steps, logs, versions, expected results, frequency, impact, or root cause.
- Distinguish what was observed from what is suspected.
- Keep reproduction steps concise but complete enough for another person to follow.
- Include exact values and timestamps when they matter, while removing credentials and sensitive data.
- Use project severity and priority definitions when available.
- A failure's severity describes its effect; priority describes how urgently stakeholders want action.
- Do not mark a failure as intermittent merely because reproduction information is incomplete.
- For performance, security, reliability, compatibility, or accessibility issues, include the relevant conditions and measurements.
- Preserve traceability to the requirement, test, build, environment, evidence, and related defect when available.

## Expected Result

Produce a decision-ready defect report followed, when requested, by a short triage assessment covering classification, severity, priority considerations, duplicates, ownership needs, and missing evidence.


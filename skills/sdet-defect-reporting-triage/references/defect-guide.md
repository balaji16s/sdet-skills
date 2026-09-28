# Defect Reporting and Triage Guide

Adapt the report to the team's defect system. Do not add empty fields that do not help investigation or decisions.

## Core Defect Report

- **Title:** Affected area, action or condition, and visible failure.
- **Summary:** What happened, where, and why it matters.
- **Source:** Requirement, acceptance criterion, design, known correct behavior, comparison system, or other test oracle.
- **Preconditions:** Required user, data, permissions, state, configuration, or setup.
- **Steps to reproduce:** Minimal numbered actions that reliably lead to the observation.
- **Expected result:** Observable behavior supported by the source.
- **Actual result:** Observable behavior that occurred.
- **Environment:** Relevant build, version, platform, device, browser, service, configuration, locale, network, or dependency.
- **Frequency:** Reproductions / attempts, or clearly state that it is unknown.
- **Impact:** Affected users, data, business process, operations, quality characteristic, workaround, and recovery.
- **Evidence:** Logs, screenshots, video, request/response, trace, query, measurement, or file, with sensitive information removed.
- **Traceability:** Related test, requirement, risk, release, and defect identifiers.

## Severity Guidance

Use the project's scale first. If none exists, propose rather than impose:

- **Critical:** Catastrophic or widespread harm, such as serious safety, security, legal, irreversible data, or essential-service failure.
- **High:** A major function is unusable or seriously wrong, with no reasonable workaround.
- **Medium:** Meaningful impact exists, but work can continue through a practical workaround or limited path.
- **Low:** Small impact with little disruption, often cosmetic or localized.

Context can change severity. Explain the impact rather than relying on the label alone.

## Triage Checks

During triage, consider:

- Is the observation reproducible or supported by enough evidence?
- Does the expected result have a valid source?
- Is it a defect, duplicate, environment or data issue, testware issue, expected behavior, or change request?
- What is the severity, and what business factors influence priority?
- Which product area or role should investigate?
- Is more diagnostic information needed?
- Does the fix need confirmation and regression testing?
- Does the pattern suggest broader prevention or root-cause analysis?

Do not confuse classification with certainty. Keep a record of the evidence behind the triage decision.

## Suggested Output

1. **Defect report** using the relevant core fields.
2. **Triage assessment** with proposed classification, severity, priority considerations, and rationale.
3. **Missing evidence or questions** that affect reproduction or decision-making.
4. **Follow-up testing** such as confirmation, nearby regression, data cleanup, or monitoring.

## Standards Basis

This guide uses the following ISTQB syllabus sections. Page numbers refer to the printed syllabus pages, not a viewer's page offset.

- Certified Tester Foundation Level v4.0.1, section 5.5, pages 56-57: anomaly classification, defect workflow, report fields, severity, and priority.
- Certified Tester Advanced Level Test Automation Engineering v2.0, section 6.1.2, page 40, and section 7.1.3, page 46: evidence-based analysis of product, automation, and environment failures.

Examples, priority labels, output tables, and agent safety/authorization rules are original repository guidance, not mandatory ISTQB templates. These references support the testing concepts; they do not certify the skill or establish compliance with every standard cited by a syllabus.

ISTQB owns the referenced syllabi and trademarks. This independent, plain-language interpretation does not imply ISTQB endorsement or accreditation.


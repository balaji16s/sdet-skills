# Test Case Review Guide

Apply the checks that fit the test level, execution method, risk, and team conventions.

## Case-Level Checks

- **Correct:** The case tests the intended condition and the expected result agrees with the source.
- **Necessary:** The case has a clear objective and is not an unexplained duplicate.
- **Feasible:** The required state, data, tools, environment, and observations are realistically available.
- **Understandable:** Another intended user can understand and execute or maintain it without guessing.
- **Traceable:** The case links to a requirement, risk, condition, defect, model, or other clear purpose when traceability is needed.
- **Observable:** The expected result says what evidence proves success or failure.
- **Repeatable:** Re-running the case under the same relevant conditions should give a meaningful result, or known variability is explained.
- **Focused:** The case is not so broad that a failure hides its cause, and not so fragmented that it loses business meaning.
- **Maintainable:** Shared setup, data, selectors, keywords, or helpers are used sensibly without hiding important intent.
- **Safe:** Sensitive data is protected, cleanup is defined, and the case does not create uncontrolled side effects.

## Suite-Level Checks

- Important requirements and risks have suitable coverage.
- Positive, negative, boundary, alternate, error, permission, recovery, and integration behavior are balanced according to risk.
- Cases are organized and prioritized for useful feedback.
- Confirmation and regression purposes are distinguishable.
- Repeated cases have a justified platform, data, workflow, or risk purpose.
- Cases do not depend on execution order unless that dependency is intentional and controlled.
- Setup, teardown, environments, and data can support reliable execution.
- Obsolete cases, unreachable paths, weak oracles, and maintenance hotspots are visible.

## Finding Priorities

- **Blocker:** The case or suite could produce a dangerously wrong conclusion or cannot be used.
- **High:** A major risk is missed, an expected result is wrong, or failures are likely to be misleading.
- **Medium:** The issue meaningfully hurts coverage, reliability, understanding, or maintenance.
- **Low:** A useful improvement with limited immediate effect.

## Output Format

### 1. Review Summary

State the suite's purpose, overall fitness, strongest qualities, and most important problems. Avoid reducing quality to a single unexplained score.

### 2. Findings

| ID | Case or suite area | Priority | Quality check | Evidence and effect | Recommended change |
|---|---|---|---|---|---|

Use stable finding IDs such as `TCQ-001`. Distinguish confirmed problems from questions caused by missing context.

### 3. Suggested Improvements

Show representative before-and-after corrections only where examples improve understanding. Do not rewrite unaffected cases.

### 4. Coverage and Open Questions

List important missing or over-represented coverage, unknown test oracles, traceability gaps, data or environment needs, and stakeholder decisions.

## Standards Basis

This guide uses the following ISTQB syllabus sections. Page numbers refer to the printed syllabus pages, not a viewer's page offset.

- Certified Tester Advanced Level Test Analyst v4.0, section 1.3.2, page 18: test-case quality criteria and context-dependent detail.
- Certified Tester Advanced Level Test Automation Engineering v2.0, sections 7.1.2-7.1.4, pages 45-46, and section 8.1.2, pages 48-51: suite verification, unexpected results, assertions, and maintainability.
- Certified Tester Advanced Level Agile Tester v2.0, section 5.3, pages 45-47: manual-test smells.

Examples, priority labels, output tables, and agent safety/authorization rules are original repository guidance, not mandatory ISTQB templates. These references support the testing concepts; they do not certify the skill or establish compliance with every standard cited by a syllabus.

ISTQB owns the referenced syllabi and trademarks. This independent, plain-language interpretation does not imply ISTQB endorsement or accreditation.


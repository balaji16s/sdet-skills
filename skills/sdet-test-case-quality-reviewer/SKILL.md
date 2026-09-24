---
name: sdet-test-case-quality-reviewer
description: Review existing manual or automated test cases for correctness, clarity, necessity, feasibility, traceability, coverage, expected results, data, and maintainability. Use when a user wants feedback on test cases or a test suite and actionable improvements. Do not use to design a complete new test suite from requirements.
---

# SDET Test Case Quality Reviewer

Review test cases as reusable testing work, not just as text. Find problems that could produce wrong results, missed coverage, slow execution, false failures, or expensive maintenance.

## Before You Start

Read the test cases together with the available requirements, risks, expected behavior, test data, environment information, and execution history. A case cannot be judged fully without knowing what it is meant to cover.

Read [references/test-case-review-guide.md](references/test-case-review-guide.md) before reviewing the cases.

## Review Method

1. Confirm the suite's purpose, test level, audience, execution method, and source material.
2. Check each case against the quality criteria in the guide.
3. Review the suite for gaps, duplication, poor balance, hidden dependencies, and maintenance risks.
4. Link every finding to a case, source item, or suite-level pattern.
5. Explain the practical effect, such as a false result, missed risk, unclear execution, or maintenance cost.
6. Recommend the smallest useful correction. Preserve valid project conventions.
7. Summarize strengths, urgent fixes, coverage concerns, and questions that need a stakeholder.

## Working Rules

- Use plain language and give concrete evidence for each finding.
- Do not rewrite every case merely to match a preferred style.
- Keep correctness and coverage issues separate from formatting preferences.
- A case should have a purpose, but it does not always need long step-by-step instructions.
- Expected results must be observable and supported by a reliable source.
- Flag hard-coded waits, unstable data, order dependence, shared state, weak assertions, and unclear cleanup when reviewing automated cases.
- Do not recommend automation solely because a test is manual.
- Do not remove apparent duplicates until their platform, data, risk, or regression purpose is understood.
- Preserve traceability and identifiers when suggesting changes.
- Do not claim the suite is complete unless a defined coverage model supports that conclusion.

## Expected Result

Lead with the suite's overall fitness and the most consequential findings. Then provide traceable case-level and suite-level findings, improvement examples, coverage gaps, and open questions using the guide.


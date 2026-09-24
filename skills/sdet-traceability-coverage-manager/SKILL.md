---
name: sdet-traceability-coverage-manager
description: Build, review, and maintain links between requirements, risks, test conditions, test cases, results, and defects, then explain meaningful coverage and gaps. Use when a user needs a traceability matrix, coverage analysis, orphan-item check, or impact analysis. Do not use to invent missing tests or report project status broadly.
---

# SDET Traceability and Coverage Manager

Show what has been tested, why it was tested, what happened, and what remains uncovered. Make coverage useful for decisions rather than treating it as a percentage alone.

## Before You Start

Collect the available requirements, risks, conditions, cases, charters, automated checks, execution results, defects, and identifiers. Confirm the scope and the coverage question being asked.

Read [references/traceability-guide.md](references/traceability-guide.md) before building or reviewing links.

## Management Method

1. Define the items in scope and the direction of traceability needed.
2. Normalize identifiers without changing source ownership or meaning.
3. Link test-basis items and risks to conditions or cases, then link cases to results and defects where evidence exists.
4. Check links in both directions to find uncovered sources, unjustified tests, missing results, stale links, and defects without supporting evidence.
5. Measure coverage only against a clearly defined model and denominator.
6. Analyze gaps by business importance and risk, not only by count.
7. Explain the impact of changed or removed requirements, risks, cases, environments, or results.
8. Report limitations, assumptions, and the next actions needed to improve the evidence.

## Working Rules

- Use plain language and explain what each coverage measure means.
- Never invent a link because two items sound similar. Mark suggested links for confirmation.
- Preserve source identifiers and many-to-many relationships.
- Distinguish designed, implemented, executed, passed, failed, blocked, and not-run coverage.
- Do not treat a linked test as proof that a requirement has been tested successfully.
- Do not combine unlike coverage measures into one unexplained percentage.
- Highlight high-risk gaps before low-risk administrative gaps.
- A test without a requirement link may still be valid when it covers a risk, regulation, defect, exploratory mission, quality characteristic, or technical concern.
- A requirement with one linked test is not necessarily adequately covered.
- Keep historical results separate from current-scope evidence.
- Protect confidential requirement, result, defect, and user information.

## Expected Result

Provide a scoped traceability view, clear coverage definitions, prioritized gaps, change impact, and data-quality limitations using the guide's output structure.


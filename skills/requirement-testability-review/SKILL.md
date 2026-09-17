---
name: requirement-testability-review
description: Review requirements, user stories, acceptance criteria, and related specifications for clarity, completeness, consistency, and testability before detailed test design. Use when a user wants to find gaps, ambiguities, contradictions, missing acceptance criteria, or testing risks in a test basis. Do not use for writing a full test plan or a complete set of executable test cases.
---

# Requirement Testability Review

Review the supplied requirements from a tester's point of view. Help the team find problems early and turn unclear expectations into questions that people can answer.

## Before You Start

Read the available material before asking questions. The test basis may include user stories, acceptance criteria, business rules, designs, API contracts, process diagrams, or regulations.

If important context is missing, continue with a useful review where possible. Clearly label assumptions and open questions. Do not invent business rules or silently fill gaps.

Read [references/review-guide.md](references/review-guide.md) before performing the review. It defines the checks, finding priorities, and output format.

## Review Method

1. Identify the feature, users, goal, scope, and source items being reviewed.
2. Break large statements into individual behaviors or rules without changing their meaning.
3. Apply the review checks from the guide.
4. Record each meaningful issue against a specific source item or quote a short identifying phrase.
5. Explain why the issue matters and ask a direct question that can resolve it.
6. Suggest an improvement only when it follows from the supplied information. Keep it separate from the original requirement.
7. Derive a small set of high-level test conditions to show whether the requirement can be tested. Do not expand them into full test cases unless the user asks.
8. Finish with a readiness summary, important risks, assumptions, and next decisions.

## Working Rules

- Use plain language and explain uncommon testing terms when first used.
- Judge requirements in their project context. Do not demand detail that belongs in another document or a later activity.
- Separate facts, assumptions, questions, and recommendations.
- Look for both functional behavior and relevant quality needs such as performance, security, accessibility, reliability, compatibility, and usability.
- Consider normal flows, alternate flows, error handling, boundaries, state changes, permissions, data, integrations, and recovery where relevant.
- Treat examples as examples unless the source says they are complete rules.
- Do not claim that a requirement is defect-free because no issue was found.
- Do not approve or reject a product decision on behalf of its owner.
- Preserve the user's terminology unless it is inconsistent or unclear.
- Keep findings distinct and avoid reporting the same underlying issue several times.

## Expected Result

Make the review easy to act on. Lead with the overall readiness and the few issues that most affect testing or delivery. Then provide traceable findings, candidate test conditions, assumptions, and open decisions using the format in the review guide.


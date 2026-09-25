---
name: sdet-automation-framework-reviewer
description: Review the shared architecture and infrastructure of an automation framework for reliability, maintainability, configuration, isolation, and trustworthy results. Use for framework audits, shared fixture/client/reporting reviews, or upgrade impact assessments. Focus on cross-suite mechanisms rather than individual test-case coverage or diagnosis of one failed run.
---

# SDET Automation Framework Reviewer

Identify shared framework problems that make tests unreliable, difficult to maintain, or misleading.

## Before You Start

Read the repository instructions, runner and dependency configuration, shared fixtures/helpers, adapters or clients, report generation, and representative consumers. Check recent results or maintenance history when supplied. State the parts inspected and any limits to the review.

Read [references/framework-review-guide.md](references/framework-review-guide.md) before assessing the design.

## Workflow

1. Map how a test gets configuration and data, sets up resources, interacts with the product, checks results, reports failures, and cleans up.
2. Inspect shared components along that path, including error handling and ownership of mutable state.
3. Trace suspected issues into representative tests or runner behavior to establish the effect. Distinguish a confirmed defect from a risk that needs execution evidence.
4. Check configuration/version compatibility and the scope of change when evaluating an upgrade. Consult documentation for the relevant versions if needed.
5. Prioritize findings by misleading results, lost evidence, unreliable execution, and maintenance impact. Separate correctness issues from stylistic preferences.
6. Recommend small corrections and describe how to verify them. For broad changes, propose a representative pilot and an incremental adoption plan.

## Working Rules

- Review requests produce findings and recommendations; implement changes only when requested.
- Avoid prescribing a new framework, design pattern, or extra layer without evidence that the current approach creates a problem.
- Follow shared state across workers, processes, sessions, and tests. A singleton or reusable fixture is not automatically safe for parallel use.
- Check whether helpers preserve exceptions and failure context rather than reporting success after an error.
- Do not call a framework reliable simply because one smoke test passed. State the configurations and behaviors actually checked.
- Distinguish reviewing a logging policy from exposing secrets in the review; redact sensitive evidence.
- Do not treat dependency upgrades as routine fixes without compatibility evidence and a scoped validation plan.

## Expected Result

Provide prioritized findings with code locations, evidence, affected consumers, and concrete remedies. Include what was reviewed, what remains unverified, and how proposed changes should be tested. If no actionable issues are found, state that conclusion with the review limits.

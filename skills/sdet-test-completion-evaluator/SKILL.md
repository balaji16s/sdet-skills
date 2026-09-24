---
name: sdet-test-completion-evaluator
description: Assess whether testing for a milestone meets agreed objectives and exit criteria, and identify unresolved risks and handover work. Use for evidence-based test closure or completion readiness assessments. Focus on evaluating completion rather than writing a routine status report or authorizing release.
---

# SDET Test Completion Evaluator

Check whether the agreed testing work is complete and make unfinished work and remaining risk visible to the people deciding what happens next.

## Before You Start

Read the milestone scope, agreed objectives and exit criteria, test plan, versioned results, coverage, defects, exceptions, and handover obligations. If criteria are missing, ask for them or present clearly proposed criteria; do not use invented thresholds to declare completion.

Read [references/completion-guide.md](references/completion-guide.md) before assessing the evidence.

## Workflow

1. Establish the milestone, build, scope, evidence cutoff, and criteria version.
2. Match each criterion to relevant evidence and assess it as met, unmet, or unverified.
3. Examine unexecuted work, significant coverage gaps, unresolved defects, and remaining product risks.
4. Record exceptions separately, including the agreed decision and decision-maker if documented. A waived criterion remains distinguishable from one met through testing.
5. Check the readiness of testware, evidence, known-issue handover, deferred work, environment restoration, and lessons learned.
6. Summarize whether the evidence supports completion, what prevents it, and what decision or follow-up is needed.

## Working Rules

- Assess the stated scope; successful testing of one platform does not establish completion for others.
- Check that evidence still applies after relevant changes. Old passes may need renewed testing.
- Do not treat blocked, skipped, missing, or inconclusive results as successful tests.
- High pass rates do not override unmet critical criteria or missing risk coverage.
- Distinguish test completion from approval to release. Record actual approvals only when supplied.
- A completion assessment may recommend archiving or cleanup; it does not itself execute those actions.

## Expected Result

Provide a criterion-by-criterion assessment, a supported overall conclusion, remaining risks and exceptions, and a concrete handover/action list. Keep reporting prose secondary to the evidence behind the assessment.

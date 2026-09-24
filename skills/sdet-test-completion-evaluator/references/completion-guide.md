# Test Completion Guide

## Evaluate Criteria

For each criterion, preserve its wording or ID and identify the required evidence, actual evidence, build/scope, result, and gap. Use:

- **Met:** Relevant evidence demonstrates the criterion.
- **Unmet:** Relevant evidence demonstrates that the criterion is not satisfied.
- **Unverified:** Evidence is missing, ambiguous, stale, or outside the required scope.

These labels are project conventions; use equivalent team labels if supplied. Record an accepted exception alongside the result instead of converting a failure to a pass.

## Close the Work

Check whether reusable cases, scripts, data definitions, configuration, logs, and results have identified storage and ownership. Identify deferred defects or backlog work, known limitations for downstream teams, retention needs, planned environment restoration, and lessons learned. Proposed actions remain pending until there is evidence they were completed.

## Example

A release has 98 of 100 tests passing. The other two cover mandatory payment recovery and were blocked by an unavailable dependency. The pass rate does not establish that payment recovery meets its exit criterion. Mark that criterion unverified and state what evidence or documented exception is needed.

## Output

| Criterion | Required scope | Evidence and version | Met/unmet/unverified | Gap or documented exception |
|---|---|---|---|---|

Then summarize remaining risks and the readiness of handover work. For each pending action, record its purpose, responsible role, and due date if agreed. Give a conclusion such as evidence supports completion, completion is not yet supported, or a stakeholder exception decision is required, with reasons.

## Standards Basis

Paraphrased from ISTQB Certified Tester Advanced Level Test Management v3.0, section 1.1.3 (test completion activities), page 20. Evidence-status labels, the example, and the table format are project conventions.

ISTQB owns the referenced syllabus and trademarks. This independent guide does not imply endorsement or accreditation.

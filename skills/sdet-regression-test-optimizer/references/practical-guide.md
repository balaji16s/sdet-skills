# Regression Test Optimizer: Practical Guide

## Selection Worksheet

Test ID | affected behavior/risk | mandatory? | unique coverage | estimated duration and source | reliability concerns | include/defer reason.

Avoid a made-up numerical score when the inputs cannot support it. A qualitative risk order is often clearer.

## Example

A tax-rule change directly affects totals, rounding, refunds, and invoice output. Select tests for these paths and critical checkout integration. Do not limit the selection to the tax function because the same amount may be reused elsewhere. A cosmetic profile-page case may be deferred, with the decision recorded.

## Time Budget

Include environment readiness, fixture setup, execution, and likely investigation. Parallel duration depends on workers, isolation, and bottlenecks; do not divide total time by worker count without evidence.

## Uncertainty

With an incomplete dependency map, broaden representative integration checks and ask for architectural input. Keep required compliance or contractual checks even if the heuristic ranks them low. Distinguish retesting a specific fix from regression checking unchanged behavior.

## Longer-Term Changes

Recommend additions or retirement candidates separately. Removing suite content requires explicit approval and a coverage assessment.

## Source Basis

ISTQB Certified Tester Advanced Level Agile Tester v2.0, section 1.4 (regression testing approaches). The selection worksheet is a repository aid, not a prescribed ISTQB formula.

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

# White Box Test Designer: Practical Guide

## Coverage Definitions

Statement coverage asks which executable statements ran. Decision coverage asks whether each decision outcome occurred. Condition coverage asks about individual Boolean condition outcomes. MC/DC additionally demonstrates that each condition can independently change its decision's result under the selected definition. Multiple-condition coverage targets combinations; feasibility and evaluation semantics matter.

Always define the denominator. Excluding unreachable code is a documented decision, not a silent way to improve a score.

## Worked Design Example

For a pure Boolean decision D = A AND B, with independent inputs:

| Case | A | B | D |
|---|---|---|---|
| T1 | true | true | true |
| T2 | false | true | false |
| T3 | true | false | false |

T1/T2 demonstrate A's independent effect; T1/T3 demonstrate B's. This is a logical design. In a short-circuit language B is not evaluated in T2; document how the selected instrumentation and coverage definition handle this. Do not claim a measured MC/DC result from this table alone.

The expected business outcome still needs a requirement. The decision expression only tells us what the current code does.

## Case Record

Case ID | inputs/state | expected result and source | structural items targeted | execution evidence, if any.

## Limits

Dependent conditions may make logical combinations impossible. Loops may require additional behavior-focused tests even after statement or decision coverage. Do not attribute basis-path coverage to the removed chapter in TTA v4.0.

## Source Basis

ISTQB Certified Tester Advanced Level Technical Test Analyst v4.0, sections 2.1–2.5 and 2.8 (white-box coverage and technique selection).

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

# Test Smell Reviewer: Practical Guide

## Patterns to Inspect

- Hidden dependencies on another case, account state, or execution order.
- Deeply nested calls to other procedures that make execution difficult to follow.
- Expected results such as “works correctly” or “A or B” without the rule selecting the result.
- Actions hidden in expected results.
- Long cases checking unrelated goals, or unclear bundles of actions.
- Fixed data likely to expire or collide with concurrent testers.
- Unstated environment requirements, missing reset steps, and copied steps that drift apart.
- Terminology or formatting that changes the intended meaning.

## Example

Before: “Submit payment. Expected: success or error.”
Finding: the tester cannot judge the result because input conditions and the selecting rule are missing.
After, as a proposal: “Using a valid test payment token, submit the order. Verify the order reaches the state required by the supplied payment contract.”
If the contract is missing, ask for it rather than inventing the state.

## Review Record

Case/step | pattern | why it matters here | suggested change | tradeoff | priority.

## Avoid Mechanical Cleanup

Two similar cases may cover different permissions or configurations. A long end-to-end case may intentionally check state transitions. Recommend change only when its benefit and retained coverage are clear.

## Source Basis

ISTQB Certified Tester Advanced Level Agile Tester v2.0, section 5.3 (manual test smells).

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

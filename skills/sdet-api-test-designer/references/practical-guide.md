# API Test Designer: Practical Guide

## Scenario Matrix

ID | operation/risk | role and setup | request variation | expected response | expected state/side effect | source | priority.

Use the protocol's own semantics. For HTTP, check relevant status, headers, body, and side effects. For messages or RPC, check acknowledgments, delivery assumptions, serialization, and observable outcomes.

## Questions Worth Asking

Can one caller access another caller's object? What happens when a request is repeated? Are partial failures atomic? How are errors represented? How are paging, ordering, versioning, and rate limits specified? Which observations establish completion for asynchronous work?

Select relevant questions; do not generate an enormous generic checklist for a small interface.

## Example

An order-creation contract supports an idempotency key. Design a repeat-request test that checks the documented response and confirms the allowed number of orders. If the contract says nothing about charging or key expiry, raise questions rather than assume those guarantees.

## Boundaries

The scenario matrix is not executable automation. Use the automation engineer for implementation. API security scenarios are limited coverage, not a claim of a comprehensive penetration test. Fake dependencies cannot establish that the real integration works.

## Source Basis

ISTQB Certified Tester Advanced Level Technical Test Analyst v4.0, section 2.7 (API testing). Contract matrices and protocol-specific prompts are repository implementation aids.

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

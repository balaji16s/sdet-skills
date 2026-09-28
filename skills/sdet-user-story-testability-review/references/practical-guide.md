# User Story Testability Review: Practical Guide

## Review Prompts

Can someone demonstrate the user outcome? What state must exist first? What does success look like? What happens when a rule fails? Which roles can perform the action? Are timing, amounts, units, and limits defined where they matter?

An acceptance criterion describes observable behavior, not merely an implementation task. “Add a refund button” does not establish who may refund, which orders qualify, or what happens to the balance.

## Slicing

Consider user workflows, scenarios, data complexity, or a thin end-to-end outcome. An independently testable API slice can be useful where the team intends staged delivery. Do not force every story into a full UI-to-database slice. Rewrite the criteria rather than copying the original large set into every slice.

Use: original criterion → proposed slice → retained or deferred behavior → dependency or owner.

## Example

For “customers can cancel orders easily,” ask which order states allow cancellation and how payment is handled. A proposed slice might cover an unpaid order before dispatch. Paid orders remain an explicit follow-up, not a silently omitted requirement. Cancellation eligibility is a question until the product owner supplies the rule.

## Review Output

Finding ID | story location | ambiguity or gap | testing impact | proposed clarification | decision owner.

## Source Basis

ISTQB Certified Tester Advanced Level Agile Tester v2.0, sections 4.1.1–4.1.5 (testware, shared examples, biases, and story slicing).

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

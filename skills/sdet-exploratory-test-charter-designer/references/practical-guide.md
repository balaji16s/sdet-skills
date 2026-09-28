# Exploratory Test Charter Designer: Practical Guide

## Charter Template

- Mission: explore [area] with [perspective or variation] to learn [risk or question].
- Scope and exclusions:
- Environment, permission, data, and reset needs:
- Sources for judging behavior:
- Starting ideas, not mandatory steps:
- Proposed timebox:
- Record: configuration, actions, observations, evidence, questions, and interruptions.
- Debrief: what was learned, what remains uncertain, and what to investigate next.

## Example

Explore shopping-cart recovery after session expiry to learn whether customers lose items or accidentally submit duplicate orders. Use synthetic accounts in an approved test environment. Vary expiry timing and browser refresh; compare outcomes against the supplied session and order rules. Where a recovery rule is missing, record a question instead of assuming a defect.

## Choosing Scope

A useful charter is narrower than “test checkout” and more adaptable than a fixed sequence of clicks. Stop or revise the mission when an unexpected issue changes the risk. A suggested 45-minute session is a local choice, not an ISTQB requirement.

## Handoff

Use recorded notes with the session-analysis skill. A promising idea that was not attempted must remain untested, not reported as covered.

## Source Basis

ISTQB Certified Tester Advanced Level Agile Tester v2.0, sections 5.1.4 (charters) and 5.1.5 (session-based exploratory testing).

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

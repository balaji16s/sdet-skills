# Exploratory Session Analyzer: Practical Guide

## Evidence Ledger

Observation ID | note or artifact reference | action and context | observed result | expected-behavior source | interpretation | next check.

Use “unknown” where the notes do not establish a fact. Distinguish a screenshot showing a message from evidence that a backend transaction succeeded.

## Example

Notes say “after reconnecting, two orders appeared” and include a screenshot, but no request IDs or payment history. Report a suspected duplicate-order issue. Do not claim two charges occurred. Request order IDs, network evidence, and the applicable retry rule before preparing a stronger defect report.

## Coverage and Time

Compare the actual areas investigated with the mission, not with an invented exhaustive list. If the notes record only session start and end, report elapsed session time; do not pretend to know minutes spent testing, investigating defects, or handling setup.

## Debrief Questions

What did the tester learn? Which expectation changed? What blocked progress? Which risky area was not reached? What evidence would distinguish competing explanations?

## Handoff

Send a reproducible finding to defect reporting. Send an uncertain but important risk to a new charter. Keep raw evidence references available and redact secrets or personal data in summaries.

## Source Basis

ISTQB Certified Tester Advanced Level Agile Tester v2.0, section 5.1.5 (session-based exploratory testing and debriefing).

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

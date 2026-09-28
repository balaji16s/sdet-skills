# Technical Review Facilitator: Practical Guide

## Tailor the Checklist

Architecture: responsibilities, interface assumptions, failure propagation, concurrency, caching, resource limits, observability, and changeability.

Code: correctness against requirements, arithmetic boundaries, branching, loops, exceptions, resource lifetime, and relevant concurrency risks.

Operational procedures: prerequisites, permissions, failure detection, recovery, and verifiable completion.

Select only relevant lenses and explain why they matter.

## Finding Record

ID | artifact/revision/location | observed evidence | concern and impact | category | question or proposed action | owner/status.

Suggested owners remain proposed until confirmed. Keep unresolved disagreements visible.

## Example

A design caches account permissions but does not define invalidation after access removal. Record the missing rule and possible continued access. Ask the owner to define acceptable propagation and invalidation behavior. Do not declare an exploitable defect or invent a time limit without evidence.

## Review Session Aid

State the decision needed, allow preparation, walk through high-risk findings, capture disagreements, and identify what evidence would close each action. Keep style preferences separate from behavior or architecture risks.

## Completion

A review can finish with open actions. “Reviewed” does not mean “approved,” and “approved” does not mean every risk has been removed.

## Source Basis

ISTQB Certified Tester Advanced Level Technical Test Analyst v4.0, sections 5.1–5.2 (technical reviews) and 4.6 (maintainability).

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

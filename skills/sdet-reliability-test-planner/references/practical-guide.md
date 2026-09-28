# Reliability Test Planner: Practical Guide

## Scenario Record

Failure mode | user/business impact | workload/state | expected tolerance or recovery | evidence | maximum permitted impact | stop/restore steps | owner.

Separate recovery time objective (how quickly service must return) from recovery point objective (how much recent data loss is acceptable). Use supplied definitions and targets; these labels do not supply values by themselves.

## Example

Plan a payment-worker restart while synthetic orders are in progress. Define checks for lost and duplicate processing according to the actual delivery and idempotency contract. Plan how to restore the worker and confirm order/payment consistency. Do not assume exactly-once behavior.

## Restore Coverage

Identify the backup version, restoration target, access requirements, dependencies, integrity checks, and business validation. Restore into a controlled target unless an explicitly authorized recovery exercise says otherwise.

## Measurement Caution

Record duration, workload, failure count, downtime definition, excluded maintenance, and detection limits. A single recovery exercise demonstrates that observed scenario, not every possible failure. Statistical reliability claims require an appropriate model and sufficient evidence.

## Safe Handoff

Keep execution gated on environment readiness, owner permission, observability, bounded impact, and a usable recovery procedure. If recovery itself is uncertain, resolve that risk before recommending a disruptive experiment.

## Source Basis

ISTQB Certified Tester Advanced Level Technical Test Analyst v4.0, sections 4.2, 4.4, and 4.9 (reliability and operational profiles).

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

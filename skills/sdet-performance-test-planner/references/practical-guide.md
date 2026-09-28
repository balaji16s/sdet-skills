# Performance Test Planner: Practical Guide

## Measurement Contract

Metric | start/end boundary | unit | aggregation/window | sample needs | acceptance source | owner.

Define where timing starts and stops. Report successful and failed outcomes together so apparently fast errors do not improve the performance conclusion. Choose percentiles where appropriate, and keep raw counts and sample limitations visible.

## Workload Record

Journey mix, arrival/concurrency model, pacing, payload and database sizes, cache state, background work, and workload source. Forecasts are assumptions until verified.

## Example

A team expects a promotion peak but has no traffic forecast. Propose a staged baseline and ask the business owner for peak arrival assumptions. Do not declare “1,000 users and p95 below 200 ms” as the requirement. Record those values only if supplied or explicitly marked as proposed.

## Execution Readiness

Check monitoring, generator headroom, data reset, third-party limits, approved test window, cost cap, and an operator who can stop the run. Stress tests need stricter guardrails and recovery verification.

## Interpretation

Compare equivalent configurations and workloads. Investigate saturation, error rates, latency distribution, and recovery together. Correlation with a resource spike suggests a bottleneck hypothesis, not proof of root cause.

## Source Basis

ISTQB Certified Tester Advanced Level Technical Test Analyst v4.0, sections 4.2, 4.5, and 4.9 (performance planning and operational profiles). Percentile and safety templates are practical repository guidance.

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

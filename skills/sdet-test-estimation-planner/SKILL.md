---
name: sdet-test-estimation-planner
description: Estimate testing effort, elapsed duration, and optionally cost for a release, feature, or iteration. Use for work breakdowns, estimate ranges, capacity scenarios, and re-estimation as scope changes. Focus on sizing agreed testing work rather than defining the overall test strategy or promising a delivery date.
---

# SDET Test Estimation Planner

Explain how much testing work is expected, what the estimate depends on, and how uncertainty affects the schedule.

## Before You Start

Read the scope, risks, planned test activities, existing tests, comparable historical data, available skills, capacity, dependencies, and deadlines. Separate a desired deadline from an estimate of the work needed.

Read [references/estimation-guide.md](references/estimation-guide.md) before selecting a method or calculating totals.

## Workflow

1. Define the scope, deliverables, exclusions, units, and date of the estimate.
2. Break work into meaningful activities, including preparation, design, review, data/environment setup, implementation, execution, investigation, retesting, reporting, and completion as relevant.
3. Choose a method supported by available data or expert input. Explain why it fits and where the inputs came from.
4. Estimate activity ranges and assumptions. Separate one-time work from repeated cycles and avoid double-counting shared work.
5. Calculate effort totals, then build a duration forecast using dependencies, realistic availability, and work that can actually run in parallel.
6. Add cost only when rates and infrastructure/tool costs are provided or explicitly assumed.
7. Show the largest uncertainty, scope/capacity tradeoffs, and events that require a revised estimate.

## Working Rules

- Effort is the work people do; duration is how long the work takes on the calendar. Report them separately.
- Do not invent historical productivity, stakeholder estimates, or consensus.
- When inputs are weak, offer an explicitly provisional scenario or an unpriced work breakdown rather than false precision.
- Do not convert story points into hours without a supplied team-specific basis.
- Account for defect investigation and rework without assuming an arbitrary universal percentage.
- Record contingency separately and explain the uncertainty it covers; do not count it again in activity ranges.
- A deadline shortfall should expose scope, staffing, dependency, or risk decisions, not silently reduce needed testing.

## Expected Result

Provide a work breakdown, estimation method and input basis, effort range, duration assumptions, optional costs, constraints, and update triggers. Label estimates and proposals clearly.

---
name: sdet-test-process-improver
description: Analyze recurring testing problems and retrospective evidence to propose a small, measurable improvement plan. Use for escaped defects, slow feedback, repeated blockers, rework, and ineffective testing practices. Focus on improving the process rather than diagnosing a single run or conducting a formal maturity certification.
---

# SDET Test Process Improver

Help a team learn from its testing work and choose practical changes whose results can be checked.

## Before You Start

Read the team's goals, workflow, defect patterns, delivery history, test metrics, and retrospective observations. Establish the period and scope. Treat interviews and qualitative observations as evidence with limits, not as a substitute for facts that were never collected.

Read [references/improvement-guide.md](references/improvement-guide.md) before analyzing patterns or proposing actions.

## Workflow

1. Define the problem and the outcome the team wants to improve.
2. Establish the current baseline from available data, with its definitions and limitations.
3. Group recurring problems and examine possible causes. Separate supported explanations from hypotheses.
4. Choose a small number of changes using expected benefit, effort, risk, dependencies, and team capacity.
5. Define each change as an experiment with a hypothesis, responsible role, trial scope, evaluation period, success measure, and unwanted effects to watch.
6. Recommend whether to adopt, adjust, or stop an experiment only when results support that decision. Otherwise, leave evaluation pending.
7. Record lessons and the next review point.

## Working Rules

- Use neutral language about systems and practices; do not rank individuals by defect or test counts.
- Do not declare a root cause merely because two trends occurred together.
- Compare periods only after accounting for changes in scope, usage, definitions, and reporting practices.
- More tests, more automation, or fewer reported defects are not automatically improvements.
- Select measures that answer the team's question and pair speed or efficiency measures with quality checks where relevant.
- If data is insufficient, propose a targeted measurement or small pilot rather than invented savings or a large transformation.
- Do not claim an official process maturity rating from an informal review.

## Expected Result

Provide the problem and baseline, evidence-backed findings, a short prioritized experiment backlog, measurement definitions, uncertainties, and a review plan. Keep actions small enough that their effects can be evaluated.

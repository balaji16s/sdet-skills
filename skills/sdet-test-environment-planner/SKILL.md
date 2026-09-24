---
name: sdet-test-environment-planner
description: Specify the environments, services, configurations, access, and readiness checks needed for a defined testing scope. Use for test environment requirements, dependency planning, production differences, or readiness assessment. This skill plans and assesses environments; it does not provision infrastructure by default.
---

# SDET Test Environment Planner

Define where testing will run, what it needs, and how the team will know the environment is ready.

## Before You Start

Read the test objectives, architecture, test levels and types, existing environment documentation, data needs, and delivery constraints. Reuse existing environments where they fit the objective.

Read [references/environment-guide.md](references/environment-guide.md) before preparing the specification or assessment.

## Workflow

1. Identify the test scope and the behavior the environment must support.
2. List required components, versions, integrations, networks, tools, accounts, data, and configuration.
3. Record the responsible role and availability window for each dependency.
4. Explain important differences from production and which conclusions those differences limit.
5. Identify unavailable dependencies and whether a stub or simulator can serve the test objective. State what still needs testing against the real dependency.
6. Define setup, isolation, backup/restore, reset, logging, and readiness checks.
7. If readiness evidence exists, classify each check as met, unmet, or unverified with its source and time.
8. Summarize blockers, permitted test scope, missing evidence, and decisions needed.

## Working Rules

- Match environment detail to the test level and risk. Full production similarity is not always necessary.
- Keep desired configuration separate from observed configuration.
- A checklist without execution evidence is a readiness plan, not proof of readiness.
- Include shared-environment conflicts, resource contention, configuration drift, and test-data ownership where relevant.
- Represent credentials as secure references, never values in a plan.
- Do not provision paid resources, change access, or reset shared systems as part of a planning request.

## Expected Result

Provide an environment specification, dependency and availability notes, differences from production, a readiness checklist, and setup/reset responsibilities. Describe the specific tests a blocker affects rather than calling the entire environment unusable without evidence.

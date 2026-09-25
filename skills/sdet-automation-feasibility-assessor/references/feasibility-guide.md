# Automation Feasibility Guide

## Assess Value and Readiness Separately

Value includes faster useful feedback, risk coverage, repeatability, execution frequency, and checks that are impractical by hand. Readiness includes an observable expected result, controllable starting state, usable interfaces, accessible data, stable dependencies, and a team able to maintain the solution.

Use a candidate table when it helps comparison:

| Candidate and risk | Expected result and observation | Value | Readiness gaps | Effort/maintenance basis | Recommendation |
|---|---|---|---|---|---|

Useful recommendation labels are:

- **Automate now:** The value is clear and the necessary conditions are available.
- **Pilot first:** There is plausible value but an important uncertainty needs a bounded experiment.
- **Prepare first:** A known gap, such as missing test data or an unobservable result, must be addressed.
- **Retain human evaluation:** Human observation or judgment remains necessary for the stated objective; automation may still assist preparation or evidence collection.

These labels are project conventions. Use the team's equivalents when supplied.

## Tool Comparison

Compare tools against requirements, not popularity. Consider supported interfaces/platforms, existing language and runner, deployment constraints, result reporting, integration, team skills, maintenance, and licensing. Record an official source or pilot observation for each material claim and leave unknowns visible. Do not treat one successful demonstration as evidence of all required capabilities.

## Pilot Design

Include a representative successful case, an expected failure, setup/reset behavior, and the hardest relevant dependency. Identify the run conditions, effort limit, ownership, and how the team will measure reliability, feedback time, diagnosis effort, and maintenance. When pipeline use is intended, include an unattended run in the pilot scope.

## Example

A daily invoice calculation check has specified rounding rules and an accessible API. It is a strong automation candidate if account data can be reset. A request to decide whether the invoice screen feels intuitive still needs user judgment; automated checks can assist but cannot establish that subjective outcome by themselves.

If comparing cost, state assumptions explicitly. Saving 15 minutes on each of 20 runs gives 5 gross hours saved, before development, investigation, and maintenance costs. It does not establish a positive return by itself.

## Standards Basis

Paraphrased from ISTQB Certified Tester Advanced Level Test Automation Engineering v2.0: section 1.1.1 (advantages and limitations), page 15; sections 2.2.1-2.2.2 (system analysis and tool evaluation), page 20; section 4.1.1 (pilots), page 30. The examples, labels, and comparison format are independent project conventions.

ISTQB owns the referenced syllabus and trademarks. This independent guide does not imply endorsement or accreditation.

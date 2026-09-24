# Test Estimation Guide

## Choose a Method

- **Comparable work:** Use measured work from a similar task and explain differences in scope, complexity, tooling, and team experience.
- **Ratios or extrapolation:** Use relevant historical ratios or early measured progress only when units and work are comparable. Do not assume all test cases take equal effort.
- **Expert estimates:** Gather estimates from people with relevant knowledge. If no experts supplied input, label the agent's range as provisional rather than calling it consensus or Delphi.
- **Three-point estimation:** When optimistic, most likely, and pessimistic inputs are available, report the three values and the chosen combination method. Do not infer a statistical confidence level from three guesses.

## Build a Credible Forecast

Record each activity's effort unit, input source, assumptions, range, dependencies, and resource needs. Check the total with consistent units. Working days depend on actual calendars; elapsed time also includes waits and unavailable services. Parallel work still consumes effort, and adding people cannot divide sequential work without limit.

Consider data/environment preparation, learning, reviews, automation maintenance, execution, investigation, fixes supplied by others, confirmation, regression, and reporting. Separate waiting time from active effort. In Agile work, check whether testing is already included in the team's story estimate before adding it again.

## Example

Illustrative inputs: 24 person-hours of preparation and 16 person-hours of execution, with one tester available for 5 focused hours per working day. This totals 40 person-hours and at least 8 working days if the activities are sequential. A two-day environment wait affects elapsed duration if it cannot overlap with other work; it does not automatically add 10 person-hours of effort. These figures illustrate the method and are not productivity benchmarks.

## Output

| Activity | Input basis | Effort range and unit | Dependencies | Key assumption |
|---|---|---|---|---|

Follow with totals, a capacity and sequencing explanation, optional cost calculation, uncertainty, and tradeoffs. Re-estimate when scope, defect rates, availability, dependencies, or measured progress materially change.

## Standards Basis

Paraphrased from ISTQB Certified Tester Advanced Level Test Management v3.0, sections 2.2.1-2.2.3, pages 52-54. The example and output table are project conventions.

ISTQB owns the referenced syllabus and trademarks. This independent guide does not imply endorsement or accreditation.

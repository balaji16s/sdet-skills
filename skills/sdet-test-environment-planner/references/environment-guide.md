# Test Environment Guide

## Specification

For each item, record its ID, purpose, required version/configuration, responsible role, availability window, and important differences from production. Include relevant hardware, software, services, network routes, interfaces, security roles, tools, data, and storage.

Use existing documentation as a baseline and describe changes. Identify prerequisites and setup order rather than presenting dependent items as independently available.

## Readiness Checks

Choose checks that establish the required starting conditions:

- deployed build and schema match the planned versions;
- required services and integrations are reachable;
- test roles have the intended permissions;
- data and fixtures are available in a known state;
- logs and results can be written and retrieved;
- capacity and isolation support the planned load or concurrent runs;
- reset and recovery procedures have evidence where required.

For each check, state the expected observation, evidence needed, responsible role, and result if known. A service health endpoint alone does not establish that a business transaction works.

## Example

A payment simulator can support testing how checkout handles a timeout. It cannot establish that the real provider accepts the application's authentication or request format. Record both the simulated scope and the outstanding provider integration check.

## Output

| Item ID | Requirement and purpose | Version/configuration | Responsible role | Needed when | Production difference |
|---|---|---|---|---|---|

Add a readiness table with check, expected observation, result, evidence/time, and affected tests. Finish with setup/reset requirements and unresolved dependencies. Use proposed roles if ownership has not been agreed.

## Standards Basis

Paraphrased from ISTQB Certified Tester Advanced Level Test Analyst v4.0, section 1.3.3, page 19; and Advanced Level Test Automation Engineering v2.0, section 7.1.1, pages 44-45. The example and table format are project conventions.

ISTQB owns the referenced syllabi and trademarks. This independent guide does not imply endorsement or accreditation.

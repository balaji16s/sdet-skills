# Compatibility Portability Test Planner: Practical Guide

## Separate the Concerns

Coexistence: applications sharing resources without harmful interference.
Interoperability: systems exchanging and using information correctly.
Installability: installing, upgrading, removing, or recovering an interrupted installation.
Adaptability: working in intended target environments.
Replaceability: substituting a component while retaining required behavior.

These terms follow the cited syllabus's model; projects may use a different version of a quality model.

## Matrix

Configuration/path | support source | usage/risk | selected checks | evidence required | included/deferred reason.

Filter impossible combinations before selecting samples. Record version boundaries and required integration contracts. Add targeted multi-factor cases where known risks exceed pairwise interactions.

## Example

For a database-driver upgrade, plan checks on supported database versions, connection behavior, serialization, transactions, and a representative business journey. Include rollback only if supported, and verify retained data after the change. Testing one database version does not support a claim about all versions.

## Migration Safety

Use disposable or backed-up test data and a controlled target. Check prerequisites, permissions, interrupted installation state, and post-install operation. A plan does not authorize replacing components or removing installations.

## Source Basis

ISTQB Certified Tester Advanced Level Technical Test Analyst v4.0, sections 4.7–4.8 (portability and compatibility). Interoperability detail is a practical extension of the listed characteristic.

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

---
name: sdet-test-data-designer
description: Define test data requirements and design synthetic datasets or fixtures for existing test conditions. Use for realistic records, boundary and invalid data, related entities, time-sensitive data, and repeatable setup and cleanup. Focus on data preparation rather than selecting the overall test approach or creating a complete test suite.
---

# SDET Test Data Designer

Help testers get the right data into the right state so their tests check the intended behavior.

## Before You Start

Read the available test conditions, business rules, schemas, sample formats, target environment, and privacy constraints. Ask for a missing schema or rule when it would materially change the data. Otherwise, mark assumptions and provide the useful part of the design.

Read [references/data-guide.md](references/data-guide.md) for data selection, lifecycle checks, and a worked example.

## Workflow

1. Link each data need to a test condition, requirement, or risk. Identify the result or state that the data must support.
2. Identify entities, required fields, relationships, permissions, and setup order.
3. Select realistic valid records, boundaries, invalid records, and combinations that serve those test conditions.
4. Specify values, formats, quantities, time assumptions, and the reason for each variation.
5. Define how to create, isolate, refresh, reset, and remove the data. Account for concurrent test runs and records changed by tests.
6. When asked to generate fixtures, use the supplied format and validate syntax, schema constraints, and relationships with available tools. Report exactly what was checked.
7. Explain gaps and limitations, including unrealistic distributions or dependencies that were simulated.

## Working Rules

- Use synthetic data by default. Do not copy production records or credentials into examples.
- Anonymized and pseudonymized data are different: replacing names does not guarantee that people cannot be identified.
- For negative tests, break the intended rule while keeping unrelated prerequisites valid. Explain deliberate exceptions such as malformed payload tests.
- Keep generated examples separate from confirmed business rules. Do not invent limits or expected results.
- Treat dates, time zones, expiration, uniqueness, and linked records as part of repeatability.
- A data design does not imply permission to insert, overwrite, or delete records in a connected system.

## Expected Result

Provide a data specification linked to test purposes, requested sample records or fixtures, setup and reset guidance, validation results, and unresolved questions. Keep the output small enough to use and extend.

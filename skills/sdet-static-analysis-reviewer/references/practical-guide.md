# Static Analysis Reviewer: Practical Guide

## Review Lenses

Control flow: unreachable branches, missing outcomes, termination risks, and exception paths.

Data flow: use before initialization, values overwritten before use, invalid lifetime assumptions, and definitions that do not reach intended uses.

Resources: acquisition/release pairing and cleanup on early returns or exceptions. Account for language-managed resources and ownership transfer.

Maintainability: complexity, coupling, and unclear boundaries where they create a concrete change or testing risk.

## Example

A tool reports a possible null dereference. The function checks for null on one branch but not another. Inspect callers and relevant assignments. If a documented invariant guarantees a non-null value, record that evidence and any uncertainty about enforcement. If not, explain the feasible risky path and propose a focused test. Do not call it reproduced without execution.

## Finding Template

ID | file/line/revision | tool rule or manual observation | path/data reasoning | impact | confidence | verification or proposed remedy.

## Reporting Limits

A clean report means no findings under that configuration, not defect-free code. Do not compare warning counts across different rule sets as if they measure equivalent quality. Keep suggested fixes separate from observed facts.

## Source Basis

ISTQB Certified Tester Advanced Level Technical Test Analyst v4.0, sections 3.1–3.2 (static analysis) and 4.6 (maintainability).

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

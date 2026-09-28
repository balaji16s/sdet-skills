# Security Test Planner: Practical Guide

## Risk-to-Check Matrix

Asset | threat or misuse | existing control | planned check | expected result source | environment/accounts | evidence | priority.

Consider authentication, authorization, object ownership, session boundaries, sensitive-data exposure, input handling, and auditability where applicable. These prompts are not an exhaustive security standard.

## Example

For a multi-tenant invoice service, plan a check that a synthetic user from tenant A cannot retrieve tenant B's invoice. The required denial behavior comes from the access policy. Run only against approved test tenants, and preserve redacted request/response evidence. Do not use actual customer invoices.

## Authorization Gate

Identify the approving owner, exact systems, allowed activities, prohibited actions, dates, limits, and emergency contact. Cloud providers and other third parties may need separate authorization. An incomplete authorization record is a blocker for execution, not a reason to guess scope.

## Safety and Conclusions

Plan how to stop on unexpected exposure, instability, or out-of-scope access. Minimize collected data and restrict evidence access. Passing selected checks does not establish absence of vulnerabilities. Report untested trust boundaries and dependencies.

The plan does not execute scans or attacks. Detailed specialist methods require the appropriate expertise and a separately authorized task.

## Source Basis

ISTQB Certified Tester Advanced Level Technical Test Analyst v4.0, sections 4.2–4.3 (non-functional and security test planning). Authorization gates are additional repository safety guidance.

This is original, plain-language guidance informed by that syllabus, not an official ISTQB procedure. Examples and templates are illustrative; project rules and stakeholder decisions must be supplied or confirmed.

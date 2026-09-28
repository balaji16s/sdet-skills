# Test Strategy Guide

Use only the sections that influence the work. A small feature may need a short strategy; a large or regulated system may need more detail.

## Strategy Decision Areas

### Context and Objectives

- What product or change is being tested?
- Which release, iteration, or decision does the strategy support?
- Who needs information from testing?
- What must testing demonstrate, discover, prevent, or measure?

Write objectives as outcomes, not activities. "Provide evidence that authorized customers can complete payment without duplicate charges" is more useful than "perform payment testing."

### Scope and Risk

- Identify included features, interfaces, platforms, data flows, and quality areas.
- Record meaningful exclusions and their consequences.
- Link important risks to the planned test response.
- State which remaining risks need stakeholder acceptance or another control.

### Test Approach

Choose and justify the relevant combination of:

- static testing such as requirement, design, code, or testware reviews;
- component, component-integration, system, system-integration, and acceptance testing;
- functional and relevant non-functional testing;
- black-box, white-box, experience-based, and collaboration-based techniques;
- confirmation testing for fixes and regression testing for unintended effects;
- scripted, exploratory, manual, and automated checks.

The names may differ across organizations. Preserve local terminology and explain any mapping.

### Testware and Traceability

Describe the needed test conditions, cases, charters, data, scripts, suites, logs, reports, and other evidence. State how requirements and risks will be linked to tests, results, and defects when traceability is valuable or required.

### Environments, Data, Tools, and Automation

State important environment configurations, integrations, simulators, devices, accounts, and observability needs. Describe test-data creation, privacy, reset, and retention needs. Explain tool or automation choices in terms of value, maintainability, feedback speed, and risk.

### People and Responsibilities

Identify the skills and roles needed, stakeholder participation, review responsibilities, and useful independence. Support whole-team ownership of quality while preserving independent evaluation where risk justifies it.

### Control and Reporting

Define useful entry, suspension, resumption, and completion criteria. Select metrics that connect to objectives, risks, progress, product quality, defects, or coverage. State the audience, reporting rhythm, escalation path, and how the approach will change when evidence changes.

### Completion and Improvement

Define expected test deliverables, stored evidence, unresolved defects, known limitations, remaining risks, handover needs, and lessons to capture.

## Suggested Output

1. **Strategy summary:** context, objectives, highest risks, and key choices.
2. **Scope:** included items, exclusions, assumptions, and dependencies.
3. **Approach:** test levels, types, techniques, static testing, regression, and exploratory work.
4. **Test support:** environments, data, tools, automation, and configuration control.
5. **People and workflow:** responsibilities, collaboration, independence, and defect handling.
6. **Control:** prioritization, traceability, criteria, metrics, reporting, and adaptation triggers.
7. **Deliverables and remaining risk:** evidence, completion, handover, limitations, and open decisions.

## Standards Basis

This guide uses the following ISTQB syllabus sections. Page numbers refer to the printed syllabus pages, not a viewer's page offset.

- Certified Tester Foundation Level v4.0.1, sections 5.1.1-5.1.3, pages 48-49: objectives, scope, approach, resources, and entry/exit criteria; sections 5.2-5.3.3, pages 51-55: risk, control, and reporting.
- Certified Tester Advanced Level Agile Tester v2.0, sections 3.1.1-3.1.2, pages 24-26: iteration/release planning and context-specific project test strategy.
- Certified Tester Advanced Level Test Analyst v4.0, sections 1.3.3-1.3.5, pages 19-21: environments, expected-result sources, and data.
- Certified Tester Advanced Level Test Management v3.0, section 1.1.3, page 20: completion and handover.

Examples, priority labels, output tables, and agent safety/authorization rules are original repository guidance, not mandatory ISTQB templates. These references support the testing concepts; they do not certify the skill or establish compliance with every standard cited by a syllabus.

ISTQB owns the referenced syllabi and trademarks. This independent, plain-language interpretation does not imply ISTQB endorsement or accreditation.


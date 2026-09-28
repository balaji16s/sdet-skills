# sdet-skills

Reusable AI agent skills for quality engineers, QA engineers, SDETs, developers, and test leaders.

These skills guide AI coding agents through practical quality-engineering work. The collection covers the Software Testing Life Cycle (STLC), from requirements and planning to completion and improvement, alongside automation, Agile and exploratory testing, and specialist technical testing.

## Who This Is For

This repository is useful for:

- QA engineers who want consistent and practical testing outputs from AI agents
- SDETs building or maintaining test automation and quality-engineering workflows
- Developers who want earlier and clearer testing feedback
- Test leads who want to standardize testing practices across a team
- Learners who want examples of applying established testing principles to real work

## Available Skills

Each skill has a focused purpose and can be installed independently. The planned collection is now authored: 33 skills, including consolidated automation responsibilities rather than separate packages for every overlapping topic. This is a catalog milestone, not a claim that every skill has passed real-project evaluation.

### Core STLC and Automation

| Skill | What it does | Example use case |
|---|---|---|
| [`sdet-requirement-testability-review`](skills/sdet-requirement-testability-review/) | Finds unclear, incomplete, conflicting, or untestable requirements before detailed test design begins. | Compare a refund policy with an API specification and identify conflicting limits and missing rules. |
| [`sdet-risk-based-test-planner`](skills/sdet-risk-based-test-planner/) | Identifies the most likely and harmful risks so testing focuses on what matters most. | Prioritize payment failures and data-loss risks above low-impact visual issues for a release. |
| [`sdet-test-strategy-designer`](skills/sdet-test-strategy-designer/) | Creates a practical testing approach covering objectives, scope, risks, test types, environments, people, automation, and reporting. | Define how a team will test a new checkout service across component, API, integration, system, and acceptance levels. |
| [`sdet-test-technique-designer`](skills/sdet-test-technique-designer/) | Selects and applies suitable test techniques to derive effective and traceable tests. | Use equivalence partitions and boundary values to test an age field, or a decision table to test discount rules. |
| [`sdet-test-case-quality-reviewer`](skills/sdet-test-case-quality-reviewer/) | Reviews existing test cases for correctness, clarity, coverage, reliability, traceability, and maintainability. | Find weak expected results, duplicate cases, hidden dependencies, and missing negative coverage in a regression suite. |
| [`sdet-traceability-coverage-manager`](skills/sdet-traceability-coverage-manager/) | Connects requirements, risks, tests, results, and defects to reveal meaningful coverage and gaps. | Build a traceability view showing which high-risk requirements have passed tests, failed tests, or no coverage. |
| [`sdet-defect-reporting-triage`](skills/sdet-defect-reporting-triage/) | Turns failure evidence into clear, reproducible defect reports and supports consistent triage. | Convert logs, screenshots, and failed steps into a defect report with expected behavior, actual behavior, impact, and proposed severity. |
| [`sdet-test-status-reporter`](skills/sdet-test-status-reporter/) | Converts test results, coverage, defects, risks, and blockers into decision-ready status or completion reports. | Prepare a release testing update that explains progress, major failures, remaining risks, blockers, and confidence. |
| [`sdet-test-data-designer`](skills/sdet-test-data-designer/) | Designs realistic, repeatable test data for normal, boundary, and invalid conditions. | Prepare linked customer and order fixtures with valid quantities and values just outside the allowed range. |
| [`sdet-test-environment-planner`](skills/sdet-test-environment-planner/) | Defines the systems, configurations, dependencies, and checks needed for a ready test environment. | Plan a checkout environment with a payment simulator and identify checks that still need the real provider. |
| [`sdet-test-execution-analyst`](skills/sdet-test-execution-analyst/) | Uses execution evidence to explain failed, intermittent, or suspiciously passing tests. | Investigate whether a CI failure comes from the application, setup, test code, or shared data. |
| [`sdet-test-estimation-planner`](skills/sdet-test-estimation-planner/) | Estimates testing effort and duration with explicit assumptions and uncertainty. | Forecast a regression cycle including preparation, investigation, retesting, and environment waits. |
| [`sdet-test-completion-evaluator`](skills/sdet-test-completion-evaluator/) | Checks agreed exit criteria against evidence and identifies remaining risks and handover work. | Assess whether blocked payment-recovery tests prevent a release's testing milestone from being complete. |
| [`sdet-test-process-improver`](skills/sdet-test-process-improver/) | Turns recurring testing problems and lessons into small, measurable improvement experiments. | Pilot decision-table reviews to reduce escaped defects in discount-rule combinations. |
| [`sdet-automation-feasibility-assessor`](skills/sdet-automation-feasibility-assessor/) | Assesses what is worth automating, what needs preparation, and how to evaluate tools with a small pilot. | Compare repeatable invoice checks with tasks that still require human judgment before investing in automation. |
| [`sdet-test-automation-engineer`](skills/sdet-test-automation-engineer/) | Builds and maintains automated tests using the project's existing framework, with meaningful assertions and reliable setup and cleanup. | Add API and UI checkout tests that verify order outcomes and isolate test data. |
| [`sdet-automation-framework-reviewer`](skills/sdet-automation-framework-reviewer/) | Reviews shared automation code and architecture for reliability, trustworthy results, and maintainability. | Find a shared assertion helper that hides failures or a fixture that mixes data between parallel tests. |
| [`sdet-ci-cd-test-integrator`](skills/sdet-ci-cd-test-integrator/) | Integrates test suites into CI/CD with suitable triggers, preserved failure evidence, and clear gate behavior. | Add required regression checks that retain reports without turning failed tests into a successful job. |

### Agile, Exploratory, and Technical Testing

| Skill | What it does | Example use case |
|---|---|---|
| [`sdet-agile-quality-coach`](skills/sdet-agile-quality-coach/) | Helps teams include quality checks throughout their everyday Agile work. | Introduce early refund-rule discussions to reduce late clarification. |
| [`sdet-user-story-testability-review`](skills/sdet-user-story-testability-review/) | Checks whether a user story is clear and small enough to test. | Clarify cancellation rules and split an oversized order story. |
| [`sdet-example-mapping-facilitator`](skills/sdet-example-mapping-facilitator/) | Turns a story into business rules, examples, and unanswered questions. | Agree how discounts apply at a price threshold. |
| [`sdet-exploratory-test-charter-designer`](skills/sdet-exploratory-test-charter-designer/) | Creates a focused mission for a tester to explore. | Investigate what happens to a cart when a session expires. |
| [`sdet-exploratory-session-analyzer`](skills/sdet-exploratory-session-analyzer/) | Summarizes what an exploratory session actually discovered. | Turn checkout notes into suspected defects and follow-up investigations. |
| [`sdet-test-smell-reviewer`](skills/sdet-test-smell-reviewer/) | Finds confusing or fragile patterns in manual test instructions. | Replace vague expected results and expose hidden setup dependencies. |
| [`sdet-regression-test-optimizer`](skills/sdet-regression-test-optimizer/) | Selects valuable regression checks for a change and available time. | Prioritize tax, refund, and invoice tests after a tax-rule change. |
| [`sdet-white-box-test-designer`](skills/sdet-white-box-test-designer/) | Designs tests to exercise specific decisions and paths in code. | Show which input pairs demonstrate each Boolean condition's effect. |
| [`sdet-api-test-designer`](skills/sdet-api-test-designer/) | Defines API scenarios, expected responses, and business-state checks. | Check duplicate order requests against the documented retry contract. |
| [`sdet-static-analysis-reviewer`](skills/sdet-static-analysis-reviewer/) | Reviews code-analysis warnings and separates evidence from suspicion. | Check whether a reported null access is reachable. |
| [`sdet-security-test-planner`](skills/sdet-security-test-planner/) | Plans safe, authorized checks for important security risks. | Plan checks that one tenant cannot read another tenant's invoices. |
| [`sdet-performance-test-planner`](skills/sdet-performance-test-planner/) | Plans realistic workloads and meaningful speed/capacity checks. | Define a promotion-load test with agreed targets and stop limits. |
| [`sdet-reliability-test-planner`](skills/sdet-reliability-test-planner/) | Plans checks for failure tolerance, backup restoration, and recovery. | Verify recovery from a worker restart without lost or duplicate orders. |
| [`sdet-compatibility-portability-test-planner`](skills/sdet-compatibility-portability-test-planner/) | Plans checks across supported platforms, integrations, and upgrades. | Assess a driver upgrade across supported database versions. |
| [`sdet-technical-review-facilitator`](skills/sdet-technical-review-facilitator/) | Organizes focused technical reviews with evidence and follow-up actions. | Review a design for stale permission-cache risks. |

## How the Skills Fit Together

```text
Requirements
    |
    v
Testability review
    |
    v
Risk analysis, test strategy, and estimation
    |
    v
Test design, data, environments, and test-case review
    |
    v
Automation feasibility, implementation, framework review, and CI/CD
    |
    v
Traceability, execution analysis, and defects
    |
    v
Completion assessment and reporting
    |
    v
Lessons and process improvement
```

This is an example flow, not a required sequence. Planning, reviews, traceability, and reporting can happen throughout delivery, and findings can lead back to earlier work.

The skills are independent. Install only the skill you need, or combine them across a testing workflow. The strategy skill covers the overall approach; data, environment, and estimation skills provide focused detail when needed. Execution analysis explains results, defect reporting documents issues, completion evaluation assesses exit criteria, and status reporting communicates the evidence.

For automation work, use feasibility assessment to decide what to automate, automation engineering to implement it, framework review to assess shared infrastructure, and CI/CD integration to run it in delivery workflows. The existing execution analyst investigates run failures; the test-case reviewer evaluates individual cases and their coverage. Tool evaluation and architecture are included in the automation skills rather than requiring separate packages.

For Agile work, use the coach for team practices, story review for refinement, and example mapping for business-rule discussions. A charter plans an exploratory session; session analysis uses its recorded evidence. Smell review focuses on manual-test maintainability, while regression optimization selects checks for a specific change.

For technical work, use API and white-box design for detailed coverage, static analysis for code warnings, and technical review for broader design or code discussions. Security, performance, reliability, and compatibility/portability skills create bounded plans; they do not authorize scans, load generation, fault injection, or migrations.

## Validation and Limitations

Structural checks cover skill format, naming, metadata, and local links. They do not prove that an AI agent will reliably choose or follow a skill.

Behavioral evaluation scenarios cover [core STLC and automation](evals/core-and-automation-skills.md) and [specialist skills](evals/specialist-skills.md), including missing evidence, coverage calculations, authorization limits, and skill selection. These are test cases, not a claim that the full collection has passed. Before relying on a skill for release decisions, evaluate it with representative project inputs and review its output with a qualified person. No cross-agent or production-readiness guarantee is made.

## Skill Structure

Each skill is self-contained:

```text
sdet-skill-name/
|-- SKILL.md                  Main agent instructions
|-- agents/
|   `-- openai.yaml           User-facing skill metadata
`-- references/
    `-- ...                   Detailed checks and output guidance
```

The main instructions are intentionally concise. Detailed review criteria, decision rules, and output formats are kept in focused reference files and loaded only when needed.

## Standards Basis

The skills are informed by testing concepts from the following ISTQB syllabi:

- Certified Tester Foundation Level v4.0.1
- Certified Tester Advanced Level Test Management v3.0
- Certified Tester Advanced Level Test Analyst v4.0
- Certified Tester Advanced Level Technical Test Analyst v4.0
- Certified Tester Advanced Level Test Automation Engineering v2.0
- Certified Tester Advanced Level Agile Tester v2.0

The repository uses original, plain-language guidance rather than copying the syllabi. ISTQB owns its syllabi and trademarks. This is an independent community project and is not affiliated with, accredited by, or endorsed by ISTQB.

Each supporting guide identifies its source syllabus and relevant sections; the original MVP guides also identify printed page numbers. Examples, templates, and agent safety conventions are repository guidance, not mandatory ISTQB rules. Describe the collection as **ISTQB syllabus-informed**, not ISTQB-certified or a guarantee of compliance with other standards mentioned in a syllabus. The source PDFs are not required to use an installed skill.

## Installation

The repository follows the open [Agent Skills](https://agentskills.io) format and can be installed with the [`skills`](https://skills.sh) CLI.

Install all skills:

```bash
npx skills add balaji16s/sdet-skills --all
```

Install one skill:

```bash
npx skills add balaji16s/sdet-skills --skill <skill-name>
```

List the available skills:

```bash
npx skills add balaji16s/sdet-skills --list
```

Target a specific supported agent:

```bash
npx skills add balaji16s/sdet-skills --agent claude-code
```

Depending on the agent, you may need to reload its skills after installation.

## Manual Installation

Copy the required folder from [`skills/`](skills/) into the skills directory used by your AI agent. Each folder includes its own `SKILL.md` and supporting guidance.

## Project Goals

- Cover practical quality-engineering activities across the STLC
- Keep instructions clear enough for new testers and useful enough for experienced engineers
- Produce evidence-based outputs instead of generic testing checklists
- Keep skills tool-neutral unless a task genuinely requires a specific tool
- Make assumptions, risks, uncertainty, and missing information visible
- Grow the collection without creating overlapping or overly broad skills

## Contributing

Contributions from testers, developers, quality engineers, and test leaders are welcome. Open an issue or pull request when you find unclear guidance, missing scenarios, or behavior that does not work well in practice.

Prefix every skill's folder and frontmatter name with `sdet-` (for example, `sdet-test-data-designer`). Use `SDET` at the start of its display name and keep invocation prompts consistent with the full skill name.

When adding or changing a skill, update the **Available Skills** tables, its metadata, and relevant evaluation scenarios so the public catalog remains current. Keep scope boundaries explicit and distinguish structural validation from observed agent behavior.

## License

This project's original skill content and documentation are licensed under the [MIT License](LICENSE). Referenced ISTQB syllabi and trademarks remain the property of their respective owners and are not relicensed by this project.

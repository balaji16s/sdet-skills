# sdet-skills

Reusable AI agent skills for quality engineers, QA engineers, SDETs, developers, and test leaders.

These skills help AI coding agents perform testing work with the structure and judgment of an experienced tester. The current collection covers core activities of the Software Testing Life Cycle (STLC), from reviewing requirements to reporting test status.

## Who This Is For

This repository is useful for:

- QA engineers who want consistent and practical testing outputs from AI agents
- SDETs building or maintaining test automation and quality-engineering workflows
- Developers who want earlier and clearer testing feedback
- Test leads who want to standardize testing practices across a team
- Learners who want examples of applying established testing principles to real work

## Available Skills

The repository currently contains eight MVP skills.

| Skill | What it does | Example use case |
|---|---|---|
| [`requirement-testability-review`](skills/requirement-testability-review/) | Finds unclear, incomplete, conflicting, or untestable requirements before detailed test design begins. | Review a user story and identify missing rules, vague acceptance criteria, and questions for the product owner. |
| [`risk-based-test-planner`](skills/risk-based-test-planner/) | Identifies the most likely and harmful risks so testing focuses on what matters most. | Prioritize payment failures and data-loss risks above low-impact visual issues for a release. |
| [`test-strategy-designer`](skills/test-strategy-designer/) | Creates a practical testing approach covering objectives, scope, risks, test types, environments, people, automation, and reporting. | Define how a team will test a new checkout service across component, API, integration, system, and acceptance levels. |
| [`test-technique-designer`](skills/test-technique-designer/) | Selects and applies suitable test techniques to derive effective and traceable tests. | Use equivalence partitions and boundary values to test an age field, or a decision table to test discount rules. |
| [`test-case-quality-reviewer`](skills/test-case-quality-reviewer/) | Reviews existing test cases for correctness, clarity, coverage, reliability, traceability, and maintainability. | Find weak expected results, duplicate cases, hidden dependencies, and missing negative coverage in a regression suite. |
| [`traceability-coverage-manager`](skills/traceability-coverage-manager/) | Connects requirements, risks, tests, results, and defects to reveal meaningful coverage and gaps. | Build a traceability view showing which high-risk requirements have passed tests, failed tests, or no coverage. |
| [`defect-reporting-triage`](skills/defect-reporting-triage/) | Turns failure evidence into clear, reproducible defect reports and supports consistent triage. | Convert logs, screenshots, and failed steps into a defect report with expected behavior, actual behavior, impact, and proposed severity. |
| [`test-status-reporter`](skills/test-status-reporter/) | Converts test results, coverage, defects, risks, and blockers into decision-ready status or completion reports. | Prepare a release testing update that explains progress, major failures, remaining risks, blockers, and confidence. |

## How the Skills Fit Together

```text
Requirements
    |
    v
Testability review
    |
    v
Risk analysis and test strategy
    |
    v
Test design and test-case review
    |
    v
Traceability, execution evidence, and defects
    |
    v
Test status and completion reporting
```

The skills are independent. Install only the skill you need, or combine them across a testing workflow.

## Skill Structure

Each skill is self-contained:

```text
skill-name/
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

When adding a skill, update the **Available Skills** table in this README so the public catalog remains current.

## License

The project is intended to be free to use, adapt, and build upon for quality-engineering workflows. Add a repository license file before the first public release so these permissions are legally explicit.

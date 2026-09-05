# sdet-skills

A set of reusable AI agent skills built for QA engineers, SDETs, and test automation folks. They teach AI coding agents (Claude, Cursor, and other agent-compatible tools) how to handle everyday QA work the way an experienced tester would — not just generic code output.

---

## Who This Is For

If you're using AI agents as part of your QA or automation work, you've probably noticed you end up re-explaining the same conventions every time — how your team writes tests, reports bugs, or reviews code. Install a skill once, and your agent just knows.

Useful if you're:
- A QA engineer who wants consistent, well-structured output from your agent
- An SDET building or maintaining a test automation framework
- A lead trying to standardize how automation, reviews, and bug reports get done across a team

---

## What's Included

Right now, this covers four areas of QA work:

- **Automation test creation** — helps an agent write structured, maintainable tests instead of one-off scripts
- **Test review** — flags common issues in existing tests: weak assertions, poor structure, missing edge cases
- **Bug/defect reporting** — writes clear, actionable Jira bug reports with steps to reproduce, expected vs. actual behavior, and severity
- **Requirements analysis** — breaks requirements or user stories into testable conditions and surfaces ambiguities before test creation starts

More skills will get added as this grows.

---

## Grounded in Real Testing Standards

These aren't just personal opinions written down. They're built on widely recognized testing principles, including guidance from **ISTQB (International Software Testing Qualifications Board)** material — so the output your agent produces actually aligns with how testing is taught and practiced, not just whatever pattern seemed convenient.

If you're ISTQB-certified or working toward it, the terminology here should feel familiar.

---

## How to Use These Skills

Built on the open [Agent Skills](https://agentskills.io) format — the same standard [skills.sh](https://skills.sh) uses — so you can install these straight into your project with the `skills` CLI.

**Install everything:**
```bash
npx skills add balaji16s/sdet-skills --all
```

**Install one specific skill:**
```bash
npx skills add balaji16s/sdet-skills --skill <skill-name>
```

**Just browse what's available first:**
```bash
npx skills add balaji16s/sdet-skills --list
```

**Target a specific agent** (if you use more than one):
```bash
npx skills add balaji16s/sdet-skills --agent claude-code
```

Depending on your agent, you may need to reload it afterward (e.g., `/skills reload`) before the skill kicks in. Once it's loaded, just work normally — the agent applies the right skill automatically when a task matches it.

---

## Prefer Not to Use the CLI?

Just copy the relevant skill folder straight into your project's skills directory. Each one is self-contained with its own `SKILL.md`, so a manual copy works exactly the same as installing through the CLI.

---

## Contributing

Got QA or automation experience and think something here could be sharper, or missing entirely? Open an issue or send a pull request — always happy to improve these based on real-world use.

---

## License

Free to use, adapt, and build on for your own QA and testing workflows.
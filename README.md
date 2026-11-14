# Dashboard Development Skill

Reusable, evidence-based workflow for designing, building, reviewing and iterating dashboards. **This repository is for generalizable guidance**, not for the code or detailed engineering logs of one particular dashboard.

## Repository structure

- [`SKILL.md`](SKILL.md) — concise instructions used by development assistants / future Skill packaging.
- [`references/PLAYBOOK.md`](references/PLAYBOOK.md) — detailed end-to-end architecture, UX, storage, testing and release methodology.
- [`references/PATTERNS.md`](references/PATTERNS.md) — proven, cross-project patterns and when not to apply them.
- [`templates/PROJECT_ITERATION_TEMPLATE.md`](templates/PROJECT_ITERATION_TEMPLATE.md) — generic per-project engineering decision/log format.
- [`docs/updates/TEMPLATE.md`](docs/updates/TEMPLATE.md) — template for Skill-specific updates linked to source project commits.
- [`docs/updates/`](docs/updates/) — append-only history of Skill changes and supporting evidence.
- [`AGENTS.md`](AGENTS.md) — contribution and promotion gate.

## Two-repository rule

1. Work and test in the **individual dashboard's repository**.
2. Commit that project's own code + scoped iteration log.
3. Decide `promote / no change / pending` based on generality, evidence and novelty.
4. **Only when promoted**, update this Skill's guidance and dated update note, with links to the originating project's evidence.

A project iteration does **not** automatically require a Skill update. Do not copy all project-specific MD or data into this repository. The first source case is [Game Dashboard](https://github.com/RoLance-G/game-dashboard), whose actual case study and logs remain there.

## Status

These are **initial Skill source files**, not an already installed ChatGPT Skill. The source repository is [RoLance-G/dashboard-development-skill](https://github.com/RoLance-G/dashboard-development-skill). These are version-controlled Skill source files, not an automatically installed ChatGPT Skill.

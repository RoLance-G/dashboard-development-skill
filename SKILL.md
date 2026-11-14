---
name: dashboard-development-workflow
description: Build, refine, audit and safely deploy dashboards; preserve project-specific iteration records first, then selectively promote evidence-backed reusable lessons into this Skill. Use for dashboard implementation, UI reviews, local-first storage, archive scalability, backup/recovery, and version iteration work.
---

# Dashboard Development Workflow

Apply this playbook when creating or iterating any dashboard. Do not assume the current dashboard uses the same stack or constraints as Game Dashboard.

## Start by inspecting evidence

1. Open the current project's actual code, docs, data shape, and recent commits. Confirm deployment, ownership and expected data growth.
2. Identify non-negotiables: user data, compatibility/migration paths, visual identity, performance, backups and privacy.
3. Read [Playbook](references/PLAYBOOK.md) for architecture, UI, scaling, testing, release and backup guidance.
4. Review [Patterns](references/PATTERNS.md) for reusable trade-offs. Cite observed project outcomes when promoting any new rule.

## Required iteration order (two repositories)

**Phase A — project first**

1. Define scoped changes and rollback. Implement and self-audit; test all affected flows and disclose untested paths.
2. Update **the project's own** dated iteration Markdown and architecture notes as needed, with user requirements, decisions, code diffs, test evidence, limits and deployment state.
3. Commit/verify the project changes and log **before** changing general Skill guidance.
4. Record the **Skill promotion decision**: `promote`, `no change`, or `pending evidence/access`. A new feature alone is not sufficient evidence of a reusable lesson.

**Phase B — promote only if justified**

5. Compare the candidate lesson against existing guidance. Only promote a nonduplicative principle that plausibly generalizes across dashboards.
6. Update the appropriate `SKILL.md` or `references/` section, with accurate constraints and linked project evidence; append `docs/updates/YYYY-MM-DD-<slug>.md`.
7. Commit and verify the Skill repository separately. If inaccessible, record `pending` in the project log rather than claiming an update.

## Quality gates

- Keep source code, user data, and cloud credentials separate. Do not commit real backup JSONs, tokens or secrets.
- Never claim real browser/cloud integration tests passed when only mocks, syntax checks or static code inspection were performed.
- Preserve migration and export/restore contracts unless verified migration is explicitly in scope.
- Verify both project and Skill GitHub writes independently. Publishing a Git commit is not proof that a deployed site works.
- Prefer minimal, observable code; avoid redundant CSS, repeated data scans, over-large DOMs and unneeded animations.
- Historical decisions are append-only records; add corrections rather than quietly rewriting prior accounts.

## Output contract

Report: app commit and project iteration-log link; changes/tests/gaps; promotion decision with rationale; optional distinct Skill commit + update-log link. Keep project-specific information inside its own repository.

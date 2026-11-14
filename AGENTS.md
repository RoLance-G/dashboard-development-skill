# Skill repository working agreement

This repository contains **portable dashboard-development instructions** only. Source-specific facts, complete implementation logs and data stay in their originating dashboard repositories.

## Before changing the Skill

1. Identify the triggering dashboard project, its **committed** iteration log, relevant code commit and what was actually tested.
2. Inspect the present `SKILL.md`, relevant `references/` files and recent `docs/updates/` notes.
3. Assess whether the candidate lesson is **(a)** evidenced, **(b)** reusable across projects, and **(c)** not already covered.
4. If any test lacks evidence, do not promote the assertion as a verified best practice; record pending investigation in the originating project instead.

## Change policy

- The project repository **must be updated first**. Never modify the source project's code or docs through a Skill-only commit.
- Keep changes small and traceable. Update the appropriate Skill/reference document; add a dated Skill update at `docs/updates/YYYY-MM-DD-<slug>.md` using the template.
- The update note must reference source project, iteration log, project commit, changed guidance and validation scope.
- Do not duplicate project-specific case studies wholesale; link to their source of truth.
- Treat `SKILL.md` as minimal stable entrypoint; detailed techniques live under `references/`.
- Keep material and paths safe: no API keys, OAuth tokens, private account data, or personal backups.
- Preserve existing useful behavior and note any breaking changes in Skill guidance; verify links and syntax before committing.
- Re-fetch the remote Skill commit after write; a Git push is not proof of a production application test.

## Release checklist

- [ ] Evidence linked to already-committed source project log and commit
- [ ] Reusable/nonduplicative promotion justified
- [ ] `SKILL.md` and/or `references/` updated
- [ ] `docs/updates/YYYY-MM-DD-<slug>.md` appended
- [ ] Links and wording validated; new docs checked for secrets
- [ ] Skill GitHub commit re-fetched; user told what remains unverified

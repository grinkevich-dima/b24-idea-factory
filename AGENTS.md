# AGENTS.md

## Cursor Cloud specific instructions

This is a **documentation-only** repository (no source code, no dependencies, no build, no tests).

### What is this repo?

- A knowledge base and Cursor AI skill for generating Bitrix24 Marketplace app idea packages.
- The main "application" is the skill at `.cursor/skills/b24-idea-factory/SKILL.md`.
- All output artifacts go into `docs/idea-briefs/`.

### Key facts for Cloud Agents

- **No package manager** — no `package.json`, `requirements.txt`, or similar.
- **No services to start** — nothing to run.
- **No tests/lint/build** — the repo is pure Markdown.
- **Language of artifacts** — all documentation is in Russian.
- **Skill usage** — read `SKILL.md` + `docs/idea-briefs/IDEA_METHOD.md` when generating/validating ideas.
- **Idea pipeline (G1–G5)** — generate → self-filter → **heavy** validate (Marketplace + native B24) → propose in chat → write `PROPOSED`/`BACKLOG` **only after** user `ок N` / `в беклог N`. Full 4-file package after `в беклог N`.
- **No hourly spray** — timer stays off unless the user explicitly re-enables it. Default 1–2 candidates per request.
- **File naming convention** — idea packages use `NN_<slug>.md` with `__competitors`, `__mvp_release_market`, `__screens_security_faq` suffixes. Always update `INDEX.md` when adding new packages.

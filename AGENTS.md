# Scripture Discovery Journey — agent instructions

## Source of truth for skills

All agent skills live in **https://github.com/getrdone/agent-skills**.

Before planning, writing, designing, building, testing, or reviewing:

1. Open agent-skills **`CATALOG.md`** (do not load every skill).
2. Match the task; for this project that is almost always **`curiosity-driven-scripture-journey`**.
3. Load `skills/curiosity-driven-scripture-journey/SKILL.md` from agent-skills and only the references it names.
4. For private source inventory/registration, use agent-skills `processing/source-vault/`.
5. Before source-dependent work **in this repo**, read `sources/registry.yaml`. Use only records with applicable `approval.status: approved`. `sources/intake/` is never authoritative.
6. Preserve locked decisions in the project’s `project-brief.md` when present.
7. Do not begin new production HTML until project status is `approved-for-build`.
8. Run quality gates from the skill’s `references/quality-gates.md`.
9. Never infer approval from silence.
10. Do **not** edit the master skill inside this repo — open a PR against **agent-skills**.

Local path `skills/curiosity-driven-scripture-journey/` is a **pointer only**.

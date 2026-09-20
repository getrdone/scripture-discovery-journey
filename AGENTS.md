# Scripture Discovery Journey — agent instructions

<!-- Agent: Codex | Model: GPT-5 | Thinking: not exposed | Date: 2026-08-21 -->

## Sources of truth

- Canonical agent skills: **https://github.com/getrdone/agent-skills**
- Canonical Bible-study sources: **https://github.com/getrdone/bible-study-source-materials**
- Consumer source snapshot: root **`source-library.lock.yaml`**

Before planning, writing, designing, building, testing, or reviewing:

1. Open agent-skills **`CATALOG.md`**; do not load every skill.
2. Match the task. For this project that is almost always **`curiosity-driven-scripture-journey`**.
3. Load `skills/curiosity-driven-scripture-journey/SKILL.md` from agent-skills and only the references it names.
4. Before source-dependent work, read this repository's `source-library.lock.yaml`, then read `registry.yaml` and applicable policy from the exact pinned source-library commit.
5. Use only source records with `approval.status: approved` and a scope that covers the task. Intake and under-review records are never authoritative.
6. Use the pinned SQLite database for routing and discovery, then verify consequential wording and locators against canonical records and permitted source text.
7. Perform source intake, approval, extraction, indexing, and database rebuilding in `getrdone/bible-study-source-materials`—never by creating a competing source library here.
8. Preserve supplied sources. Add corroboration or stronger evidence beside them; do not silently replace them.
9. Record material study claims in a source-alignment manifest. Unresolved contradictions among applicable approved sources make the affected claim `BLOCKED`.
10. Preserve locked project decisions in `project-brief.md` when present.
11. Do not begin new production HTML until project status is `approved-for-build`.
12. Run the applicable quality gates from the skill's `references/quality-gates.md`.
13. Never infer approval from silence.
14. Do **not** edit the master skill inside this repository; open a PR against **agent-skills**.

Load the installed managed skill or the canonical library directly; there is no project-local skill alias. `source-library.lock.yaml` is also a pointer: it does not make this repository a source authority.


## Authoritative skills and work placement

Use `G:/__ai-projects/_agent-skills/CATALOG.md` to discover current skills; resolve releases through their CURRENT/STABLE selectors. That library contains all managed instructions and resources. Do not use old aliases or archived skills as fallback instructions. Put drafts, temporary plans, experiments and diagnostic captures in project `_wip/<task>/`, not root or planning/. Put reusable project utilities in `_tools/` and consult the master `G:/__ai-projects/_agent-skills/_tools/TOOLS.md` first. Preserve accepted plans, source, tests, assets, deliverables and project-specific locks. Complete authorized work in cohesive verifiable chunks without elapsed-time quotas or automatic kills.

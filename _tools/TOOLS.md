# Project tools

Master catalog: `G:/__ai-projects/_agent-skills/_tools/TOOLS.md`. Search it before creating a utility. Established source/build commands retain their current homes; new reusable utilities belong in `_tools/`.

| Purpose | Invocation from project root | Dependencies | Reuse |
|---|---|---|---|
| source vault inventory | `python scripts/source_vault_inventory.py` | Python 3 | Existing command and implementation; inspect arguments before invoking |

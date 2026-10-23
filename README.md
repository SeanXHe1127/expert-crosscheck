# expert-crosscheck

An agent skill that forces an expert-perspective crosscheck **before** executing a user's plan.

When the user states a goal together with their own approach, the skill answers four questions first:

1. **What top experts in the field would do that the user didn't ask for** — surfacing unknown unknowns.
2. **Which primary/raw sources experts would start from** — raw data, original papers, source code, filings — instead of predigested secondhand material.
3. **The specific tools and methods experts would use** — named software, databases, frameworks, and procedures, not vague advice.
4. **Besides the AI and the user, what could prove the result is right** — recomputable metrics, independent data sources, benchmarks, executable tests, falsifiable predictions.

It then delivers a verdict (execute as-is / execute after additions / directional problem) and **waits for user confirmation before doing any work**.

## Install

Copy `expert-crosscheck/` into your agent's skills directory, e.g.:

- Kimi / Kimi Work: managed skills root (or import via the plugin-builder)
- Claude Code / Kimi Code CLI: `~/.claude/skills/` or `~/.config/agents/skills/`
- Or with the skills CLI: `npx skills add <your-github-user>/expert-crosscheck`

## Trigger

Activates when the user proposes a goal plus their own plan, or on phrases like "crosscheck my plan", "is my approach sound", "what would an expert do".

## License

MIT

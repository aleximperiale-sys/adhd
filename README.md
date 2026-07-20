# adhd

Claude Code skills and tools that help developers with ADHD by enforcing easily-readable, low-cognitive-load context — short chunks, clear structure, visible progress — instead of long unstructured explanations or open-ended tasks.

## Structure

```
adhd/
├── readable-context/   # enforces scannable output and chunked task breakdowns
└── ...
```

Each skill folder contains:
- `SKILL.md` (required) — instructions and YAML front matter
- `references/` (optional) — extra reference documentation, examples

## Install / usage

| Tool | Usage |
|---|---|
| Claude Code, Codex, Cursor, OpenCode, [more](https://agentskills.io/) | `npx skills add aleximperiale-sys/adhd` |
| Manual | Clone this repo and copy the skill folder(s) you want into your project's `.claude/skills/` (or equivalent) directory |

## Skills

- **[readable-context](readable-context/SKILL.md)** — enforces short, scannable responses (headers over walls of text, one idea per paragraph, explicit next actions) and small checkpointed task breakdowns instead of open-ended multi-step work.

## License

MIT — see [LICENSE](LICENSE). All content in this repo is original.

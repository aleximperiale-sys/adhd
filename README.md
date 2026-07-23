# adhd

Claude Code skills and tools that help developers with ADHD by enforcing easily-readable, low-cognitive-load context, short chunks, clear structure, visible progress, instead of long unstructured explanations or open-ended tasks.

## Structure

```
adhd/
├── readable-context/    # enforces scannable output and chunked task breakdowns
├── session-resume/      # reconstructs "where was I" at the start of a session
├── scope-guard/         # catches and names scope drift/rabbit holes mid-task
├── decision-log/        # captures side-decisions and tangents the moment they happen
├── done-enough-check/   # flags when the bar is cleared and asks before further polishing
├── single-thread-focus/ # keeps one active thread and parks the rest explicitly
└── ...
```

Each skill folder contains:
- `SKILL.md` (required), instructions and YAML front matter
- `references/` (optional), extra reference documentation, examples

## Install / usage

| Tool | Usage |
|---|---|
| Claude Code, Codex, Cursor, OpenCode, [more](https://agentskills.io/) | `npx skills add aleximperiale-sys/adhd` |
| Manual | Clone this repo and copy the skill folder(s) you want into your project's `.claude/skills/` (or equivalent) directory |

## Skills

- **[readable-context](readable-context/SKILL.md)**, enforces short, scannable responses (headers over walls of text, one idea per paragraph, explicit next actions) and small checkpointed task breakdowns instead of open-ended multi-step work.
- **[session-resume](session-resume/SKILL.md)**, reconstructs "where was I" from git status, recent commits, and open todos at the start of a session or after an interruption.
- **[scope-guard](scope-guard/SKILL.md)**, detects when work has drifted from the original task (a rabbit hole, an unrelated refactor) and names it explicitly before continuing.
- **[decision-log](decision-log/SKILL.md)**, captures small side-decisions, tangents, and deferred TODOs into a running log the moment they come up, instead of relying on memory.
- **[done-enough-check](done-enough-check/SKILL.md)**, flags the moment a task meets its actual bar and asks explicitly whether to stop or keep polishing.
- **[single-thread-focus](single-thread-focus/SKILL.md)**, forces one explicit active thread when work has fragmented across multiple open tasks, and parks the rest visibly.

## License

MIT, see [LICENSE](LICENSE). All content in this repo is original.

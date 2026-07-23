---
name: decision-log
description: Immediately captures small side-decisions, tangential ideas, and deferred TODOs into a running log the moment they come up, instead of relying on working memory to hold them until later. TRIGGER whenever a decision is made in passing, a tangent/idea surfaces that isn't the current task, or the user says "remind me to", "note that", "don't let me forget". DO NOT TRIGGER for the main decision being actively worked on right now, this is for things that would otherwise be dropped.
triggers:
  - "note that"
  - "remind me to"
  - "don't let me forget"
  - "log this"
  - "park this for later"
---

# decision-log

Working memory drops side-thoughts the moment attention moves elsewhere. This skill's job is to catch anything worth keeping the instant it appears, not to wait for a natural pause that may never come.

## What to log

- **Small decisions made in passing**: a naming choice, a "let's do it this way for now," a tradeoff accepted without full discussion.
- **Deferred work**: anything explicitly punted ("not now, but later").
- **Tangents**: an idea or concern that surfaced but isn't the current task.
- **Open questions**: anything left unresolved that needs an answer before it matters.

## How to log it

Append a single line per item, as it happens, in this shape:

```
- [decision|todo|tangent|question] <one-line description>, <why it matters, if not obvious>
```

Log it in whatever the project already uses for this (an existing TODO file, a todo tool, a tracked markdown file), don't invent a new location if one exists. If none exists, propose creating a single `DECISIONS.md` or equivalent rather than scattering notes across comments.

## Rules

- **Log at the moment it happens**, not at the end of the session from memory, end-of-session recall is exactly the failure mode this exists to avoid.
- **One line, no essay.** The log is a pointer to revisit, not the full resolution.
- **Surface the log periodically**, not just on request, mention unresolved items when they become relevant again, and review the list before ending a session.
- **Close items out.** When a logged item gets resolved, remove or check it off rather than leaving a growing pile of stale notes.

## Anti-patterns to avoid

- Waiting until "a good stopping point" to write anything down.
- Logging everything with equal weight so the list becomes noise instead of signal.
- Letting the log grow indefinitely without ever revisiting or pruning it.

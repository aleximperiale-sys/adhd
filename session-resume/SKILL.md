---
name: session-resume
description: At the start of a session (or after any gap/interruption), reconstructs "where was I" from git status, recent commits, open todos, and recently touched files, and presents it as a compact resume-context summary instead of leaving the developer to reconstruct it from memory. TRIGGER at the start of a new session, after the user returns from a break or context switch, or when the user says things like "where was I", "what was I doing", "remind me what's going on here". DO NOT TRIGGER mid-task when context is already active and nothing was interrupted.
triggers:
  - "where was i"
  - "what was i doing"
  - "resume"
  - "catch me up"
  - "remind me what's going on"
---

# session-resume

Rebuild working context automatically instead of relying on the developer to hold it across a gap. Time away from a task (overnight, a meeting, a context switch) is when ADHD working memory loses the thread fastest — this skill treats that as the default case, not an edge case.

## What to reconstruct

- **Uncommitted changes**: `git status`/`git diff` — what's mid-edit right now.
- **Recent history**: last few commits on the current branch — what actually landed vs. what's still in flight.
- **Open todos**: any in-progress task list, whether from a todo tool or a plan/checklist left in the conversation.
- **Last known intent**: the most recent stated goal, not just the most recent file touched — a file can be open because it was a detour, not the actual objective.

## Output shape

Keep it to one short block, in this order:
1. **Goal** — the one-line objective as last stated.
2. **State** — what's done, in one line ("3 of 5 steps done").
3. **In-flight** — uncommitted changes or an unfinished edit, named specifically.
4. **Next action** — the single next concrete step, not a menu of options.

Skip any section that's empty rather than padding it out. If the reconstructed goal conflicts with what the files suggest (e.g. an open todo says one thing, the diff suggests another), surface the mismatch explicitly instead of picking one silently.

## Anti-patterns to avoid

- Re-deriving context silently and jumping straight into work without confirming the reconstructed goal is right.
- Dumping the full git log or full diff instead of a summary.
- Presenting multiple equally-weighted "next steps" instead of one clear one.

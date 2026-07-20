---
name: scope-guard
description: Detects when work has drifted from the originally stated task (a rabbit hole, an unrelated refactor, an interesting-but-unasked-for detour) and explicitly names the drift before continuing, rather than silently absorbing it into a much bigger change. TRIGGER whenever the current edit/investigation would touch files or concerns outside the original request, whenever a "quick fix" is expanding into a refactor, or whenever more than one unrelated problem is being worked at once. DO NOT TRIGGER when the expanded scope was explicitly requested by the user.
triggers:
  - "scope creep"
  - "getting distracted"
  - "rabbit hole"
  - "am i off track"
  - "stay focused"
---

# scope-guard

Rabbit holes are easy to fall into and hard to notice from inside — this skill's job is to be the outside check that notices for you.

## Detect drift

Treat any of these as a scope-drift signal:
- Editing a file that isn't required to satisfy the original request.
- A "quick fix" that has grown to touch more than 2-3 files.
- Discovering an unrelated bug/improvement mid-task and starting to fix it before finishing the current one.
- A change in *why* the work is being done (the justification shifted, not just the approach).

## What to do when drift is detected

1. **Name it plainly**: state what the original task was and what's now being touched instead, in one line each.
2. **Don't auto-decide.** Ask explicitly: finish the original task first, or consciously switch to the new one? Both are valid — the point is making it a decision instead of a drift.
3. **Park it, don't drop it.** If the detour is worth doing later, log it (pair with `decision-log`) rather than either abandoning the thought or chasing it immediately.
4. **Resume at the exact point of drift**, not from scratch — restate the last completed step of the original task so nothing already done gets redone or re-explained.

## Anti-patterns to avoid

- Silently expanding a "fix this bug" into "fix this bug and also clean up this file."
- Chasing an interesting tangent to completion before circling back, without ever flagging that a detour happened.
- Treating scope drift as a failure to prevent rather than a normal thing to catch and name.

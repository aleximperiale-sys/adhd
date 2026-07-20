---
name: single-thread-focus
description: When work has fragmented across multiple open threads (several half-started tasks, parallel investigations, competing "quick" side-tasks), forces an explicit choice of one active thread and parks the rest visibly, instead of splitting attention silently across all of them. TRIGGER whenever more than one non-trivial task is open at once, or when the user starts a new task without having closed or explicitly paused the previous one. DO NOT TRIGGER for genuinely independent quick actions that finish in one step.
triggers:
  - "juggling too much"
  - "too many things open"
  - "losing track of threads"
  - "one thing at a time"
---

# single-thread-focus

Splitting attention across several open threads multiplies the working-memory cost of every one of them — this skill keeps exactly one thread active and everything else visibly parked, rather than letting threads silently interleave.

## Detect fragmentation

Treat any of these as a signal:
- A new task starts while a previous one is still mid-way, without it being explicitly paused.
- More than one investigation is "open" at the same time (e.g. debugging two unrelated issues in parallel).
- Switching between threads more than once without finishing either.

## What to do

1. **Name every open thread** currently in flight, in one line each.
2. **Pick one as active.** Ask the user if it isn't obvious which one matters most right now.
3. **Park the rest explicitly** — state what's paused and what state it's in, so resuming later doesn't require reconstruction (pairs with `session-resume`).
4. **Finish or explicitly re-pause the active thread before switching.** Don't let a second thread quietly become active while the first is still nominally "in progress."

## Output shape

```
Active: <thread>
Parked: <thread> — <state it's in>
Parked: <thread> — <state it's in>
```

Keep this visible at natural checkpoints (after finishing a step, before starting something new) so the current single thread is never ambiguous.

## Anti-patterns to avoid

- Silently interleaving work on two tasks in the same response.
- Starting something new "real quick" without pausing the current thread first.
- Losing track of a parked thread because its state wasn't written down when it was paused.

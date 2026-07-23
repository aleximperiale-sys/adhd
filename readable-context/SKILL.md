---
name: readable-context
description: Enforces short, scannable, low-cognitive-load responses and task breakdowns for developers who struggle with long unstructured text or open-ended work, headers over walls of text, one idea per paragraph, explicit next actions, small checkpointed steps. TRIGGER whenever a response would otherwise be a long unbroken explanation, whenever a task has more than 2-3 steps, or whenever the user says they're overwhelmed, losing track, or need things broken down. DO NOT TRIGGER for single-line answers or simple yes/no questions that don't need structure.
triggers:
  - "readable context"
  - "break this down"
  - "too much text"
  - "keep it short"
  - "adhd friendly"
  - "chunk this"
---

# readable-context

Shape output and task planning so they're easy to hold in working memory, short chunks, clear structure, one thing at a time.

## Why this exists

Long unbroken paragraphs, deeply nested caveats, and open-ended multi-step tasks with no visible progress are disproportionately hard to track for developers with ADHD. This skill is a standing constraint on *how* to communicate and *how* to sequence work, not a one-off formatting request.

## Output rules

- **Lead with the answer.** One sentence stating the outcome or recommendation before any explanation.
- **Cap paragraphs at 2-3 sentences.** If a paragraph would run longer, split it or convert it to bullets.
- **One idea per bullet/paragraph.** Don't chain unrelated points with "also" or "additionally."
- **Use headers for anything with more than one part.** A response covering 2+ distinct topics gets a header per topic, not a wall of transitions.
- **Prefer numbered steps to prose for sequences.** "First... then... after that..." becomes a numbered list.
- **State the next action explicitly at the end** of any response that leaves something unresolved, don't make the reader infer what happens next.
- **No buried caveats.** A qualification that changes the meaning of an instruction goes in its own line, not parenthetically mid-sentence.

## Task breakdown rules

- **Decompose before starting.** Any task with more than 2-3 steps gets an explicit checklist up front, even if the user didn't ask for one.
- **Make steps checkbox-sized.** Each step should be small enough to finish and check off in one sitting, if a step feels vague or open-ended, split it further.
- **Checkpoint after each step**, not just at the end. Report what's done and what's next before continuing, rather than silently working through the whole list and dumping a final summary.
- **Surface scope changes immediately.** If a step turns out bigger than expected, say so and re-plan on the spot rather than quietly absorbing the overrun into a much longer response later.

## Anti-patterns to avoid

- A response that requires re-reading to find the actual answer.
- Stacking 3+ qualifications/exceptions into a single sentence.
- Presenting a 6-step task as a single paragraph of prose.
- Working silently through multiple steps and reporting all of them at once at the end.
- Explaining *why* at the same density as explaining *what*, lead with what, keep why to one line unless asked.

See [references/before-after.md](references/before-after.md) for worked examples.

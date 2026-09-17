# Continuity and progress checkpoints

The traveler should never have to reread a long conversation to recover the plan. Preserve progress during research and after every meaningful choice.

## Durable checkpoint

Keep one authoritative trip state synchronized with the HTML artifact. Store a compact machine-readable snapshot inside the self-contained HTML when practical, for example an `application/json` script element, while rendering the same facts in the overview.

Checkpoint after:

- The traveler answers a preference or selects an option
- A trip direction or day theme is accepted
- A candidate price or booking term materially changes a decision
- A named hotel, activity, meal, or transport is selected or rejected
- A reservation is confirmed, cancelled, or changes
- A day, map route, budget, or safety gate is updated

During intake, checkpoint answers with `intake_status: collecting`. Do not change it to `generation_started` until the traveler explicitly passes the completion gate.

The snapshot should contain confirmed facts, current assumptions, decisions, rejected options with brief reasons, researched candidates, source timestamps, open questions, next action, and the last completed planning stage. Do not store passwords, payment data, authentication codes, or unnecessary personal data.

## Visible progress

Keep the HTML overview current with:

- Last completed step
- Current research or planning step
- Next user decision
- Completed, selected, booked, pending, and blocked counts
- Recent changes
- Sources still being checked

During lengthy work, provide concise milestone updates so the traveler can see that work is progressing. Do not flood the conversation with raw browsing steps.

## Avoid stalls

Do not let one slow, logged-out, broken, or unavailable marketplace hold the whole plan. Preserve results already collected, mark the source attempt and limitation, then use another suitable platform or the direct provider. Stop repeating equivalent failed attempts.

If a login, CAPTCHA, missing date, or user-only choice is truly required, finish all independent research first. Ask only for the smallest action needed and preserve a clear next step in the trip state.

Before opening a blocking choice popup, save the pending question and current stage. Do not perform background work while the popup waits. If the popup is dismissed without an answer, keep that question pending for the next interaction.

Do not wait for perfect information before showing useful progress. Update Version 0.1 and its pending fields as reliable facts arrive.

## Resume behavior

After interruption or in a new task with access to the artifact or state:

1. Read the saved state before asking questions.
2. Give a compact recap of confirmed trip frame, completed work, and the single next decision.
3. Continue from the checkpoint without asking the traveler to repeat known answers.
4. Surface stale prices or facts that require rechecking.

Keep the recap short enough to scan. Put detailed history in the artifact, not in the resumption message.

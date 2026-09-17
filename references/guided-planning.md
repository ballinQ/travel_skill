# Guided planning and early drafts

Reduce user typing without turning the conversation into a long questionnaire. Ask only questions whose answers change the next planning decision.

## Choice design

- Use the interface's interactive question control whenever it is available so the traveler can answer by clicking.
- Do not present plain numbered or bulleted choices when clickable controls are available.
- Prefer one to three questions per round.
- Offer two to four distinct choices; combine overlapping choices.
- Put the likely or balanced choice first when a recommendation is justified.
- Allow combinations when preferences are not mutually exclusive.
- Always preserve a custom-answer path. If the interface automatically adds an `Other` text field, do not add a duplicate option. Otherwise make `Other — type your own` the final option.
- Include a short consequence in each label or description, such as `Fast pace — more highlights, less downtime`.
- Reuse known answers and accessible conversation context. Do not ask the user to repeat facts.
- Ask free-form questions only when a meaningful option cannot be anticipated.

If interactive controls are unavailable, use a compact text fallback and make the selectable labels easy to copy or answer by name. Do not delay the trip plan solely because the interface cannot render buttons.

Useful early choices cover destination focus, dates or season, duration, origin, party, pace, anchor experiences, food profile, photo/video profile, comfort needs, and spend-versus-save priorities. Do not ask all of them when several can be inferred.

## Earliest useful draft

Generate Version 0.1 when these are clear enough:

- Destination or workable region
- Approximate duration and timing
- Starting point and party
- Preferred pace
- One or more primary trip goals
- Hard constraints
- Spend priorities, even if the total budget is unknown

Version 0.1 should make the trip visible. Include:

- A one-sentence trip concept
- Geographic trip arc and preliminary overview map
- Day-by-day shells with one theme and anchor activity per day
- Likely lodging zones and major transport assumptions
- Approximate effort and spend shape
- Known risks or seasonal constraints
- Clearly marked open slots and decisions

An incomplete day is valid. Label gaps such as `afternoon open`, `meal not selected`, or `weather fallback pending` rather than filling them with weak recommendations.

If artifact creation is available, create the first HTML plan at this stage. The overview, map, and daily tabs may contain explicit placeholders. Keep one canonical artifact and update it continuously.

## Progressive day planning

After Version 0.1, guide the user through the highest-impact unresolved decision. Often this means Day 1 first, but resolve bookings or schedule dependencies earlier when they constrain several days.

For each day:

1. Confirm the day's purpose and acceptable effort.
2. Offer a few compatible activity clusters, already grouped geographically.
3. Ask about food and photo priorities relevant to that area.
4. Fill the timeline, transit, reservations, budget, filming, and fallback.
5. Update the overview and map before advancing.

Show the revised day immediately after the choice. Do not hold all updates until the final day.

## Avoid questionnaire fatigue

Use sensible defaults for reversible details and label them. Pause questioning when the user can benefit from seeing a draft. Alternate between a small choice and a visible improvement to the plan.

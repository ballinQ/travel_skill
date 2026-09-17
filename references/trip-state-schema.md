# Canonical trip state

Maintain these concepts in the artifact or supporting structured data. Omit irrelevant fields rather than showing empty scaffolding.

## Core

- Traveler profile: origin, party, pace, interests, comfort, mobility/health constraints, dietary needs, food preference mix, photo/check-in profile, filming needs, preferred sources, queue tolerance, and reservation tolerance.
- Trip frame: destination, timezone, dates, duration, budget, currency, fixed commitments.
- Transport and lodging: exact segments, locations, check-in/out, baggage, transfers, cancellation.
- Activities: status, operator, schedule, meeting point, requirements, inclusions, safety and fallback.
- Daily itinerary: time blocks, travel time, meals, reservations, costs, route, energy load, alternatives.
- Equipment and preparation: owned, provided, rent, buy, confirm, packing and purchase deadlines.
- Filming and narration: shots, restrictions, story facts, pronunciation, narration, source confidence.
- Budget: paid, confirmed-but-unpaid, estimated, contingency, currency assumptions, category-level splurge/save priorities, and any flexible or unconstrained categories.
- Sources: URL, claim supported, source role, last checked, recheck date.
- Decision history: decision, reason, alternatives rejected, date, and what changed downstream.

## Status vocabulary

Use a small consistent set:

- idea
- researching
- tentative
- selected
- booked
- completed
- cancelled
- rejected
- blocked

Do not collapse `selected` into `booked`. Attach a reason and next action to blocked or unresolved items.

## Consistency pass

After a material change, check affected dates, transit, opening hours, meals, reservations, lodging nights, pickup locations, recovery, budget, equipment, filming, and fallback plans. Update overview counts last so they reflect the details.

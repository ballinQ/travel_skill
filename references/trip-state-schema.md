# Canonical trip state

Maintain these concepts in the artifact or supporting structured data. Omit irrelevant fields rather than showing empty scaffolding.

## Core

- Traveler profile: origin, party, pace, interests, comfort, mobility/health constraints, dietary needs, food preference mix, photo/check-in profile, filming needs, preferred sources, queue tolerance, and reservation tolerance.
- Trip frame: destination, timezone, dates, duration, budget, currency, fixed commitments.
- Transport and lodging: exact segments, locations, check-in/out, occupancy, room and bed type, live total price, comparison baseline and price delta, tax/fee inclusion, breakfast, shuttle, parking, usable benefits, rate type, payment timing, star source, guest score scale, review count, price checked-at time, baggage, transfers, and cancellation.
- Activities: status, marketplace and operator, exact product variant, schedule, participants, live party total, price type, rating and review count, meeting or pickup point, guide language, group format, requirements, inclusions, exclusions, cancellation, checked-at time, safety, and fallback.
- Daily itinerary: time blocks, travel time, meals, reservations, costs, route, energy load, alternatives.
- Equipment and preparation: owned, provided, rent, buy, confirm, packing and purchase deadlines.
- Filming and narration: shots, restrictions, story facts, pronunciation, narration, source confidence.
- Budget: paid, confirmed-but-unpaid, estimated, contingency, currency assumptions, category-level splurge/save priorities, and any flexible or unconstrained categories.
- Sources: URL, claim supported, source role, last checked, recheck date.
- Decision history: decision, reason, alternatives rejected, date, and what changed downstream.
- Continuity checkpoint: last completed stage, current step, next action, open user decision, recent changes, source attempts, and last saved time.

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

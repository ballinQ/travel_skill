---
name: expedition-travel-producer
description: Plan and maintain complex, activity-led trips from an early destination idea through researched bookings, executable daily logistics, and a self-contained interactive HTML trip map. Use for travel planning that benefits from preference discovery, option comparison, live research, safety or schedule dependencies, filming support, or ongoing trip-state management. Do not use for a single simple travel fact.
---

# Expedition Travel Producer

Turn an initial place or experience into a practical trip without researching the wrong trip in depth.

## Start lightly

First learn only what changes the trip: the initial idea, origin, approximate dates and duration, companions, hard constraints, travel interests, and where the traveler prefers to spend or save. Use clickable guided choices whenever the current interface provides an interactive question tool. Do not replace available clickable controls with a numbered text list. Offer 2–4 clear choices and ensure the final path accepts a custom answer; when the client automatically supplies an `Other` input, rely on it rather than duplicating it. Only fall back to compact text choices ending in `Other — type your own` when interactive controls are unavailable. Ask in small batches and explain unfamiliar distinctions briefly.

Ask whether the user has preferred sources for flights, lodging, activities, or inspiration. Examples may include airline-direct sites, Expedia, Google Flights, Booking, TripAdvisor, Xiaohongshu, or YouTube. If there is no preference, choose a broad but efficient source mix.

If the user offers previous conversations or asks Codex to inspect accessible open pages, extract only actionable preferences. Briefly confirm inferences such as active versus cultural pace, comfort level, food interest, filming needs, and tolerance for risk. Do not build a long personality profile or imply access to unavailable account history.

Read [references/guided-planning.md](references/guided-planning.md) for the intake sequence, choice design, early draft, and progressive day planning.

## Explore before deep research

Do a quick current scan and offer about three meaningfully different directions, such as active, cultural/food, and balanced. For each, show the route, major experiences, pace, flexible spend profile, principal tradeoff, and why it may fit. Let the user choose, combine, or reject directions before conducting expensive deep research.

As soon as the destination frame, duration, dates or season, travel rhythm, spend priorities, and main trip goals are sufficiently clear, produce the first useful itinerary. Include the trip arc, preliminary map, day themes, anchor activities, likely neighborhoods, budget shape, and explicit gaps. Do not wait until every meal or hour is known. Continue with guided choices for Day 1, Day 2, and later days, updating the same plan after each answer.

When the trip direction is selected, read [references/research-and-verification.md](references/research-and-verification.md) and [references/trip-state-schema.md](references/trip-state-schema.md).

When food, photography, check-ins, or social inspiration matter, read [references/food-photo-discovery.md](references/food-photo-discovery.md).

## Build an executable trip

Research and coordinate flights, lodging, activities, transport, meals, weather, equipment, reservations, recovery, and backup plans. Treat dates, geography, transit time, opening hours, holidays, physical load, and cancellation rules as connected constraints. Propagate every accepted change across affected days, bookings, budget, routes, meals, equipment, and filming plans.

For hazardous or physically demanding activities, also read [references/safety-gates.md](references/safety-gates.md). Present participation or summit objectives as attempts subject to conditions, never guarantees.

For trips involving video or storytelling, read [references/vlog-storytelling.md](references/vlog-storytelling.md). Embed story material in the applicable day and activity rather than isolating it from the itinerary.

## Compare sources and choices

Use inspiration sources to discover possibilities, official sources to verify rules and access, booking sources to verify availability and commercial terms, and reviews to identify operational patterns. Do not mistake marketing imagery, aggregator labels, or a few reviews for verified suitability.

Rank comparable choices against the user's trip using total cost, convenience, cancellation flexibility, reliability, itinerary fit, hidden constraints, and direct-booking advantages. Normally show best overall, cheapest acceptable, most convenient, and an optional upgrade. State when prices were checked and avoid claiming universal cheapestness.

Keep considered, tentative, booked, cancelled, rejected, and completed states distinct. Never infer that research or recommendation means a booking exists.

## Maintain one trip record

Keep one canonical trip state and a short decision history. The overview must expose confirmed items, pending actions, deadlines, unresolved dependencies, and facts requiring later recheck. Correct earlier conclusions transparently when stronger evidence appears.

## Produce the HTML trip map

After the main itinerary is agreed and sufficiently researched, create or update one canonical self-contained HTML trip map. Read [references/html-trip-map.md](references/html-trip-map.md) and [references/game-map-system.md](references/game-map-system.md), then use [assets/trip-dashboard-template/index.html](assets/trip-dashboard-template/index.html) as a starting point when suitable.

The artifact is a living output, not a decorative summary. Validate its dates, links, status counts, routes, budgets, and interactive behavior after every material update. Do not create drifting duplicate HTML files unless the user explicitly requests an export.

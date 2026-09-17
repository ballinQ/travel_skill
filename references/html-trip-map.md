# HTML trip map specification

Create one self-contained, mobile-friendly HTML file that remains useful offline for core itinerary content. External map tiles or live links may require connectivity; make that limitation visible.

Create Version 0.1 once the trip frame and direction are clear. It may contain deliberately open time blocks, tentative locations, preliminary routes, and pending research, but must label them honestly. Update the same artifact after each meaningful guided choice instead of waiting for a fully researched final plan.

## Required experience

- Overview is the default view and source of truth.
- Day navigation follows chronological order.
- Status summary distinguishes booked, selected, tentative, pending, cancelled, and completed.
- Each day includes timeline, route, transit, meals, costs, reservations, conditions, backup, filming, and narration as applicable.
- The map contains every operationally relevant location with category filters and links back to its day.
- Booking cards preserve provider, product, price/currency, date, cancellation deadline, identifier when supplied, and source link.
- Hotel cards show the live total-stay price, tax/fee status, room type, rate type, stars, guest score with scale, review count, cancellation terms, source, and checked-at time.
- Budget separates paid, committed, estimated, and contingency amounts.
- Sources show what they support and when they were checked.
- Recheck list highlights volatile facts and deadlines.
- Emergency and essential contact information is easy to reach.
- A compact hero summarizes destination, dates, duration, budget, readiness, and countdown.
- Map pins and filters coordinate with location details and applicable itinerary days.
- Daily views expose weather, effort, transit, spend, decision gates, and recovery load at a glance.
- Support dark theme, print/PDF output, persistent checklist state, and deep links to days when useful.

Avoid a separate narration silo: embed narration in the matching day and activity. Avoid showing rejected comparisons in the execution view; retain only a concise decision note when it helps explain the plan.

## Implementation

Start from the bundled template when it fits, replacing sample content completely. Keep CSS and JavaScript in the file unless the user requests a project structure. Use semantic HTML, keyboard-operable controls, clear focus states, sufficient contrast, and responsive layouts. Escape inserted text and avoid injecting untrusted page content as HTML.

Prefer a visually specific design reflecting the destination rather than a generic admin dashboard. Decorative effects must not obscure operational information. The bundled template uses an offline-safe illustrated SVG route. A real map may use verified coordinates and online tiles, but must preserve an offline itinerary fallback and disclose connectivity requirements.

For information hierarchy, zoom levels, 2.5D landmarks, daily mission maps, interactions, and accuracy boundaries, read [game-map-system.md](game-map-system.md).

If precise coordinates are unavailable, do not invent them. Use verified map links or mark the location pending. If a route estimate is volatile, label it as an estimate and record the conditions.

## Validation

Check:

- All trip dates and weekday labels
- Lodging nights and flight boundaries
- Status counts against detailed cards
- Currency and budget arithmetic
- Links and anchors
- Tabs, accordions, filters, and print layout
- Theme, countdown, checklist persistence, map pins, and location drawer
- No duplicate IDs or hidden essential content
- Mobile readability
- No stale option presented as current

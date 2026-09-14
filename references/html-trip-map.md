# HTML trip map specification

Create one self-contained, mobile-friendly HTML file that remains useful offline for core itinerary content. External map tiles or live links may require connectivity; make that limitation visible.

## Required experience

- Overview is the default view and source of truth.
- Day navigation follows chronological order.
- Status summary distinguishes booked, selected, tentative, pending, cancelled, and completed.
- Each day includes timeline, route, transit, meals, costs, reservations, conditions, backup, filming, and narration as applicable.
- The map contains every operationally relevant location with category filters and links back to its day.
- Booking cards preserve provider, product, price/currency, date, cancellation deadline, identifier when supplied, and source link.
- Budget separates paid, committed, estimated, and contingency amounts.
- Sources show what they support and when they were checked.
- Recheck list highlights volatile facts and deadlines.
- Emergency and essential contact information is easy to reach.

Avoid a separate narration silo: embed narration in the matching day and activity. Avoid showing rejected comparisons in the execution view; retain only a concise decision note when it helps explain the plan.

## Implementation

Start from the bundled template when it fits, replacing sample content completely. Keep CSS and JavaScript in the file unless the user requests a project structure. Use semantic HTML, keyboard-operable controls, clear focus states, sufficient contrast, and responsive layouts. Escape inserted text and avoid injecting untrusted page content as HTML.

If precise coordinates are unavailable, do not invent them. Use verified map links or mark the location pending. If a route estimate is volatile, label it as an estimate and record the conditions.

## Validation

Check:

- All trip dates and weekday labels
- Lodging nights and flight boundaries
- Status counts against detailed cards
- Currency and budget arithmetic
- Links and anchors
- Tabs, accordions, filters, and print layout
- No duplicate IDs or hidden essential content
- Mobile readability
- No stale option presented as current

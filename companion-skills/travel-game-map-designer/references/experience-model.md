# Experience model

## Three coordinated views

### World overview

Frame the complete itinerary extent plus only enough surrounding geography to orient the traveler. Show bases, arrival and departure points, major visited zones, and signature landmarks. Context-only places stay small, quiet, and explicitly distinct from planned stops.

The overview should answer: Where is the trip happening? How far apart are the main areas? Where do we sleep? What is the route's overall logic?

### Daily mission

Make the day's operating area the visual subject. Show the start and return base, ordered stops, transport mode, segment duration, critical departure time, reservations, entrances, rest points, food, viewpoints, weather gates, and fallback options that affect execution.

The daily map should answer: What do I do next? When must I leave? How do I get there? What changes if the plan fails?

### Story mode

Use a short sequence of authored camera states tied to day cards or chapters. Each transition should reveal a useful relationship, not merely demonstrate animation. Let the traveler pause, scrub, skip, or exit story mode without losing position.

## Interaction grammar

- Selecting a day focuses its bounds and emphasizes its route.
- Selecting a stop highlights its matching timeline card and opens concise operational detail.
- Selecting a route segment shows mode, duration, distance, assumption, and fallback.
- Scrubbing time changes the active stop, route progress, and relevant light or weather state.
- Filters change visibility without destroying selection or scroll position.
- Back returns to the previous map state, not an arbitrary default.
- Deep links restore the selected day or stop when practical.

## Useful game patterns

- **Mission objective:** the day's purpose and completion conditions.
- **Discovery:** reveal optional context as the traveler explores; never hide required logistics.
- **Photo quest:** saved shot, suggested orientation, light window, and crowd tradeoff.
- **Food collection:** chosen dishes or neighborhoods, not a meaningless checklist of venues.
- **Travel stamps:** calm visual records of completed places, never a pressure mechanic.
- **Scenario switch:** rain, fatigue, closure, late start, or traffic changes the visible fallback.
- **Route replay:** animate movement along verified segments with time controls.

## Visual hierarchy

Use at least four display priorities:

1. Active operational stop or urgent gate
2. Planned stop or route
3. Trip context such as lodging, airport, or visited district
4. Famous orientation landmark not included in the plan

Use scale, contrast, elevation, lighting, label weight, and animation sparingly to express this hierarchy. Avoid encoding status by color alone.

## Camera behavior

Author named camera states for overview, each day, and important clusters. Bound pitch, zoom, and rotation so labels remain readable. A daily mission may use a cinematic transition into the area, but it should settle into a stable controllable view. Provide reset, north-up, and fit-day controls.

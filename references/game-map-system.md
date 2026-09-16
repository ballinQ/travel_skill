# Game-style trip map system

Build maps as edited travel worlds, not generic street maps. Their job is orientation, storytelling, and execution. They should resemble a polished game map or theme-park guide while preserving geographic truth.

## Three map levels

### Regional map

Use only when the trip crosses cities or distant regions. Show major geography, arrival points, overnight bases, and intercity movement. Remove neighborhood detail.

### Overview city map

Show the complete extent used by the itinerary plus enough context to understand it. For Los Angeles, this may include the coast, Santa Monica, central LA, Hollywood, Griffith Park, the Hollywood Hills, and other visited zones.

Retain coastlines, terrain, large parks, major itinerary districts, airports, lodging bases, famous orientation landmarks, and only the roads or transit lines needed to understand movement. Suppress residential streets, minor businesses, low-value attractions, generic labels, advertisements, and unrelated transit detail.

Visited locations must be visually stronger than contextual landmarks. Make context-only landmarks smaller, desaturated, or explicitly labeled `nearby`, so they cannot be mistaken for planned stops.

### Daily mission map

Make the day's operating area the visual subject. Use a tighter extent, larger landmark models, and more route detail. Show:

- Starting base and return point
- Ordered stops with time or mission number
- Walking, driving, transit, and tour segments with distinct styles
- Segment time and critical departure time
- Terrain, elevation, entrances, viewpoints, or meeting points that affect execution
- Food, rest, filming, and fallback locations relevant to that day
- A visible objective, completion state, and go/no-go gate when applicable

If a day revolves around the Hollywood Hills, the hills should dominate the composition. The Hollywood Sign, Griffith Observatory, trailheads, ridgelines, viewpoints, parking or pickup point, and relevant route should be legible. Downtown and the coast may remain as faint orientation context.

## Visual language

Use restrained isometric or 2.5D illustration rather than photorealistic 3D. Combine simplified terrain masses, elevation shadows, small landmark models, district zones, route animations, muted non-itinerary areas, numbered mission pins, a compact legend, compass, scale cue, and current-day indicator.

Landmark size communicates narrative importance, not literal scale. Preserve approximate position and direction so the map remains trustworthy.

## Interaction

- Selecting a landmark opens its day, time, status, significance, booking, filming note, and verified navigation link.
- Selecting a route shows mode, duration, distance, traffic assumption, and fallback.
- Filters cover planned stops, contextual landmarks, food, lodging, transport, filming, and safety.
- The overview can focus a day; a daily map can return to the overview without losing state.
- Keyboard, touch, reduced-motion, dark theme, print, and mobile layouts remain supported.

## Generation and data

Create structured map data for bounds, terrain, districts, landmarks, stops, route segments, and display priority. Verify coordinates before positioning items. Do not derive turn-by-turn navigation from decorative SVG geometry.

Prefer SVG/CSS for editable 2.5D maps. A generated raster illustration may be used as a background only after its geography is checked and operational pins and routes remain separate interactive overlays. External 3D or tile libraries are optional; preserve an offline fallback.

## Accuracy rules

- Never invent a road, entrance, viewpoint, trail, or transit stop.
- Label schematic geometry as illustrative.
- Link operational stops to a verified navigation provider.
- Distinguish planned, optional, fallback, and context-only locations.
- Do not make a beautiful map look more precise than the evidence supports.

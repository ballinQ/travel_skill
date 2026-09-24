---
name: travel-game-map-designer
description: Design or improve accurate, game-like interactive HTML travel maps with geographic hierarchy, 2.5D or 3D landmarks, daily mission views, route playback, and useful trip-state interactions. Use for travel-map UX or implementation, not ordinary itinerary writing or generic non-map websites.
---

# Travel Game Map Designer

Turn verified trip data into an explorable travel world that helps the traveler orient, decide, and execute. Make it feel authored and playful without weakening geographic truth or operational clarity.

## Establish the map's job

Inspect the existing artifact, trip state, framework, dependencies, coordinates, routes, and offline requirements before choosing an engine or visual direction. Identify the primary mode:

- **Overview:** communicate the trip's complete geographic shape and major anchors.
- **Daily mission:** execute one day with ordered stops, timing, movement, risks, and fallbacks.
- **Story mode:** reveal a route or day through camera-led chapters.

Do not make one view perform all three jobs at once. Read [references/experience-model.md](references/experience-model.md) when defining hierarchy, interactions, or game-like behavior.

## Choose the lightest capable rendering stack

Preserve the user's existing stack unless a change is justified.

- Prefer SVG/CSS for schematic, offline-first 2.5D maps with a small number of locations.
- Prefer MapLibre GL JS for real coordinates, camera movement, vector styling, terrain, and custom layers without committing to a proprietary basemap.
- Consider Mapbox GL JS when its maintained basemap, 3D landmarks, or commercial data materially improves the requested result and the user accepts tokens, terms, and online dependency.
- Add Three.js only for meaningful terrain, landmark models, atmosphere, or custom WebGL scenes that the map engine cannot express cleanly.
- Add deck.gl only for data-heavy paths, timed route playback, or many GPU-rendered objects.
- Use GSAP or an equivalent animation system only when native transitions are insufficient for a deliberate story or mission sequence.

Do not stack libraries merely for visual novelty. Read [references/implementation.md](references/implementation.md) before selecting dependencies, defining data, or implementing advanced rendering.

## Design from data, not decoration

Keep geographic data and presentation separate. Use structured records for bounds, districts, terrain, landmarks, planned stops, route segments, day membership, status, priority, verified links, and fallback relationships.

Use semantic zoom and narrative priority:

- suppress residential streets, minor businesses, generic labels, advertisements, and irrelevant attractions;
- retain terrain, coastlines, major parks, airports, trip districts, lodging bases, essential transport, and famous orientation landmarks;
- make visited stops stronger than contextual landmarks;
- let landmark size express narrative importance while preserving approximate position and direction;
- reveal detail as the camera moves closer instead of displaying everything at once.

Never invent coordinates, entrances, paths, traffic times, or terrain. Label schematic geometry as illustrative and link operational locations to a verified navigation source.

## Make play serve travel

Treat each day as a mission with an objective, ordered stops, route segments, current state, key timing, and recovery or fallback logic. Useful playful patterns include discovery, route playback, chapter progress, photo quests, food collections, stamps, and weather or energy scenarios.

Avoid points, streaks, artificial scarcity, competitive ranking, or celebratory motion that pressures the traveler into unsafe or unwanted activity. Never imply a tentative or researched item is booked or completed.

## Build resilient interaction

Coordinate the map, day cards, timeline, filters, drawer, and URL state. Preserve context when moving between overview and daily views. Every pointer interaction needs a keyboard and touch equivalent. Essential itinerary information must remain reachable when tiles, WebGL, animation, or network access fails.

Provide reduced-motion behavior and a low-power mode for heavy effects. Do not let camera animation block interaction. Avoid scroll hijacking, surprise rotation, continuous idle motion, tiny pins, hover-only details, and deep modal chains.

## Verify the experience

Render and operate the result at desktop and mobile sizes. If an interactive browser-testing skill is available, use it for complex behavior. Read [references/verification.md](references/verification.md) for the relevant acceptance checks.

Finish only when the map is geographically honest, operationally useful, visually specific to the destination, recoverable after failure, and smooth enough on the target device class.

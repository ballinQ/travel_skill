# Verification checklist

Choose checks proportional to the implementation.

## Geographic and trip integrity

- Overview bounds contain every planned location without excessive unrelated area.
- Daily bounds and route order match the itinerary.
- Coordinates, entrances, meeting points, and navigation links are verified.
- Planned, optional, fallback, contextual, booked, and completed states remain distinct.
- Mode, distance, duration, critical departure time, and assumptions agree with the day plan.

## Interaction

- Day, stop, pin, timeline, drawer, filters, and URL state remain synchronized.
- Back, reset view, north-up, fit-day, and close behavior are predictable.
- Rapid switching does not leave stale highlights or overlapping camera animations.
- Touch targets are usable and no essential detail depends on hover.
- Keyboard order, activation, escape behavior, focus return, and accessible names work.

## Motion and 3D

- Camera transitions settle in a readable view and can be interrupted.
- Reduced motion removes fly-throughs, route trails, pulsing, and parallax appropriately.
- Landmark models do not cover pins or imply false geographic precision.
- WebGL resource use remains stable after repeated day switching.
- The low-power or fallback experience preserves all operational information.

## Responsive and resilience

- Test representative desktop, tablet, and narrow-phone viewports.
- Test long place names, dense days, dark mode, print, and zoomed text.
- Simulate tile failure, slow loading, missing model, empty route, and unavailable WebGL.
- Confirm core itinerary, reservations, addresses, contacts, and fallback instructions remain usable offline.

## Experience quality

- The destination is recognizable without generic decorative clichés.
- Each animation communicates location, sequence, time, status, or change.
- The active task is visually obvious within a few seconds.
- Playful elements increase curiosity or memory without pressuring unsafe completion.
- The page still works when every decorative animation is disabled.

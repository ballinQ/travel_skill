# Expedition Travel Producer

A personal Codex skill that turns an early destination idea into a researched, executable trip and a self-contained interactive HTML trip map. It is designed especially for activity-led travel where bookings, physical demands, weather, transport, filming, and backup plans must work together.

## What it does

- Learns only the traveler preferences that materially affect the trip.
- Offers a few quick directions before spending time on deep research.
- Separates inspiration, official verification, booking data, and review evidence.
- Compares flights, lodging, and activities by total cost, convenience, flexibility, reliability, and itinerary fit.
- Maintains clear trip states such as tentative, selected, booked, completed, and cancelled.
- Coordinates dates, routes, recovery, weather, equipment, safety gates, meals, filming, and narration.
- Produces one canonical mobile-friendly HTML trip dashboard and map.

## Planning approach

The skill deliberately avoids producing a large itinerary immediately. It uses a staged workflow:

1. Briefly learn the traveler's idea, constraints, interests, pace, and preferred sources.
2. When offered, extract only useful preferences from accessible past conversations.
3. Perform a quick scan and offer a few meaningfully different trip directions.
4. Let the traveler select or combine a direction.
5. Deep-research the selected trip using appropriate official, booking, review, and inspiration sources.
6. Maintain confirmed, selected, tentative, rejected, cancelled, and completed items separately.
7. Produce and continually update one canonical HTML trip dashboard.

The skill does not claim to search every website or guarantee the universally lowest price. It compares a broad, efficient source set, records when volatile information was checked, and explains the tradeoffs behind its ranking.

## Install

Clone this repository into your personal Codex skills directory:

```bash
mkdir -p ~/.codex/skills
git clone https://github.com/ballinQ/travel_skill.git ~/.codex/skills/expedition-travel-producer
```

Start a new Codex task so the installed skill is discovered, then invoke it with:

```text
Use $expedition-travel-producer. I am thinking about visiting Japan, but I am not sure what kind of trip I want yet.
```

For an existing installation, update it with:

```bash
git -C ~/.codex/skills/expedition-travel-producer pull --ff-only
```

## Final trip artifact

After the itinerary direction is agreed and researched, the skill creates a responsive HTML trip map containing the operational details of the trip. Depending on the trip, this can include:

- An overview of bookings, pending work, deadlines, and rechecks
- Chronological daily plans and geographically sensible routes
- Flights, lodging, activities, restaurants, stores, and transport points
- Prices, cancellation terms, confirmation details, and source links
- Weather, clothing, equipment, health, safety, and fallback conditions
- Vlog shots, filming restrictions, background stories, and narration within each applicable day
- Confirmed and estimated budget totals

The HTML file is treated as a living trip record. An itinerary change should propagate to routes, bookings, meals, recovery, budget, equipment, and filming plans.

## Structure

- `SKILL.md` contains the primary behavior and routing instructions.
- `references/` contains research, state, safety, storytelling, and HTML-map guidance.
- `assets/trip-dashboard-template/` contains the reusable HTML starting point.

## Current maturity

This is an early working release derived from a real multi-stage Mexico volcano and Vlog planning workflow. The initial behavior, research model, state schema, safety guidance, storytelling guidance, and dashboard template are in place. Future updates will improve comparison scoring, map presentation, automated consistency checks, and real-world testing across different trip types.

## Contributing

Issues and focused improvements are welcome. Please keep the skill concise: reusable instructions belong in `SKILL.md`, conditional detail belongs in `references/`, and output-oriented files belong in `assets/`.

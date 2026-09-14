# Expedition Travel Producer

A Codex skill for turning an early destination idea into a researched, executable, activity-led trip and a self-contained interactive HTML trip map.

## What it does

- Learns only the traveler preferences that materially affect the trip.
- Offers a few quick directions before spending time on deep research.
- Separates inspiration, official verification, booking data, and review evidence.
- Compares flights, lodging, and activities by total cost, convenience, flexibility, reliability, and itinerary fit.
- Maintains clear trip states such as tentative, selected, booked, completed, and cancelled.
- Coordinates dates, routes, recovery, weather, equipment, safety gates, meals, filming, and narration.
- Produces one canonical mobile-friendly HTML trip dashboard and map.

## Install

Copy this repository into your personal Codex skills directory:

```bash
mkdir -p ~/.codex/skills
git clone REPOSITORY_URL ~/.codex/skills/expedition-travel-producer
```

Start a new Codex task and invoke it with:

```text
Use $expedition-travel-producer. I am thinking about visiting Japan, but I am not sure what kind of trip I want yet.
```

## Structure

- `SKILL.md` contains the primary behavior and routing instructions.
- `references/` contains research, state, safety, storytelling, and HTML-map guidance.
- `assets/trip-dashboard-template/` contains the reusable HTML starting point.

## Status

This is an early working version developed from a real multi-stage Mexico volcano and Vlog planning workflow. Expect the comparison rules and dashboard template to evolve through further testing.

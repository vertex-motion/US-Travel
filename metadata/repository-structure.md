# Repository Structure

Canonical inventory of planning files and their scope rules.

## Planning Files

| File | Owns |
| --- | --- |
| `01-trip-purpose.md` | Traveler intent, preferences, constraints, dates, pace, planning principles. No route options, tasks, or costs. |
| `02-current-plan-options.md` | Selected route, retained alternatives, rationale, major tradeoffs, open decisions. No booking details, day schedules, or logistics inventory. Link option details to `03-potential-options.md`. |
| `03-potential-options.md` | Registry for every considered option: routes, places, lodging, logistics, booking guardrails, split-family options, rejected/parked/retained/selected options. Keeps interest scores, current-fit notes, decision triggers, do-not-book guardrails. |
| `04-daily-itinerary.md` | Day-by-day plan: sleep location, activities, transfers, backups, source notes. References `05-trip-logistics.md` for lodging operating details. No booking facts, hotel addresses, confirmation details, check-in/checkout logistics, or cross-trip task ownership. |
| `05-trip-logistics.md` | Cross-day logistics: lodging bases, hotel operating details (check-in/checkout times, parking, fees, cancellation), rental car, airport buffers, luggage, route disruptions (active road closures, works, conditions affecting driving), fallback lodging. No day-by-day activity schedules, costs, committed spend, tasks, deadlines, or unresolved decisions. |
| `06-budget.md` | Costs, ranges, committed spend, quote assumptions, exchange rates, cost-control notes. Never sync to `index.html`. |
| `07-checklist.md` | All traveler tasks and open decisions: bookings, timed reservations, documents, deadlines, verification, follow-up, and unresolved questions requiring a traveler choice. No guardrails, rejected options, day plans, logistics constraints, or cost tracking. |
| `index.html` | Presentation view generated from `01-07`. Exclude `06-budget.md`. |

## Other Files

| File | Purpose |
| --- | --- |
| `air-tickets/air-tickets.pdf` | Booked air ticket documents. |
| `metadata/repository-structure.md` | This file — file inventory and planning scope rules. |
| `metadata/content-tags.md` | Planning content tag definitions and usage rules. |
| `work/` | Working notes and research scratch files. Not synced to `index.html`. |
| `CLAUDE.md` / `AGENTS.md` | Agent instructions. Must be kept identical. |

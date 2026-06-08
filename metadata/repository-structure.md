# Repository Structure

Canonical inventory of planning files and their scope rules.

## Planning Files

| File | Owns |
| --- | --- |
| `01-trip-purpose.md` | Traveler intent, preferences, constraints, dates, pace, planning principles. No route options, tasks, or costs. |
| `02-current-plan-options.md` | Selected route, retained alternatives, rationale, major tradeoffs. Link option details to `03-potential-options.md`. |
| `03-potential-options.md` | Registry for every considered option: routes, places, lodging, logistics, booking guardrails, split-family options, rejected/parked/retained/selected options. Keeps interest scores, current-fit notes, decision triggers, do-not-book guardrails. |
| `04-daily-itinerary.md` | Day-by-day plan: sleep location, activities, transfers, backups, source notes. No cross-trip logistics or task ownership. |
| `05-trip-logistics.md` | Cross-day logistics: lodging bases, hotel checks, rental car, airport buffers, parking, luggage, route-condition decisions, fallback lodging. No day-by-day schedules, sleep lines, costs, committed spend, tasks, deadlines, or unresolved decisions. |
| `06-budget.md` | Costs, ranges, committed spend, quote assumptions, exchange rates, cost-control notes. Never sync to `index.html`. |
| `07-checklist.md` | All traveler tasks: bookings, timed reservations, documents, deadlines, verification, follow-up. No guardrails, rejected options, day plans, logistics constraints, cost tracking, or unresolved decisions. |
| `08-open-questions.md` | Unresolved traveler decisions only — choices that must be made before content can move to another file. No tasks, deadlines, stable facts, options, costs, or quote checks. |
| `index.html` | Presentation view generated from `01-05` and `07-08`. Exclude `06-budget.md`. |

## Routing Out of `08-open-questions.md`

| Content type | Move to |
| --- | --- |
| Tasks, verification, deadlines, during-trip checks | `07-checklist.md` |
| Stable route and booking facts | `02`, `04`, or `05` |
| Options (any status) | `03-potential-options.md` |
| Costs, ranges, quote checks | `06-budget.md` |

## Other Files

| File | Purpose |
| --- | --- |
| `air-tickets/air-tickets.pdf` | Booked air ticket documents. |
| `metadata/repository-structure.md` | This file — file inventory and planning scope rules. |
| `metadata/content-tags.md` | Planning content tag definitions and usage rules. |
| `work/` | Working notes and research scratch files. Not synced to `index.html`. |
| `CLAUDE.md` / `AGENTS.md` | Agent instructions. Must be kept identical. |

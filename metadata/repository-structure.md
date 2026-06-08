# Repository Structure

Use these files as the canonical homes for planning state:

- `01-trip-purpose.md`: traveler intent, constraints, preferences, dates, pace, and planning principles. Do not store route options, tasks, or costs here.
- `02-current-plan-options.md`: selected route, retained alternatives, route rationale, and major tradeoffs. Link option details back to `03-potential-options.md`.
- `03-potential-options.md`: golden source for every found route, attraction, logistics, lodging, booking guardrail, split-family option, selected option, retained option, parked option, and rejected option. Maintain the 0-10 interest score there; `0` means no traveler input has been provided.
- `04-daily-itinerary.md`: day-by-day schedule, sleep locations, activities, transfers, backups, and source notes. Do not store cross-trip logistics or task ownership here.
- `05-trip-logistics.md`: cross-day logistics: lodging bases, hotel operating checks, car, airports, parking, luggage, buffers, route conditions, and fallback lodging.
- `06-budget.md`: category estimates, assumptions, ranges, committed spend, exchange rates, quote assumptions, and cost sources. Keep this file as the only budget page; do not sync it into `index.html`.
- `07-checklist.md`: single source for traveler tasks before, during, and after the trip, including bookings, timed reservations, checks, documents, and follow-up tasks.
- `08-open-questions.md`: unresolved traveler decisions that need a choice before they can move into itinerary, logistics, budget, option, or checklist files.
- `index.html`: generated or presentation-oriented trip view. Use planning files `01-05` and `07-08` as dashboard sources; exclude `06-budget.md`.

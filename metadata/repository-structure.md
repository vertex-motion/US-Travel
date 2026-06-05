# Repository Structure

Use these files as the canonical homes for planning state:

- `01-trip-purpose.md`: traveler intent, constraints, preferences, and planning principles.
- `02-current-plan-options.md`: selected route, current-route rationale, retained alternatives, and route tradeoffs. Link to `03-potential-options.md` for the canonical option registry.
- `03-potential-options.md`: golden source for every found route, attraction, logistics, lodging, or split-family option, including selected, retained, parked, and rejected options. Maintain the 0-10 interest score there; `0` means no traveler input has been provided.
- `04-daily-itinerary.md`: day-by-day schedule, sleep locations, activities, transfers, backups, and source notes.
- `05-lodging-transport.md`: base cities, hotel strategy, car, airport, parking, luggage, and transport logistics.
- `06-budget.md`: category estimates, assumptions, ranges, and cost sources. Keep this file as the only budget page; do not sync it into `index.html`.
- `07-booking-checklist.md`: reservations, timed-entry tasks, documents, deadlines, and verification work.
- `08-open-questions.md`: unresolved traveler decisions, research gaps, and assumptions that need confirmation.
- `index.html`: generated or presentation-oriented trip view. Use planning files `01-05` and `07-08` as dashboard sources; exclude `06-budget.md`.

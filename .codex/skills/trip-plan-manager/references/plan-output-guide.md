# Trip Plan Output Guide

## Recommended Document Set

Use existing repository structure first. If no structure exists beyond the source intent document, create only the files needed for the current request:

- `02-current-plan-options.md`: route, activity, lodging, and logistics options included in the working plan or retained as fallbacks.
- `03-potential-options.md`: options considered or researched but parked outside the working plan, with reasons and reconsideration triggers.
- `04-daily-itinerary.md`: day-by-day plan with timing, drive time, walking load, meals, and backup options.
- `05-lodging-transport.md`: hotels, base cities, rental car or transit, parking, airport logistics, and luggage constraints.
- `06-budget.md`: estimated costs by category with low/target/high ranges and source notes.
- `07-booking-checklist.md`: reservations, timed-entry tickets, cancellation deadlines, documents, and verification tasks.
- `08-open-questions.md`: unresolved traveler decisions, research gaps, and assumptions.

Do not create all files automatically. Add a document when it reduces complexity or preserves useful planning state.
Add a `Sources` section to any file that contains researched facts, estimates, rules, or availability-sensitive recommendations.

## Planning Brief Template

```markdown
## Planning Brief

- Travelers:
- Trip dates:
- Primary goals:
- Must-see places:
- Pace:
- Driving tolerance:
- Walking tolerance:
- Lodging preference:
- Food preferences:
- Budget posture:
- Hard constraints:
- Assumptions:
- Open questions:
```

## Current Plan Options Template

```markdown
## Included Options

| Option in the plan | Why it remains included | Where it appears |
| --- | --- | --- |

## Retained Alternatives

| Option kept available | Why it remains in the plan set | Decision trigger |
| --- | --- | --- |
```

## Daily Itinerary Template

```markdown
## Day 1: [Date or Trip Day] - [Base / Main Area]

- Sleep:
- Morning:
- Lunch:
- Afternoon:
- Dinner:
- Driving:
- Walking:
- Reservations:
- Backup plan:
- Source notes:
```

## Sources Template

```markdown
## Sources

| Fact or decision supported | Source | Original page | Accessed | Status |
| --- | --- | --- | --- | --- |
|  |  | [Page title](https://example.com) | YYYY-MM-DD | Current / Needs current verification |
```

Use one `Sources` section per planning file. Keep links close to the file they support so future updates can refresh the same source record.

## Potential Options Template

```markdown
| Potential option | Current fit / tradeoff | Reconsider if |
| --- | --- | --- |
|  |  |  |
```

Use this table for routes, attractions, logistics, lodging approaches, or booking ideas that were meaningfully considered and rejected. Tie each reason to traveler constraints, current research, route quality, budget posture, or explicit assumptions.

## Budget Template

```markdown
| Category | Low | Target | High | Basis / source |
| --- | ---: | ---: | ---: | --- |
| Lodging |  |  |  |  |
| Car / transport |  |  |  |  |
| Fuel / parking / tolls |  |  |  |  |
| Attractions |  |  |  |  |
| Food |  |  |  |  |
| Buffer |  |  |  |  |
```

## Quality Checks

- Every day has one primary sightseeing focus unless attractions are adjacent.
- Hotel changes are justified by meaningful distance, scenery, or cost savings.
- Transfer days include realistic packing, checkout, parking, meals, and arrival time.
- Luxury lodging recommendations consider both property quality and route convenience.
- Outdoor-heavy days include weather, daylight, closure, and backup considerations.
- Source-sensitive facts include original page links, source names, access dates, and verification status in the same file.
- Existing source links remain present after edits unless the supported fact is removed or the link is replaced with a better original page.
- Current plan options include a clear inclusion reason and a pointer to the detailed planning file.
- Open questions are written as decisions the traveler can answer, not vague reminders.
- Potential options include a clear reason they are outside the working plan and a trigger for reconsideration.

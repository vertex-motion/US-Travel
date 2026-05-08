# Trip Plan Output Guide

## Recommended Document Set

Use existing repository structure first. If no structure exists beyond the source intent document, create only the files needed for the current request:

- `02-route-options.md`: candidate routes, tradeoffs, and recommendation.
- `03-daily-itinerary.md`: day-by-day plan with timing, drive time, walking load, meals, and backup options.
- `04-lodging-transport.md`: hotels, base cities, rental car or transit, parking, airport logistics, and luggage constraints.
- `05-budget.md`: estimated costs by category with low/target/high ranges and source notes.
- `06-booking-checklist.md`: reservations, timed-entry tickets, cancellation deadlines, documents, and verification tasks.
- `07-open-questions.md`: unresolved traveler decisions, research gaps, and assumptions.

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

## Route Option Template

```markdown
## Option A: [Route Name]

| Segment | Base | Nights | Key sights | Approx. transfer | Notes |
| --- | --- | ---: | --- | --- | --- |

### Best For

- 

### Tradeoffs

- 

### Verification Needed

- 
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
- Open questions are written as decisions the traveler can answer, not vague reminders.

# Claude / Agent Instructions

## Session Start (Mandatory)

At the start of every session, run `git pull` before reading or editing any file. If the pull fails or conflicts, report it and stop until resolved.

## File Sync (Mandatory)

`AGENTS.md` and `CLAUDE.md` must be identical at all times. Apply every change to both files in the same commit. If they differ, reconcile before committing.

## Writing Rules

Apply to all technical documents, instructions, and planning files.

1. Write for action: state what to do, when, and what output is expected.
2. Be succinct. Imperative verbs, short sentences, no background narration.
3. Make requirements testable. Use `must`, `must not`, `can`, `optional` precisely.
4. Keep structure scannable: headings, numbered steps for ordered work, bullets for unordered rules.
5. Check existing files before adding guidance. Update stale content; don't layer on top.

## Units

State every distance in both miles and kilometers, miles first with kilometers in parentheses: `30 mi (48 km)`. Applies to all files, tables, research, and generated `index.html` output. Convert with 1 mi = 1.609 km, round both to the same style (whole numbers, or matching decimals). For a range, convert both ends: `30–35 mi (48–56 km)`. Do not state a distance in only one unit.

## Commit Workflow

Finalize all changes before committing. Commit directly to `main` and push to `origin/main` after each successful commit.

## Privacy

This repo is public. Never add personal data: contact details, document numbers, account numbers, booking references, payment details, exact addresses, or private family details. Use placeholders. If personal data is found, flag it before editing.

Sensitive personal files must never be committed. This includes tickets, insurance documents, IDs, passports, boarding passes, bookings, and any file containing the personal data listed above. Such files (and their folders) must be added to `.gitignore` and kept on disk only. Before any commit, verify no sensitive personal file is staged; if one is, unstage it, add it to `.gitignore`, and flag it.

The `private/` folder is the canonical, gitignored home for confidential trip data: actual hotel addresses, confirmation numbers, booking references, room/rate codes, and contact details. The tracked planning files reference bookings by city and date only; their real values live in `private/confidential.md`. Read and update that file when confidential details are needed, but never copy its contents into a tracked file.

## Duplication

One canonical home per fact. Before editing, check for existing coverage.

- `03-potential-options.md` is the registry for every trip option (selected, retained, parked, rejected). Add or update there first.
- `07-checklist.md` is the canonical home for all traveler tasks and open decisions. Do not track tasks or open questions elsewhere.
- Default option interest score to `0` (no input, not rejection).
- Link to the canonical file; don't restate its content.
- Intentional repetition must serve a distinct purpose (summary, checklist, rationale, evidence).

## Planning Files

See [`metadata/repository-structure.md`](metadata/repository-structure.md) for per-file scope rules and routing.

## Content Tags

See [`metadata/content-tags.md`](metadata/content-tags.md) for tag definitions and usage rules.

## Dashboard Sync

`index.html` is generated from planning files `01-07`. Never sync `06-budget.md`. Sync blocks tagged `current-plan`, `traveler-notes`, and `to-confirm` only.

The **Research** tab is bespoke (not generated from `01-07`). Each entry must be **self-contained**: a reader must be able to act on it without opening the research file — include the decision/recommendation and the key facts (e.g. options, costs, ages, links) that support it, as a table when comparing options. Keep it **summary-level, not exhaustive**: omit full reasoning, every source, and edge-case detail. Always keep the "Read the full paper" link for the complete write-up. When the linked research file changes, update the tab entry to match.

## Day Cards (Mandatory)

A day card is one day's plan in `04-daily-itinerary.md` (each `### Day`) and in `index.html` (`days[]`). It states a single committed plan: what to do and how, in time order.

- A day card must not contain alternative options, "choose one" / "or" swaps, "if not used" cross-references, optional-attraction roles, weather or backup plans, or rain contingencies. State one plan only.
- All alternatives, swaps, and fallbacks live only in `03-potential-options.md` and its `index.html` Potential Options and Potential Map tabs. Do not restate them in a day card.
- `days[]` must not use a `backup` field. Place `role` values must describe the committed stop (e.g. `Morning anchor`), never `Alternative`, `Optional`, `swap`, or `backup`.
- If conditions change (weather, closure, energy), rebuild the affected day card on request. Do not pre-list fallbacks.
- When the traveler reports an option done, set its `Plan status` to `Visited` in `03-potential-options.md` and its `planStatus` to `Visited` in `index.html`, with the visit date in the fit note. Do not schedule a `Visited` option into a later day card.

When building a day card, account for:

1. Availability: opening hours, closed days, holiday hours, and reservation/timed-entry release windows. Place each stop on a day it is open.
2. Crowds and light: pick the best day-of-week and time-of-day; sequence stops to avoid peak crowds, heat, and traffic.
3. Reservations: name what must be booked and route the task to `07-checklist.md`.
4. Season and weather: confirm the stop suits the travel-window climate (heat, fog, daylight).
5. Pace and driving: one main stop per day, two only if adjacent; respect the driving and walking tolerances in `01-trip-purpose.md`.
6. Family fit: pram access, child suitability, and meal timing.
7. Parking: per the Parking rule below.

## Parking (Mandatory)

Two place sets in `index.html` must carry a `parking` array:

1. Each discrete attraction in an itinerary day card (`days[].places[]`). Add or update its `parking` when adding, renaming, or replacing the attraction or sightseeing stop, in the same change.
2. Each concrete map place (`potentialMapPlaces[]`) whose option has a star (interest `>= 1`). Add or update its `parking` when an option reaches interest `>= 1`, or when adding, renaming, or replacing such a place. Rejected options are exempt. When a starred attraction also exists as a day place, reuse the same lots.

Parking renders in the day card, the Potential Map marker popup, and the Potential Options row (combined per option). Reuse `renderParking` / `renderParkingList`; do not hand-build the markup.

- Each `parking` entry must have a short `name` (a real lot name, or `P1`/`P2`/`P3` when none fits), a `cost`, and a `query` used for map links.
- List up to three parking areas per place.
- Each area must render four map buttons: Apple and Google, place (`P`) and route (`R`).
- Do not add `parking` to lodging bases, airports, route corridors, or combined placeholder entries.

## Trip Change Impact Review

When the user adds a fact, preference, constraint, booking, task, or decision: check impact across itinerary, route, lodging, transport, budget, checklist, options, and open questions. Present proposed follow-up changes as a table before making any change the user did not explicitly request.

| Affected area | Impact | Proposed change | User decision needed |
| --- | --- | --- | --- |
| `<file or trip area>` | `<what changes>` | `<specific update>` | `<yes/no or choice>` |

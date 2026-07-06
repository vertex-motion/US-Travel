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

The `private/` folder is the canonical, gitignored home for confidential trip data: actual hotel addresses, confirmation numbers, booking references, room/rate codes, and contact details. The tracked planning files may name the booked hotel, but must keep exact addresses, confirmation numbers, booking references, room/rate codes, and contact details out — those live in `private/confidential.md`. Read and update that file when confidential details are needed, but never copy its contents into a tracked file.

## Duplication

One canonical home per fact. Before editing, check for existing coverage.

- `03-potential-options.md` is the registry for every trip option (selected, retained, parked, rejected). Add or update there first.
- `07-checklist.md` is the canonical home for all traveler tasks and open decisions. Do not track tasks or open questions elsewhere.
- Default option interest score to `0` (no input, not rejection).
- Link to the canonical file; don't restate its content.
- Intentional repetition must serve a distinct purpose (summary, checklist, rationale, evidence).

## Categories (Mandatory)

Every option in `03-potential-options.md` and every `index.html` `potentialOptions[]` / `potentialMapPlaces[]` entry carries one `Category` / `category`. The table and map filters build from the distinct category values in the data, so a category needs no separate list to appear as a filter.

Assign category by the option's primary nature:

- **Universities** — the whole option is a college or university campus visit (grounds, quads, campus landmarks). Current members: Caltech, Occidental, UCLA, Claremont Colleges, Stanford, UC Berkeley.
- **Parks** — the whole option is a park, garden, open-space preserve, or national/state park. Includes city and urban parks, botanic gardens, and NPS/state units (national parks, monuments, preserves, conservation areas, state parks).
- Keep a stop in **Scenic Walks and Viewpoints** when it is a viewpoint, overlook, beach walk, or coastal drive, even if it sits inside a park. Classify by what the stop is for, not by the land's designation.
- Must not move an audience-split option (`Teen-Focused Split`, `Younger-Child Add-On`, `Dad-Focused Adventure`) or a `Route and Region` / `Logistics and Pacing` anchor into Universities or Parks. Those keep their category.

Split mixed options:

- An option must not bundle a park or campus with unrelated stops under one category. If it does, split it into two options: one for the park/campus (category `Parks` or `Universities`) and one for the rest (its original category).
- On split, reassign each `potentialMapPlaces[]` marker to the matching new option and set its `category`. Carry `parking`, `interest`, and `Plan status` to the half each marker belongs to.
- Apply the split in `03-potential-options.md` and `index.html` in the same change.

Decompose regions into discrete places:

- An option whose primary nature is a place (category `Attractions and Experiences`, `Scenic Walks and Viewpoints`, `Parks`, or `Universities`) must name one concrete, mappable place — one you can drop a single pin on and drive to. A region, corridor, whole park, or town (e.g. "Big Sur", "Death Valley") is a container, not a place.
- Must not use a region or bundle word as the attraction in the name: no `or`, no plural stop list, no `reach`, `area`, `corridor`, or `loop`. One place, one row. `Route and Region` and `Logistics and Pacing` anchors are exempt — they describe corridors by design.
- When a container is worth visiting, split it into one row per signature stop, each with its own `Category`, `interest`, `parking`, and `potentialMapPlaces[]` marker. Example: "Big Sur" → McWay Falls, Pfeiffer Beach, Bixby Creek Bridge, Pfeiffer Big Sur trail as separate rows.
- Each such option's description must state what the place is for — its distinguishing feature (e.g. "purple-sand cove", "waterfall onto the beach", "arched span over the canyon") — not only its location. A description giving only location fails this rule.
- Before recommending or adding a container, expand it to its named stops and web-check current access (road and lot status, closures, reservations); recommend the specific stops, not the container. This applies to day cards too: an itinerary stop must be a named place, never "a viewpoint" or "the visitor center".

Adding a category:

- A new category must have a distinct color in the `categoryColors` map in `index.html`. No other list needs editing.

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
- When the traveler reports past visits, in the same change you must: (1) mark every reported option `Visited` per the rule above; (2) rewrite the affected past day card(s) in `04-daily-itinerary.md` and `index.html` to record what was actually visited, in time order; and (3) replan every following day the change affects — drop or swap any now-visited stop, refill freed slots from Potential Options by interest, and re-apply the day-construction and Parking rules.
- `Plan status` / `planStatus` of `In the plan` must match a committed stop in the day cards. An option is `In the plan` only if it appears in a day card; otherwise it is `Potential option` (or `Visited` / `Rejected` / `Parked`). Booked route, lodging, and logistics anchors stay `In the plan`. Whenever a day card adds, drops, or swaps a stop, update that option's status in both `03-potential-options.md` and `index.html` in the same change.

When building a day card, apply these rules:

1. One area per day. Every sightseeing stop must lie in a single compact area. Keep each drive between consecutive stops to 20 min or less; where stops are within 1 mi (1.6 km), park once and walk. Do not scatter anchors across the metro.
2. Cap the day's driving. Total sightseeing driving must stay within the `01-trip-purpose.md` local tolerance (about 3 hr round trip from the base). Do not place a long (more than 1 hr each way) commute to the same far area on two consecutive days — fold that area into one day.
3. Limit anchors. One primary stop per day; add at most one or two short same-area stops (café, photo stop, viewpoint). Three or more separated anchors, or anything that breaks rules 1-2, is over-packed — split it.
4. Sequence for crowds, heat, and parking. Open the day at the hardest-parking or highest-crowd stop (rope-drop / opening) or a low-traffic window; keep indoor or shaded stops for midday heat; save viewpoints for golden hour only when parking and traffic are not worst then. If a stop's best-light window is its worst-parking window, take the easier window.
5. Pick the lowest-crowd open day. Place each stop on a day it is open and least busy; avoid weekend museum peaks, market rush, and event closures.
6. Reserve and route the task. Book timed or limited-entry stops and record each booking in `07-checklist.md`. Never schedule a stop you cannot reach before it closes.
7. Match weather and season. Outdoor and coastal stops on clear, cooler windows; indoor or shaded stops during peak heat; check fog for coastal viewpoints and daylight for sunset plans.
8. Keep buffer days light. Arrival days, pre-transfer days, and the day after a long drive carry at most one easy, base-near stop, or none.
9. Fit the family. Confirm pram access and child stamina, leave rest and meal gaps, and keep walking within the `01-trip-purpose.md` tolerance.
10. Fill by interest. Use limited day slots for the highest-interest starred options first; lower-rated or unscheduled options stay in Potential Options. Apply the Parking rule below to every stop.

## Hotel Line (Mandatory)

A base-change day is any day the traveler sleeps in a different hotel than the night before — every arrival and transfer day. On each base-change day, the last line of the day card must name the actual booked hotel and its parking.

- Applies in `04-daily-itinerary.md` (the final bullet of the `### Day`) and `index.html` (the last entry in `days[].places[]`).
- Name the actual booked hotel. Keep the exact street address in `private/confidential.md` only; the public `query` uses hotel name plus city, no street number.
- The `index.html` hotel place must carry a full `parking` widget (`parking[]` with map buttons), the same as an attraction. This is the exception to the lodging-base parking exemption.
- A same-base day (no hotel change) must not repeat the hotel line.

## Parking (Mandatory)

Two place sets in `index.html` must carry a `parking` array:

1. Each discrete attraction in an itinerary day card (`days[].places[]`). Add or update its `parking` when adding, renaming, or replacing the attraction or sightseeing stop, in the same change.
2. Each concrete map place (`potentialMapPlaces[]`) whose option has a star (interest `>= 1`). Add or update its `parking` when an option reaches interest `>= 1`, or when adding, renaming, or replacing such a place. Rejected options are exempt. When a starred attraction also exists as a day place, reuse the same lots.

Parking renders in the day card, the Potential Map marker popup, and the Potential Options row (combined per option). Reuse `renderParking` / `renderParkingList`; do not hand-build the markup.

- Each `parking` entry must have a short `name` (a real lot name, or `P1`/`P2`/`P3` when none fits), a `cost`, and a `query` used for map links.
- List up to three parking areas per place.
- Each area must render four map buttons: Apple and Google, place (`P`) and route (`R`).
- Do not add `parking` to airports, route corridors, combined placeholder entries, or a lodging base on a same-base day. Exception: the overnight hotel on a base-change day carries a full `parking` widget (see Hotel Line).

## Trip Change Impact Review

When the user adds a fact, preference, constraint, booking, task, or decision: check impact across itinerary, route, lodging, transport, budget, checklist, options, and open questions. Present proposed follow-up changes as a table before making any change the user did not explicitly request.

| Affected area | Impact | Proposed change | User decision needed |
| --- | --- | --- | --- |
| `<file or trip area>` | `<what changes>` | `<specific update>` | `<yes/no or choice>` |

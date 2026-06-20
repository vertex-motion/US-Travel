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

## Trip Change Impact Review

When the user adds a fact, preference, constraint, booking, task, or decision: check impact across itinerary, route, lodging, transport, budget, checklist, options, and open questions. Present proposed follow-up changes as a table before making any change the user did not explicitly request.

| Affected area | Impact | Proposed change | User decision needed |
| --- | --- | --- | --- |
| `<file or trip area>` | `<what changes>` | `<specific update>` | `<yes/no or choice>` |

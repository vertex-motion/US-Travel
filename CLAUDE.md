# Claude / Agent Instructions

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

Finalize all changes before committing. Push to GitHub after each successful commit.

## Privacy

This repo is public. Never add personal data: contact details, document numbers, account numbers, booking references, payment details, exact addresses, or private family details. Use placeholders. If personal data is found, flag it before editing.

## Duplication

One canonical home per fact. Before editing, check for existing coverage.

- `03-potential-options.md` is the registry for every trip option (selected, retained, parked, rejected). Add or update there first.
- Default option interest score to `0` (no input, not rejection).
- Link to the canonical file; don't restate its content.
- Intentional repetition must serve a distinct purpose (summary, checklist, rationale, evidence).

## Planning Files

See [`metadata/repository-structure.md`](metadata/repository-structure.md) for per-file scope rules and routing.

## Content Tags

See [`metadata/content-tags.md`](metadata/content-tags.md) for tag definitions and usage rules.

## Dashboard Sync

`index.html` is generated from planning files `01-05` and `07-08`. Never sync `06-budget.md`. Sync blocks tagged `current-plan`, `traveler-notes`, and `to-confirm` only.

## Trip Change Impact Review

When the user adds a fact, preference, constraint, booking, task, or decision: check impact across itinerary, route, lodging, transport, budget, checklist, options, and open questions. Present proposed follow-up changes as a table before making any change the user did not explicitly request.

| Affected area | Impact | Proposed change | User decision needed |
| --- | --- | --- | --- |
| `<file or trip area>` | `<what changes>` | `<specific update>` | `<yes/no or choice>` |

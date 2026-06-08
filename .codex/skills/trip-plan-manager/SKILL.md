---
name: trip-plan-manager
description: Create, update, or review trip plans from travel notes and research. Use when Codex needs to manage an itinerary, route, budget, lodging or transport plan, attraction shortlist, booking checklist, or decision log for a trip, especially in this US-Travel repository.
---

# Trip Plan Manager

## Overview

Turn trip intent and constraints into a maintained set of planning documents. Keep the plan traceable: every recommendation should connect back to traveler preferences, current research, tradeoffs, or an explicit assumption.

## Workflow

1. Read repository instructions and existing travel notes before editing.
   - Start with `AGENTS.md`, then read the repo-root `metadata/repository-structure.md`.
   - Use the metadata file to choose which numbered trip documents to read or update.
   - Preserve existing user edits. If a file is already modified, treat its content as intentional unless the user says otherwise.

2. Build a planning brief.
   - Extract travelers, dates, desired places, pace, lodging level, mobility limits, food preferences, budget posture, and non-negotiables.
   - List missing decisions as open decisions in the current-plan options document, but continue with clearly labeled assumptions when the plan can safely move forward.

3. Research volatile facts before using them.
   - Verify current prices, opening hours, ticket rules, closures, road conditions, timed-entry requirements, hotel availability, flights, transit, legal/visa rules, and safety guidance.
   - Prefer official sources for parks, attractions, airports, government rules, and venue hours. Use reputable aggregators for comparison shopping only when official sources are insufficient.
   - Add the original source page link, source name, and access date next to the fact or in the document's `Sources` section.
   - Keep source links in the same file as the facts they support. Do not rely on chat history or browser history as the record.
   - If browsing is unavailable, mark affected facts as `Needs current verification`.

4. Create or update the plan documents.
   - Follow existing repo naming if present; otherwise use numbered Markdown files at the repo root.
   - Keep `01-trip-purpose.md` as source intent.
   - Keep `03-potential-options.md` as the golden source for every found option, including selected, retained, parked, and rejected routes, attractions, logistics, lodging ideas, booking ideas, and split-family ideas.
   - Set each option's interest score in `03-potential-options.md` to `0` unless the traveler provides a 1-10 preference. Treat `0` as no input, not as rejection.
   - Link current-plan, itinerary, lodging, budget, checklist, and open-decision entries back to `03-potential-options.md` when they depend on an option.
   - Add later documents for current plan options, daily itinerary, lodging/transport, budget, and booking tasks as needed. Keep open decisions in the current-plan options document.
   - When trip data changes, update `index.html` in the same change so the presentation view stays current. Keep the Markdown files as the planning source of truth.
   - Use the output patterns in `references/plan-output-guide.md` when drafting new planning documents.
   - When editing existing documents, preserve valid source links. Update the access date when re-checking a source, replace dead or stale links with the current original page, and keep obsolete links only when they explain a prior decision.

5. Review the plan as a system.
   - Check that daily pacing matches driving and walking tolerance.
   - Avoid one-way routing mistakes, unrealistic transfer days, hidden ticket constraints, and plans that require being in two places at once.
   - Make tradeoffs explicit when optimizing for luxury, scenery, lower cost, fewer hotel changes, or slower pace.
   - Record rejected routes, attractions, logistics, or lodging approaches when they were meaningfully considered or researched.

6. Finish with a concise status.
   - Summarize changed files, key planning decisions, unresolved questions, and any facts that still need live verification.
   - Run available Markdown or project validation if the repository provides it.

## Editing Rules

- Prefer concise Markdown tables for side-by-side comparisons, budgets, and booking trackers.
- Use bullets for assumptions, risks, and rationale.
- Keep recommendations specific enough to act on: dates or day numbers, locations, estimated durations, booking windows, and decision owners when known.
- Do not invent exact costs, hours, drive times, hotel availability, or legal requirements without current verification.
- Link each researched recommendation, estimate, or constraint to its original source page. Use stable official pages when available, not search result pages or unsourced snippets.
- Maintain a `Sources` section in each planning file that contains researched facts. Include source name, URL, access date, supported fact, and status when the source needs re-checking.
- Keep family preferences and constraints visible in the plan instead of burying them in prose.
- For each current plan option, state why it remains included or retained as a fallback, point to the file where it is planned in detail, and ensure the option also appears in `03-potential-options.md`.
- For each parked or rejected option, state what was considered, why it is outside the working plan, and what constraint change would justify reconsidering it.

## Resources

- `metadata/repository-structure.md`: repo-root map of canonical planning files and their intent. Read it every time before editing trip files.
- `references/plan-output-guide.md`: document set, templates, quality checks, and planning heuristics for trip-plan creation.

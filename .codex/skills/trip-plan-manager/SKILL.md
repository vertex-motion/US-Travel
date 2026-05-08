---
name: trip-plan-manager
description: Create, update, or review trip plans from travel notes and research. Use when Codex needs to manage an itinerary, route, budget, lodging or transport plan, attraction shortlist, booking checklist, or decision log for a trip, especially in this US-Travel repository.
---

# Trip Plan Manager

## Overview

Turn trip intent and constraints into a maintained set of planning documents. Keep the plan traceable: every recommendation should connect back to traveler preferences, current research, tradeoffs, or an explicit assumption.

## Workflow

1. Read repository instructions and existing travel notes before editing.
   - Start with `AGENTS.md`, then read numbered trip documents such as `01-trip-purpose.md`.
   - Preserve existing user edits. If a file is already modified, treat its content as intentional unless the user says otherwise.

2. Build a planning brief.
   - Extract travelers, dates, desired places, pace, lodging level, mobility limits, food preferences, budget posture, and non-negotiables.
   - List missing decisions as open questions, but continue with clearly labeled assumptions when the plan can safely move forward.

3. Research volatile facts before using them.
   - Verify current prices, opening hours, ticket rules, closures, road conditions, timed-entry requirements, hotel availability, flights, transit, legal/visa rules, and safety guidance.
   - Prefer official sources for parks, attractions, airports, government rules, and venue hours. Use reputable aggregators for comparison shopping only when official sources are insufficient.
   - Record source links and the access date in the relevant planning document.
   - If browsing is unavailable, mark affected facts as `Needs current verification`.

4. Create or update the plan documents.
   - Follow existing repo naming if present; otherwise use numbered Markdown files at the repo root.
   - Keep `01-trip-purpose.md` as source intent. Add later documents for route options, daily itinerary, lodging/transport, budget, and booking tasks as needed.
   - Use the output patterns in `references/plan-output-guide.md` when drafting new planning documents.

5. Review the plan as a system.
   - Check that daily pacing matches driving and walking tolerance.
   - Avoid one-way routing mistakes, unrealistic transfer days, hidden ticket constraints, and plans that require being in two places at once.
   - Make tradeoffs explicit when optimizing for luxury, scenery, lower cost, fewer hotel changes, or slower pace.

6. Finish with a concise status.
   - Summarize changed files, key planning decisions, unresolved questions, and any facts that still need live verification.
   - Run available Markdown or project validation if the repository provides it.

## Editing Rules

- Prefer concise Markdown tables for side-by-side comparisons, budgets, and booking trackers.
- Use bullets for assumptions, risks, and rationale.
- Keep recommendations specific enough to act on: dates or day numbers, locations, estimated durations, booking windows, and decision owners when known.
- Do not invent exact costs, hours, drive times, hotel availability, or legal requirements without current verification.
- Keep family preferences and constraints visible in the plan instead of burying them in prose.

## Resources

- `references/plan-output-guide.md`: document set, templates, quality checks, and planning heuristics for trip-plan creation.

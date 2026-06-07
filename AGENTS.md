# Codex Instructions

## Instruction and Technical Documentation Guidance

Use these rules when writing or updating technical documents, including skills, agent instructions, runbooks, and implementation notes.

1. Write for action. State what the reader or agent must do, when to do it, and what output is expected.
2. Be succinct and direct. Prefer short sentences, imperative verbs, and concrete requirements over background narration.
3. Avoid description-only prose. Include context only when it changes a decision, prevents misuse, or explains a non-obvious constraint.
4. Make requirements testable. Use `must`, `must not`, `can`, and `optional` deliberately; avoid vague terms such as "usually", "robust", or "simple" unless they are defined.
5. Keep structure scannable. Use descriptive headings, numbered procedures for ordered work, bullets for unordered rules, and parallel phrasing in lists.
6. Prefer references over restating external material. Link to stable source documentation, code paths, issues, specs, or decision records whenever they support or constrain the instruction.
7. Keep examples minimal and executable. Include examples only when they remove ambiguity, and make commands or snippets match the current repository.
8. Preserve local truth. Check existing files and project conventions before adding broad guidance, and update stale instructions instead of layering new ones on top.
9. Optimize for future maintainers. Remove duplicated guidance, note ownership or scope boundaries, and keep each instruction close to the workflow it governs.
10. Review before committing. Verify that the document is accurate, concise, and free of filler.

## Commit Workflow

- Commit changes after all modifications have been finalized and reviewed.
- Sync committed changes to GitHub after each successful commit.

## Public Repository Privacy

- Treat this repository as public.
- Do not add personal data, private contact details, identifying document numbers, account numbers, booking references, payment details, exact home addresses, or private family details.
- Use placeholders or broad descriptions when a plan requires sensitive context.
- If existing personal data is discovered, flag it in chat and ask before editing or removing it unless the user explicitly requests cleanup.

## Duplication Review

- Before editing planning files, check nearby documents for the same fact, decision, task, or instruction.
- Keep one canonical home for stable traveler intent, route decisions, rejected options, budgets, booking tasks, and open questions.
- Use `03-potential-options.md` as the golden source for every found trip option, including selected, retained, parked, and rejected options.
- When adding a route, attraction, logistics, lodging, booking, or split-family option, add or update its row in `03-potential-options.md` first.
- Set the option interest score to `0` unless the traveler gives a 1-10 preference. Treat `0` as no input, not as rejection.
- Link other planning files to the option row or registry instead of duplicating full option rationale.
- Link or refer to the canonical file instead of restating the same material in another file.
- Keep necessary repetition when it supports use of the file on its own. This includes daily itinerary fields, status tables, and source rows required to keep researched facts traceable in the same file.
- Remove template prompts, stale summaries, and duplicate guidance when the surrounding content already answers the question.
- When repetition remains intentional, make each instance serve a distinct purpose, such as summary, action checklist, rationale, or source evidence.

## Planning Content Tags

Use planning tags to mark what each section or row is for.

- `current-plan`: Selected or confirmed trip plan content. Sync this tag to `index.html`.
- `traveler-notes`: Practical notes the traveler should see. Sync this tag to `index.html`.
- `to-confirm`: Outstanding checks or traveler-facing confirmation tasks. Sync this tag to `index.html`.
- `planning-notes`: Research direction, option exploration, rationale, and LLM working notes. Do not sync this tag to `index.html`.
- `sources`: Source evidence, citations, access dates, and verification status. Do not sync this tag to `index.html`.
- `constraints`: Rules, limits, preferences, privacy requirements, and decision boundaries. Do not sync this tag to `index.html`.
- `fallback`: Contingency options that are not part of the main working plan. Do not sync this tag to `index.html`.

When updating `index.html`, sync tagged content by default unless the tag is listed as non-sync above.

## Dashboard Sync

- Keep `index.html` as a presentation view for the trip plan.
- Do not sync `06-budget.md` into `index.html`.
- Keep budget details, cost ranges, cost controls, and quote tasks in `06-budget.md`.
- When updating `index.html`, use planning files `01-05` and `07-08` as the dashboard sources unless the user explicitly requests another source.

## Trip Change Impact Review

- When the user adds a trip fact, preference, constraint, booking, task, or decision, check how it affects the rest of the trip plan.
- Review affected itinerary days, route choices, lodging, transport, budget, booking checklist, potential options, and open questions.
- In chat, present proposed follow-up changes as a table before making changes the user did not explicitly request.
- Use this table format:

| Affected area | Impact | Proposed change | User decision needed |
| --- | --- | --- | --- |
| `<file or trip area>` | `<what the new input changes>` | `<specific update to make>` | `<yes/no or choice>` |

# Codex Instructions

## Commit Workflow

- Commit changes after all modifications have been finalized and reviewed.
- Sync committed changes to GitHub after each successful commit.

## Duplication Review

- Before editing planning files, check nearby documents for the same fact, decision, task, or instruction.
- Keep one canonical home for stable traveler intent, route decisions, rejected options, budgets, booking tasks, and open questions.
- Link or refer to the canonical file instead of restating the same material in another file.
- Keep necessary repetition when it supports use of the file on its own. This includes daily itinerary fields, status tables, and source rows required to keep researched facts traceable in the same file.
- Remove template prompts, stale summaries, and duplicate guidance when the surrounding content already answers the question.
- When repetition remains intentional, make each instance serve a distinct purpose, such as summary, action checklist, rationale, or source evidence.

## Trip Change Impact Review

- When the user adds a trip fact, preference, constraint, booking, task, or decision, check how it affects the rest of the trip plan.
- Review affected itinerary days, route choices, lodging, transport, budget, booking checklist, potential options, and open questions.
- In chat, present proposed follow-up changes as a table before making changes the user did not explicitly request.
- Use this table format:

| Affected area | Impact | Proposed change | User decision needed |
| --- | --- | --- | --- |
| `<file or trip area>` | `<what the new input changes>` | `<specific update to make>` | `<yes/no or choice>` |

## Technical Documentation Guidance

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

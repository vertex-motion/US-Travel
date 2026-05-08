# Codex Instructions

## Commit Workflow

- Commit changes after all modifications have been finalized and reviewed.

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

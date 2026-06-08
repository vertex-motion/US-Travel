# Planning Content Tags

Use tags to mark what each text block is for. Place `<!-- tag: <tag> -->` immediately before the paragraph, bullet list, ordered list, or table it controls. One tag per block.

## Tags

| Tag | Sync to `index.html` | Use for |
| --- | --- | --- |
| `current-plan` | Yes | Selected or booked trip facts, public-safe versions. |
| `traveler-notes` | Yes | Practical notes about a booked location, transport, route segment, or place to visit — what the traveler needs during the trip. |
| `to-confirm` | Yes | Outstanding checks, open decisions, traveler-facing confirmation tasks. |
| `planning-notes` | No | Research direction, option exploration, rationale, planning assumptions, LLM working notes. Use even when the text mentions a booked item if the purpose is planning, not traveler action. |
| `sources` | No | Source evidence, citations, access dates, verification status. |
| `constraints` | No | Rules, limits, preferences, privacy requirements, decision boundaries. |
| `fallback` | No | Contingency options not part of the main plan. |

## Usage Rules

- If multiple tags could fit, choose the most specific one.
- Group adjacent same-tag content into one block rather than tagging each item separately.
- Use tables only when they are the clearest format — not solely to carry a tag.
- When updating `index.html`, sync all blocks tagged `current-plan`, `traveler-notes`, and `to-confirm`. Skip all others.

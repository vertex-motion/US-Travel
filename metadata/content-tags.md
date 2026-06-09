# Planning Content Tags

Use tags to mark what each text block is for. Place `<!-- tag: <tag> -->` immediately before the paragraph, bullet list, ordered list, or table it controls. One tag per block.

## Tags

| Tag | Default sync to `index.html` | Use for |
| --- | --- | --- |
| `current-plan` | Yes | Selected or booked trip facts, public-safe versions. |
| `traveler-notes` | Yes | Practical notes about a booked location, transport, route segment, or place to visit — what the traveler needs during the trip. |
| `to-confirm` | Yes | Outstanding checks, open decisions, traveler-facing confirmation tasks. |
| `planning-notes` | No | Research direction, option exploration, rationale, planning assumptions, LLM working notes. Use even when the text mentions a booked item if the purpose is planning, not traveler action. |
| `sources` | No | Source evidence, citations, access dates, verification status. |
| `constraints` | No | Rules, limits, preferences, privacy requirements, decision boundaries. |
| `fallback` | No | Contingency options not part of the main plan. |

## Exception Override

To override the default sync behavior for a specific block, append an exception marker on the same line as the tag:

| Marker | Meaning |
| --- | --- |
| `<!-- except: sync -->` | Sync this block even though the tag default is no-sync. |
| `<!-- except: no-sync -->` | Do not sync this block even though the tag default is sync. |

Example:
```
<!-- tag: sources --><!-- except: sync -->
<!-- tag: current-plan --><!-- except: no-sync -->
```

## Usage Rules

- If multiple tags could fit, choose the most specific one.
- Group adjacent same-tag content into one block rather than tagging each item separately.
- Use tables only when they are the clearest format — not solely to carry a tag.
- The exception marker overrides the tag default for that block only. All other blocks with the same tag keep the default behavior.
- When updating `index.html`, sync blocks where the resolved behavior is sync (default yes, or default no with `<!-- except: sync -->`). Skip blocks where the resolved behavior is no-sync.

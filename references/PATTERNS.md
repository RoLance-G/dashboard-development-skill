# Reusable Dashboard Patterns — Evidence & Boundaries

Patterns here are general advice derived from observed work. Details and exact implementation belong in originating projects; first example: [Game Dashboard case study](https://github.com/RoLance-G/game-dashboard/blob/main/docs/GAME_DASHBOARD_CASE_STUDY.md).

| Problem | Reusable pattern | Boundary / when to avoid |
|---|---|---|
| UI looks like a dense CRUD admin panel | Establish typography hierarchy and one primary action per region | Don't hide frequent secondary actions merely for aesthetics |
| Settings duplicates navigation context | Reuse a single selection source of truth | Separate selectors may be appropriate if they represent independent objects |
| Inconsistent colors and ever-growing overrides | Semantic tokens for color and spacing, with visual regression comparisons | Tokenization alone is not a reason to rewrite stable layout |
| Thousands of historical rows | IndexedDB or similar structured storage; load archives on demand; cache summaries | Active list still may need pagination or virtualization |
| Sidebar badges repeatedly scan full task set | Single-pass aggregation keyed by parent entity | Cache invalidation and stale counts need testing |
| JSON export misses unloaded items | Export from persistent storage, not UI memory | Ensure export waits for pending writes and validates schema |
| Cloud backup from browser-only site | On-open check, explicit authorization, durable success/failure state | Not unattended after browser closes; token lifecycle is separate |
| Cloud API mocked test appears successful | Distinguish mocks, local browser tests, production OAuth/upload tests | Do not claim real external service success based on simulation |
| Chat transcript not reusable | Capture actual decisions, evidence, limitations, and changes | Avoid inventing absent early chat turns |
| General lessons pollute application repo | Maintain project history locally; promote proven lessons into separate Skill repository | Not every iteration needs a Skill update |

## Promotion rule

A pattern is added or changed only with linked, already-committed project evidence, an explanation of transferability, and an honest validation status. Store a dated entry under `docs/updates/` for each Skill promotion.

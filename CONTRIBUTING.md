# Contributing — Commit Conventions (Founder‑Grade)

Use semantic, governance‑aligned commits to keep the repo clean, searchable, and auditable.

Commit types (prefixes)

- doctrine:  
- spec:  
- vertical:  
- agent:  
- pipeline:  
- udp:  
- diagram:  
- governance:  
- meta:  

Examples

- doctrine: add appendix D integration map
- spec: define KΞMALLX vertical activation key
- udp: add pipeline heartbeat definitions
- vertical: create metamallx safe mode spec

Branch naming

- proposal/<short-descriptor> — for governance proposals
- fix/<area>-<short> — for small fixes and corrections
- chore/<area>-<short> — for maintenance tasks

PRs & reviews

- Every PR that modifies doctrine, activation, or go-live behavior must reference an issue and include rationale.
- Major doctrine or vertical changes require documented consensus and approvers (see /docs/governance.md).
- Keep PRs focused; include tests, validation, or dry-run artifacts for changes that affect activation.

Commit message format

- Use the prefix from the list above followed by a concise description. Optionally include a body describing rationale, tests, and rollbacks.

Examples:

- doctrine: add appendix D integration map
- spec: define KΞMALLX vertical activation key
- udp: add pipeline heartbeat definitions
- vertical: create metamallx safe mode spec

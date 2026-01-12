# Atlas Stack — MetaReasonX Governance Repository

Purpose
-------
Single source of truth for:
- doctrine-as-code
- diagrams
- keys and signals (specs, not secrets)
- agents and pipeline definitions
- UDP diagnostics (protocols)
- vertical activation specifications (MetaMallX, Love’s Pure Taste™, SNAP, MetaXida, MetaReasonX)

No system is considered "live" unless it is defined here.

Mission 001 — Code to Repository
-------------------------------
The first mission of the Atlas Stack is to canonicalize all governance, structure, and activation logic as code in this repository. This repo is the authoritative source for the Atlas Governance Doctrine, agent and pipeline definitions, diagnostic protocols, and vertical activation specifications.

Goals
-----
- Capture governance doctrine as executable/parseable artifacts.
- Keep diagrams and architecture artefacts in-sync with code.
- Store protocol and diagnostic specifications (no secrets).
- Define and version agent/pipeline manifests and activation flows.
- Enable traceable, auditable change through PRs and CI.

Repository layout (recommended)
-------------------------------
- /doctrine/           — doctrine-as-code (YAML, JSON, or DSL)
- /agents/             — agent manifests, capabilities, interfaces
- /pipelines/          — pipeline definitions and activation specs
- /diagrams/           — architecture diagrams (source files + exports)
- /protocols/          — diagnostics, UDP specs, message formats
- /keys-and-signals/   — key & signal *specs* (NOT secrets; only formats and rotation policies)
- /scripts/            — tooling for validation, generation, and CI helpers
- /docs/               — explanatory docs, onboarding, governance process
- /archive/            — historical snapshots and retired specs

Conventions
-----------
- Everything that affects activation, governance, or "go live" status must be committed here.
- Use structured, machine-readable formats where practical (YAML/JSON/TOML).
- Keep diagrams editable (source file + exported PNG/SVG/PDF).
- Do not commit secrets or private keys. Use references to secret stores and document access procedures.
- Every change that affects behavior must include tests or validation steps.

Validation & CI
---------------
- Provide linting/validation for doctrine, agent manifests, and pipeline files.
- Provide a test harness or dry-run mode for activation specifications where feasible.
- CI must verify that changes conform to schema and do not break existing contracts.

How to propose changes
----------------------
1. Open an issue describing the change or the governance decision.
2. Create a branch using a clear name: `proposal/<short-descriptor>` or `fix/<area>-<short>`.
3. Add or update files, include schema changes and validation tests.
4. Submit a pull request (PR) that references the issue and documents rationale.
5. Reviews should focus on correctness, compatibility, auditability, and governance implications.

Governance process
------------------
- Major doctrine changes require a formal proposal, discussion, and recorded consensus (see /docs/governance.md).
- Emergency or hotfix changes should be accompanied by post-merge review and retroactive justification.
- All merges affecting activation must list the responsible approvers.

Security
--------
- This repository stores only specs and protocol definitions. Never store private keys, credentials, or other secrets here.
- Document required secrets, their storage locations, and access procedures in /docs/security.md.
- Report vulnerabilities or sensitive disclosures via the maintainers' contact channel.

Contributing
------------
- See /CONTRIBUTING.md for contribution guidelines, branch rules, and commit message conventions.
- Keep changes small and focused; include tests and validation where applicable.

License & Attribution
---------------------
- License: MIT
- Love’s Pure Taste™ is a registered or claimed trademark of its respective owner; inclusion here is for reference only.

Maintainers & Contact
---------------------
- Maintainers: MetaReasonX governance group / @metareasonxai-del / governance@metaexample.org
- Contact: open an issue at https://github.com/metareasonxai-del/atlas-stack-or-mrx-atlas-stack-governance/issues

Acknowledgements
----------------
This repository centralizes governance artifacts for the Atlas Stack and is intended to enable reproducible, auditable activation across MetaReasonX ecosystems.

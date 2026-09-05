# AGENTS.md: ThinkingSeed Universal Agent Directives

> Standard protocol for autonomous coding agents operating within this repository.

## 1. Project DNA Concept
- A ThinkingSeed is the architectural DNA and technical memory of a project, **NOT its full source code repository**.
- Seeds reside in `001_Seed/` and provide high-density ground truth for conversational LLMs and coding agents.

## 2. Workflows
- **`/seed`**: Fast, hybrid snapshot. Generates `001_Seed/seed-[project-name].md`.
- **`/seedMaster`**: Deep, exhaustive audit. Generates `001_Seed/seed-[project-name]-master.md`.

## 3. Epistemic Rigor & Security
- `[CONFIRMADO]`: Directly verified in repository code/manifests.
- `[INFERIDO]`: Reasonable deduction.
- `[FALTANTE]`: Expected component currently absent (reflects real progress).
- Redact all credentials with `<REDACTED>`.

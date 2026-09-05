# CLAUDE.md: ThinkingSeed Integration for Claude Code

This repository uses the **ThinkingSeed Standard** (by Gravity HyperScale Thinking) to manage architectural context and project knowledge seeds.

---

## 🧬 Core Concept: Project DNA
- A **ThinkingSeed** is the **architectural DNA and technical memory** of a software project. **It is NOT the full source code repository**.
- Seeds are high-density, portable snapshots created to transfer accurate context to LLM conversational threads without exhausting token limits.
- When you read or generate a seed, understand that any missing files or sections marked as `[FALTANTE]` reflect real work-in-progress (WIP), NOT a broken file.

---

## 🛠️ Slash Commands / Workflows

### 1. `/seed` (Hybrid ThinkingSeed - Fast & Frequent)
When the user types `/seed` or asks for a project seed:
1. Inspect the current workspace (dependencies, file tree, entry points, configs, core flows).
2. Apply evidence tags: `[CONFIRMADO]`, `[INFERIDO]`, `[FALTANTE]`.
3. Sanitize all sensitive data (passwords, API keys, tokens) using `<REDACTED>`.
4. Ensure directory `001_Seed/` exists in the workspace.
5. Create or update `001_Seed/seed-[project-name].md` following the template in `ThinkingSeed_MasterHybrid.md` (or `.agents/skills/seed/SKILL.md`).
6. **MANDATORY:** Include the top banner declaring the document as project DNA / passive context, and the bottom handshake block for receptor models.

### 2. `/seedMaster` (Master ThinkingSeed - Deep & Exhaustive)
When the user types `/seedMaster` or asks for the deep/exhaustive master seed:
1. Perform a deep, granular inspection of the repository (testing strategy, CI/CD, contracts, failure modes, data persistence, technical debt).
2. Ensure directory `001_Seed/` exists in the workspace.
3. Create or update `001_Seed/seed-[project-name]-master.md` following `ThinkingSeed Master.md` (or `.agents/skills/seedMaster/SKILL.md`).
4. Apply strict evidence tags and secret redaction (`<REDACTED>`).

---

## 🔒 Security Policy
- **ZERO LEAKS:** Never commit or output actual credentials, API keys, or private certificates into any seed. Always replace with `<REDACTED>`.

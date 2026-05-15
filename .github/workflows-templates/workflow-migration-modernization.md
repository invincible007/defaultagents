# Workflow: Migration / Modernization (Incremental, Safe)

## Purpose
Plan and execute refactors/migrations with minimal risk and no breaking changes unless approved.

## Chain
1) Refactor/Migration → 2) Architect → 3) Data/API (if contracts/data change) → 4) Tester → 5) Ops → 6) Project Manager → 7) Coder → 8) Reviewer → 9) Release → 10) Documentation/Knowledge Curator

---

## Steps

### Step 1 — Migration Plan (no code)
@Refactor  
- Phased plan, entry/exit criteria, compatibility strategy, risk register.

### Step 2 — Structural alignment
@Architect  
- Confirm boundaries and system-level impacts.

### Step 3 — Contracts (if applicable)
@DataAPI  
- Versioning strategy, compatibility rules.

### Step 4 — Validation design
@Tester  
- Regression focus, acceptance checks by phase.

### Step 5 — Operational readiness
@Ops  
- Observability and rollback requirements per phase (spec only).

### Step 6 — Delivery plan
@ProjectManager  
- Timeline, milestones, dependencies.

### Step 7 — Implementation
@Coder  
- Implement phase-by-phase, provide verification mapping.

### Step 8 — Review & Release
@Reviewer → @Release  
- Quality + rollout safety.

### Step 9 — Documentation/Knowledge
@Documentation → @KnowledgeCurator  
- Update docs + record decisions and lessons learned.
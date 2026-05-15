# Workflow: Release / Rollout (Operational Safety)

## Purpose
Roll out changes safely with clear gates, rollback triggers, and monitoring.

## Chain
1) Release → 2) Ops → 3) Tester → 4) Security (if sensitive) → 5) Project Manager → 6) Coder (automation/config if needed) → 7) Documentation

---

## Steps

### Step 1 — Release plan (no code)
@Release  
- Strategy, phases, gates, rollback decision tree, release notes template.

### Step 2 — Ops readiness (no code)
@Ops  
- Monitoring/alerts/runbooks requirements, go-live checklist.

### Step 3 — Validation plan (no code)
@Tester  
- Smoke/regression criteria for each rollout phase.

### Step 4 — Security gate (conditional)
@Security  
- Confirm no security regression; add release gates if needed.

### Step 5 — Schedule and comms
@ProjectManager  
- Timeline, freeze windows, stakeholder comms plan.

### Step 6 — Implementation of automation/config (only if needed)
@Coder  
- Implement deployment automation/config per specs.

### Step 7 — Docs update
@Documentation  
- Release notes + operational notes (no code snippets).
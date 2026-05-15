# Workflow: Bug Fix (Fast but Governed)

## Purpose
Diagnose, fix, validate, and safely release a defect with minimal overhead.

## Entry Criteria
- Defect description exists
- Repro steps or logs are available (or can be obtained)

## Chain
1) Project Manager (optional triage) → 2) Reviewer (analysis) → 3) Tester (test design) → 4) Security (if relevant) → 5) Coder → 6) Reviewer → 7) Ops/Release (if production) → 8) Documentation/Knowledge Curator (if needed)

---

## Steps

### Step 1 — Triage (optional)
@ProjectManager  
- Confirm severity, scope, target release, owners, timeline.

### Step 2 — Diagnosis Review (no code)
@Reviewer  
- Identify likely root cause areas, risks, and what evidence is needed.
- Output: findings, suspected causes, verification steps.

### Step 3 — Validation Plan (no test code)
@Tester  
- Create test scenarios: repro, regression, negative paths.
- Output: test plan and coverage.

### Step 4 — Security check (conditional)
@Security  
- If bug touches auth/PII/permissions: threat/risk check and required mitigations.

### Step 5 — Fix Implementation
@Coder  
- Implement fix + tests (Coder only), provide mapping: fix → repro eliminated → tests.

### Step 6 — Review
@Reviewer  
- Validate changes meet quality and do not introduce regressions.

### Step 7 — Release/Ops (if prod)
@Ops → @Release  
- Confirm monitoring, rollback, rollout plan.

### Step 8 — Docs/Knowledge (if recurring/critical)
@Documentation → @KnowledgeCurator  
- Update troubleshooting/known issues, record decision/lessons learned.
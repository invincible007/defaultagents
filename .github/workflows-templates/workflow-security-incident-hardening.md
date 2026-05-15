# Workflow: Security Hardening (Threat → Controls → Implementation)

## Purpose
Identify security risks, define mitigations as requirements, implement safely, and verify.

## Chain
1) Security → 2) Compliance (if needed) → 3) Architect (if design changes) → 4) Tester → 5) Ops → 6) Coder → 7) Reviewer → 8) Release → 9) Knowledge Curator

---

## Steps

### Step 1 — Threat model and findings (no code)
@Security  
- Threat model + prioritized findings + security requirements + verification plan.

### Step 2 — Governance alignment (conditional)
@Compliance  
- Controls/evidence expectations if audit/regulatory applies.

### Step 3 — Architecture alignment (conditional)
@Architect  
- Validate trust boundaries and required design changes.

### Step 4 — Security test design (no code)
@Tester  
- Abuse cases, negative tests, verification checklist.

### Step 5 — Ops hardening requirements
@Ops  
- Secrets handling, monitoring/alerts, incident readiness (spec only).

### Step 6 — Implementation
@Coder  
- Implement mitigations + tests, map changes to SEC requirements.

### Step 7 — Review and release
@Reviewer → @Release  
- Validate quality and rollout gates.

### Step 8 — Record
@KnowledgeCurator  
- Decision log + traceability to SEC findings.
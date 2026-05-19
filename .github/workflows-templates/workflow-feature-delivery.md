# Workflow: Feature Delivery (Standard SDLC)

## Purpose
Deliver a feature end-to-end with clear requirements, design, contracts, implementation, validation, and operational readiness.

## Entry Criteria
- Feature idea exists (may be vague)
- Stakeholders and target users are known or discoverable

## Chain (Minimal subset is okay)
1) Strategist (if vague) → 2) Sparring Partner (optional) → 3) UX/UI → 4) User Story & AC → 5) Architect → 6) Data/API Contract → 7) Project Manager → 8) Coder → 9) Tester → 10) Reviewer → 11) Security → 12) Ops → 13) Release → 14) Documentation → 15) Knowledge Curator

---

## Step-by-step

### Step 1 — Strategy (when needed)
**Agent:** @Strategist  
**Goal:** clarify goals, scope, constraints, priorities, success metrics  
**Outputs:** scope in/out, priorities, roadmap phase suggestion, open decisions
**Artifact path:** `docs/strategy/<work-item>.md` (create/append)

**Auto-handoff to:** @SparringPartner (optional) or @UX

---

### Step 2 — Challenge (optional but recommended for non-trivial features)
**Agent:** @SparringPartner  
**Goal:** stress-test assumptions, identify risks, propose alternatives  
**Outputs:** critical questions, risk scenarios, decision pressure points
**Artifact path:** `docs/strategy/<work-item>.md` (append)

**Auto-handoff to:** @UX

---

### Step 3 — UX Flow / Wireframes
**Agent:** @UX  
**Goal:** user journey, screens, interactions, error states, accessibility notes  
**Outputs:** flow steps, wireframes (text/ASCII), interaction rules, edge UX states
**Artifact path:** `docs/ux/<work-item>.md` (create/append)

**Auto-handoff to:** @UserStory

---

### Step 4 — User Stories & Acceptance
**Agent:** @UserStory  
**Goal:** stories and testable acceptance criteria  
**Outputs:** US-IDs, AC (Given/When/Then), edge cases, DoR/DoD, open questions
**Artifact path:** `docs/requirements/<work-item>.md` (create/append)

**Auto-handoff to:** @Architect

---

### Step 5 — Architecture
**Agent:** @Architect  
**Goal:** define system boundaries, components, NFR considerations, diagrams (textual)  
**Outputs:** architecture overview, component interactions, data flow, risks, trade-offs
**Artifact path:** `docs/architecture/<work-item>.md` (create/append)

**Auto-handoff to:** @DataAPI (if APIs/data) and @ProjectManager

---

### Step 6 — Data & API Contracts
**Agent:** @DataAPI  
**Goal:** finalize contracts; remove ambiguity; versioning rules  
**Outputs:** endpoint catalog, schemas/specs (contract artifacts), error model, compat strategy
**Artifact path:** `docs/api/<work-item>.md` (create/append)

**Auto-handoff to:** @ProjectManager

---

### Step 7 — Delivery Plan
**Agent:** @ProjectManager  
**Goal:** tasks, dependencies, sprint plan, owners, milestones  
**Outputs:** WBS, dependency map, plan, risks, execution kickoff prompt
**Artifact path:** `docs/planning/<work-item>.md` (create/append)

**Auto-handoff to:** @Coder

---

### Step 8 — Implementation
**Agent:** @Coder  
**Goal:** implement per architecture + contracts + ACs  
**Outputs:** code/config/scripts as needed, mapping to ACs, brief verification summary

**Auto-handoff to:** @Tester and @Reviewer

---

### Step 9 — Test Design
**Agent:** @Tester  
**Goal:** test strategy + scenarios; no test code  
**Outputs:** test cases catalog, coverage matrix, failure modes, quality gates
**Artifact path:** `docs/testing/<work-item>.md` (create/append)

**Auto-handoff to:** @Reviewer

---

### Step 10 — Review
**Agent:** @Reviewer  
**Goal:** quality findings; no patch writing  
**Outputs:** prioritized findings, verification steps, risk notes, handoff to @Coder for fixes
**Artifact path:** `docs/reviews/<work-item>.md` (create/append)

**Auto-handoff to:** @Security (if sensitive) and @Ops/@Release (if moving to rollout)

---

### Step 11 — Security Review (as needed)
**Agent:** @Security  
**Goal:** threat model + security requirements + verification plan  
**Outputs:** SEC findings, mitigations as requirements, release checklist items
**Artifact path:** `docs/security/<work-item>.md` (create/append)

**Auto-handoff to:** @Ops and @Release

---

### Step 12 — Ops Readiness
**Agent:** @Ops  
**Goal:** deployment/monitoring/runbooks as specs; no YAML/scripts  
**Outputs:** CI/CD spec, observability spec, alerts policy, runbooks, go-live checklist
**Artifact path:** `docs/operations/<work-item>.md` (create/append)

**Auto-handoff to:** @Release

---

### Step 13 — Release Planning
**Agent:** @Release  
**Goal:** rollout safety plan, versioning, rollback decision tree  
**Outputs:** release plan, gates, rollback triggers, validation checklist, release notes template
**Artifact path:** `docs/release/<work-item>.md` (create/append)

**Auto-handoff to:** @Documentation and @KnowledgeCurator

---

### Step 14 — Documentation
**Agent:** @Documentation  
**Goal:** README/guide updates; no code snippets  
**Outputs:** structured docs, onboarding steps (descriptive), troubleshooting notes
**Artifact path:** `docs/documentation/<work-item>.md` (create/append)

**Auto-handoff to:** @KnowledgeCurator

---

### Step 15 — Knowledge Curation
**Agent:** @KnowledgeCurator  
**Goal:** decision log, traceability, glossary, cross-references  
**Outputs:** KB entry, ADR/decision record, trace map, gaps list
**Artifact path:** `docs/knowledge/<work-item>.md` (create/append)
``
# 🧠 Agent Capability Matrix

## Purpose
This matrix defines **what each agent can and cannot do** so the system remains predictable, governed, and scalable.

### 🚨 Global Rule (Non‑Negotiable)
- ✅ **ONLY `@Coder Agent`** may:
  - write code
  - output code blocks
  - create/modify config files, scripts, pipelines, manifests
- ❌ **All other agents** must not write code or output code blocks.
- 🗑️ **Meeting Companion Agent is deleted** and must not be referenced.

---

## Legend
- ✅ Allowed
- ⚠️ Limited / Conditional (see notes)
- ❌ Not allowed

---

## Capability Categories (Definitions)
- **Route/Orchestrate**: decide next agent(s), ordering, handoff prompts
- **Strategy/Scope**: goals, priorities, phased roadmap (no design)
- **Challenge**: devil’s advocate, risk probing, alternatives
- **UX/Flows**: user journeys, wireframes (text), interaction behavior (no UI code)
- **Stories/AC**: user stories, acceptance criteria, DoR/DoD
- **Architecture**: system boundaries, patterns, NFRs, diagrams (textual)
- **Contracts**: API/data schemas/specs as *contract artifacts* (no implementation)
- **Planning/Tracking**: tasks, dependencies, sprints, status
- **Implementation**: code/config/scripts (Coder only)
- **Testing/QA**: test strategy + cases (no test code unless Coder)
- **Review**: quality findings (no patching)
- **Security**: threat model + security requirements (no patching)
- **Compliance**: controls/evidence/checklists (no legal advice, no implementation)
- **Performance**: profiling/measurement plan and perf budgets (no scripts)
- **Ops/Release**: deployment/runbooks/rollout plans as specs (no configs)
- **Documentation**: README/guides (no code snippets)
- **Knowledge**: decision log, traceability, glossary
- **Research**: compare options with confidence + gaps (no speculation)
- **Semantic**: clustering, similarity reasoning, RAG strategy (conceptual)
- **Math/Logic**: proofs, calculations, complexity (no pseudocode)
- **Vision**: interpret visuals into structured text (no hallucination)

---

## Capability Matrix

| Agent | Route / Orchestrate | Strategy / Scope | Challenge | UX / Flows | Stories / AC | Architecture | Contracts | Planning / Tracking | Testing / QA | Review | Security | Compliance | Performance | Ops / Release | Documentation | Knowledge | Research | Semantic | Math / Logic | Vision | Implementation (Code/Configs) | Output Code Blocks |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Router | ✅ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ |
| Strategist | ❌ | ✅ | ⚠️ | ❌ | ⚠️ | ❌ | ❌ | ✅ | ❌ | ❌ | ⚠️ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Sparring Partner | ❌ | ⚠️ | ✅ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ |
| UX/UI Design | ❌ | ❌ | ⚠️ | ✅ | ⚠️ | ⚠️ | ❌ | ❌ | ⚠️ | ❌ | ⚠️ | ⚠️ | ❌ | ❌ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| User Story & AC | ❌ | ⚠️ | ⚠️ | ⚠️ | ✅ | ❌ | ❌ | ⚠️ | ✅ (design only) | ❌ | ⚠️ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Architect | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ✅ | ⚠️ | ⚠️ | ⚠️ | ✅ (design review only) | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Data & API Contract | ❌ | ❌ | ⚠️ | ❌ | ⚠️ | ⚠️ | ✅ | ❌ | ⚠️ (contract tests design) | ✅ (contract review) | ⚠️ | ⚠️ | ❌ | ❌ | ⚠️ (API docs text) | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Project Manager | ❌ | ⚠️ | ❌ | ❌ | ⚠️ | ❌ | ❌ | ✅ | ⚠️ | ❌ | ⚠️ | ⚠️ | ❌ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Coder | ❌ | ❌ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ✅ |
| Tester | ❌ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ✅ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Reviewer | ❌ | ❌ | ⚠️ | ⚠️ | ⚠️ | ✅ (alignment) | ⚠️ | ❌ | ⚠️ | ✅ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Security | ❌ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ⚠️ (test scenarios) | ⚠️ (findings) | ✅ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Compliance & Governance | ❌ | ⚠️ | ❌ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ✅ | ❌ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Performance & Profiling | ❌ | ❌ | ⚠️ | ❌ | ❌ | ⚠️ | ❌ | ❌ | ⚠️ (perf test design) | ⚠️ (perf review) | ⚠️ | ❌ | ✅ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ⚠️ | ❌ | ❌ | ❌ |
| Ops Agent | ❌ | ❌ | ⚠️ | ❌ | ❌ | ⚠️ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ✅ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Release & Deployment | ❌ | ⚠️ | ⚠️ | ❌ | ❌ | ⚠️ | ❌ | ✅ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ✅ | ✅ (release notes structure) | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Dev Environment & Tooling | ❌ | ❌ | ⚠️ | ❌ | ❌ | ⚠️ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ✅ (guides text) | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Integration & Dependency | ❌ | ❌ | ⚠️ | ❌ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ❌ | ⚠️ | ❌ | ❌ | ❌ | ❌ |
| Refactor & Migration | ❌ | ❌ | ⚠️ | ❌ | ⚠️ | ⚠️ | ⚠️ | ✅ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Documentation | ❌ | ❌ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ✅ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Knowledge Curator | ❌ | ⚠️ | ❌ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ⚠️ | ✅ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ |
| Researcher | ❌ | ⚠️ | ⚠️ | ❌ | ❌ | ⚠️ | ⚠️ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ❌ | ✅ | ⚠️ | ❌ | ❌ | ❌ | ❌ |
| Embedder | ❌ | ❌ | ❌ | ❌ | ❌ | ⚠️ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ⚠️ | ❌ | ❌ | ⚠️ | ⚠️ | ✅ | ❌ | ❌ | ❌ | ❌ |
| Math | ❌ | ❌ | ❌ | ❌ | ❌ | ⚠️ | ❌ | ❌ | ⚠️ | ⚠️ | ❌ | ❌ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ | ❌ |
| Vision | ❌ | ❌ | ❌ | ✅ (interpretation only) | ❌ | ⚠️ | ⚠️ | ❌ | ⚠️ | ⚠️ | ⚠️ | ⚠️ | ❌ | ❌ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ✅ | ❌ | ❌ |
| Autocomplete (Handoff‑Only) | ❌ | ❌ | ❌ | ❌ | ⚠️ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ | ❌ |

---

## Notes (Important Clarifications)

### Router (v2)
- Router is **allowed to reference** all capabilities only to decide routing/order.
- Router is **not allowed** to perform the work or produce deliverables.

### Coder (Only code-producing agent)
- Only Coder can output code blocks and modify configs/scripts/pipelines.
- Coder should remain **requirements- and design-driven**.

### Data & API Contract
- Can output **contract artifacts** (OpenAPI/JSON Schema) as interface definitions.
- Must not provide application implementation.

### Tester / Reviewer / Security / Ops / Release
- Produce **plans, findings, specifications, checklists** — no executable output.

### Documentation
- Must avoid code snippets; if code examples are required, hand off to Coder.

### Autocomplete
- Disabled for code output; used only to clarify completion intent and hand off to Coder.

---

## Quick Compliance Check (One-liner)
✅ If an agent is not `@Coder`, it must never produce code or code blocks.
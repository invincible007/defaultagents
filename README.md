# 🤖 Ramukaka (RK) Agent Framework (VS Code GitHub Copilot)

> **Scope:** This handbook explains how to use the repository’s Copilot Agents effectively and safely in VS Code. It includes governance rules, end‑to‑end workflows, approval-based chaining, and practical “how‑to” playbooks.

---
## 0) Why "Ramukaka"?

This framework draws its name and spirit from **Ramu Kaka** — one of Hindi cinema's most enduring and beloved character archetypes.

Ramu Kaka is far more than a servant. He is the **steady hand** in every household he serves — a figure of unwavering loyalty, quiet wisdom, and boundless devotion. Across decades of Hindi films, Ramu Kaka has been the trusted confidant, the gentle advisor, and the moral compass who has been with the family through generations.

He represents something rare and precious: **reliable service with dignity**.

That is exactly what this framework aspires to be for your development team:

- **Loyal** — always present, always ready, never failing when you need it most
- **Wise** — seasoned with governance, experience, and best practices
- **Trusted** — the steady presence that keeps the house of code running smoothly
- **Selfless** — focused entirely on serving the team's success, not on taking credit

Each agent in this framework is named "RK_[Role]" in honor of that tradition — a reminder that great service, whether in a household or a codebase, is built on trust, consistency, and quiet excellence.

> *"Ramu Kaka was not just part of the family. He was the family."*

---
## 1) What this is
This repository uses **GitHub Copilot Agents defined in-repo** (stored under `.github/agents/*.md`) to standardize how work is clarified, designed, implemented, validated, released, and documented.

### Goals
- **Predictability:** consistent outputs and collaboration patterns
- **Governance:** prevent accidental implementation from non‑implementation agents
- **Speed with safety:** rapid iteration without skipping critical steps
- **Traceability:** connect requirements → design → contracts → implementation → tests → release → docs → knowledge

---

## 2) Non‑negotiable governance rules
### 2.1 Only one agent can write code
- ✅ **Only `@Coder`** may write code or output code blocks.
- ❌ All other agents must **not** generate code or code blocks.

### 2.2 Router v2 uses the Approval Pattern
- Router proposes the **next step** and asks **Proceed? (Yes/No)**.
- Only when you answer **Yes** does Router emit the runnable `@NextAgent` prompt.

### 2.3 Meeting Companion is deleted
- 🗑️ Do not reference or route to Meeting Companion.
- Use:
  - `@ProjectManager` for actions/follow‑ups
  - `@KnowledgeCurator` for decisions/long‑term memory

### 2.4 User preferences are mandatory
- `userpreferences.json` **must exist** at workspace root before the framework operates.
- On first interaction, the Router **must** present the setup wizard and create this file.
- The Router **must not** process any request until `userpreferences.json` is in place.
- This is a **hard gate** — no routing, no agent invocation, no task execution without it.

### 2.5 Discovery-first (no guessing)
- If requirements are unclear, agents must ask clarifying questions before producing outputs.

---

## 3) Repo navigation (where everything lives)
- `.github/agents/` — agent definitions (`*.agent.md`)
- `.github/agent-policy.md` — global rules
- `.github/agent-capability-matrix.md` — quick capability view
- `.github/agent-capability-registry.md` — detailed catalog
- `.github/output-artifact-standard.md` — standard output-to-file routing and naming rules
- `.github/workflows-templates/` — workflow playbooks
- `docs/` — progressive, cumulative project artifacts generated during SDLC

---

## 4) How to use agents in VS Code (practical)
### 4.1 How to invoke an agent
In Copilot Chat (VS Code), start your message with the agent mention:
- `@Router …`
- `@Architect …`
- `@UserStory …`
- `@Coder …`

> **Recommendation:** Start with `@Router` for anything that is not a trivial one‑liner.

### 4.2 How the Approval Pattern feels (Yes/No)
1) You run `@Router` with your request.
2) Router returns:
   - Intent summary
   - Routing plan
   - Proposed next step
   - **Proceed? (Yes/No)**
3) You answer **Yes**.
4) Router outputs a runnable `@Agent` prompt.
5) You run that prompt.
6) After that agent responds, return to `@Router` with the output and continue.

### 4.3 Fast commands you can use
- `Yes` / `Proceed` / `Go` — approve the proposed next step
- `No — <reason>` — reject and adjust
- `Adjust: …` — change scope/order/constraints
- `Skip: <agent or step>` — skip a step if already done
- `Approve All` — request a full prompt pack (still execute step-by-step)

---

## 5) Agent cheat sheet (when to use what)
### 5.1 Orchestration
- `@Router` — routing, sequencing, approval-gated orchestration

### 5.2 Strategy / requirements
- `@Strategist` — goals, scope, priorities, roadmap
- `@UserStory` — user stories, acceptance criteria, DoR/DoD

### 5.3 Design
- `@UX` — flows, wireframes (text), interactions, accessibility notes
- `@Architect` — boundaries, patterns, NFRs, diagrams (text)
- `@DataAPI` — contracts/specs, schema rules, versioning
- `@Integration` — external integration strategy + dependency policy

### 5.4 Implementation (ONLY)
- `@Coder` — code/config/scripts/pipelines/manifests

### 5.5 Quality & risk
- `@Tester` — test strategy and test cases (no code)
- `@Reviewer` — review findings (no patch writing)
- `@Security` — threat model + security requirements
- `@Compliance` — controls/evidence/checklists (no legal advice)
- `@Performance` — perf measurement plan/budgets (no scripts)

### 5.6 Operations & release
- `@Ops` — CI/CD & ops specifications, monitoring/runbooks (no configs)
- `@Release` — rollout plan, gates, rollback, versioning

### 5.7 Knowledge
- `@Documentation` — docs/guides (no code snippets)
- `@KnowledgeCurator` — decision logs, traceability, glossary

### 5.8 Specialist utilities
- `@Vision` — interpret diagrams/mocks (facts only)
- `@Embedder` — semantic clustering/retrieval strategy (conceptual)
- `@Math` — proofs/calculations/complexity (no pseudocode)
- `@Autocomplete` — handoff-only completion clarifier (no code)

---

## 6) Workflow templates (how to run playbooks)
All playbooks are designed for **approval-gated chaining**.

### 6.1 How to run a workflow
1) Start with Router:
   - `@Router Use workflow <name> for: <your request>`
2) Router proposes step 1 → you answer **Yes/No**
3) Execute step 1
4) Return outputs to Router and continue

---

## 7) Workflow: Feature Delivery (Standard SDLC)
**Use when:** building a feature end-to-end.

### Recommended chain
Strategist → Sparring → UX → UserStory → Architect → DataAPI → ProjectManager → Coder → Tester → Reviewer → Security → Ops → Release → Documentation → KnowledgeCurator

### How-to (template prompt)
1) Start:
- `@Router Feature Delivery: <feature description> (include constraints and target users)`

2) Approve each step:
- Router proposes the next step → you answer `Yes` or `No/Adjust/Skip`.

### Outputs you should expect
- UX: flows/wireframes/interactions
- UserStory: story IDs + ACs + DoR/DoD
- Architect: boundaries/NFR/risk/tradeoffs
- DataAPI: contract artifacts + versioning
- PM: tasks/sprints/dependencies
- Coder: code changes + mapping to AC

---

## 8) Workflow: Bug Fix (Fast but governed)
**Use when:** defect needs diagnosis + fix + validation.

### Recommended chain
ProjectManager (optional) → Reviewer (diagnosis) → Tester (scenario plan) → Coder (fix) → Reviewer (verify) → Ops/Release (if prod) → Documentation/KnowledgeCurator (if recurring)

### How-to
- `@Router Bug Fix: <symptom> | repro: <steps> | expected: <x> | actual: <y> | severity: <level>`

---

## 9) Workflow: Spike / Research (Option analysis → decision)
**Use when:** comparing technologies or approaches.

### Chain
Researcher → SparringPartner → Strategist → Architect (if needed) → KnowledgeCurator

### How-to
- `@Router Spike: Compare <A> vs <B> for <context> with constraints <...>`

---

## 10) Workflow: Migration / Modernization (Incremental & safe)
**Use when:** refactoring or migrating frameworks/infrastructure.

### Chain
Refactor → Architect → DataAPI (if needed) → Tester → Ops → ProjectManager → Coder → Reviewer → Release → Documentation → KnowledgeCurator

### How-to
- `@Router Migration: <from> → <to> | constraints: <compatibility, downtime, windows>`

---

## 11) Workflow: Security Hardening (Threat → controls → implementation)
**Use when:** threat modeling, mitigation planning, security validation.

### Chain
Security → Compliance (if needed) → Architect (if needed) → Tester → Ops → Coder → Reviewer → Release → KnowledgeCurator

### How-to
- `@Router Security Hardening: <area> | assets: <...> | concerns: <...>`

---

## 12) Workflow: Release / Rollout (Operational safety)
**Use when:** planning rollout gates and rollback readiness.

### Chain
Release → Ops → Tester → Security (if needed) → ProjectManager → Coder (automation) → Documentation

### How-to
- `@Router Release Plan: <services> | strategy: canary/blue-green/rolling | constraints: <SLOs, windows>`

---

## 13) How‑To Playbooks (common tasks)

### 13.1 “I have a vague idea” → get to implementable requirements
1) `@Router I have an idea: <describe>`
2) Approve Strategist
3) Approve UserStory
4) Approve Architect
5) Approve Coder (only when ready)

### 13.2 “Challenge my design” (before building)
- `@SparringPartner Challenge this plan: <paste>`

### 13.3 Convert a diagram/mock into a design
1) `@Vision Interpret this diagram (facts only)`
2) `@UX` for flows (if UI)
3) `@Architect` for system design

### 13.4 Create sprint plan from approved stories
- `@ProjectManager Create a 2-week plan for US-xxx with dependencies and owners`

### 13.5 Contracts-first API development
1) `@DataAPI Define contract for <resource>`
2) `@Tester` define contract test scenarios
3) `@Coder` implement per contract (only code agent)

### 13.6 Add security gates to feature delivery
- Ask Router:
  - `Adjust: include Security review before implementation` (for sensitive features)

---

## 14) Practical “Yes/No” patterns (approval gating)
### 14.1 Use **Yes** when
- The next agent and outputs match your intent
- Constraints are included
- The step is not premature

### 14.2 Use **No** when
- Wrong agent chosen
- Wrong order
- Missing constraints

### 14.3 Use **Adjust:** for precision
Examples:
- `Adjust: skip UX; we already have wireframes`
- `Adjust: include compliance constraints for PII`
- `Adjust: treat as bug fix workflow`

### 14.4 Use **Skip:** to bypass completed steps
Examples:
- `Skip: Strategist (scope approved)`
- `Skip: DataAPI (no API changes)`

---

## 15) Troubleshooting

### 15.1 A non-RK_Coder outputs code
This violates policy.
- Reply: `Stop. No code. Follow agent policy. Hand off to @Coder.`
- Then reroute:
  - `@Router This step violated no-code policy. Re-run correctly.`

### 15.2 Router tries to send directly to Coder too early
- Reply: `No — enforce Coder Protection Gate. Route upstream first.`

### 15.3 Agent repeats questions you already answered
- Provide missing context/outputs in your message.
- Or ask Router to include the prior outputs in the next runnable prompt.

### 15.4 Someone references Meeting Companion
- Reply: `Meeting Companion is deleted. Use PM for actions and Knowledge Curator for decisions.`

---

## 16) Contribution guide (maintaining the agent system)

### 16.1 Adding a new agent
A new agent must include:
- strict scope
- no-code rule (unless it is Coder)
- structured output format
- explicit handoffs
- compatibility with approval gating

Update:
- `.github/agent-capability-matrix.md`
- `.github/agent-capability-registry.md`

### 16.2 Updating Router
Router is the governance engine. Changes must preserve:
- approval gating
- Coder protection gate
- meeting companion exclusion

---

## 17) FAQ

### Q: Does Router truly auto-run agents?
No. Router emits approval-gated runnable prompts. You execute them in VS Code Copilot Chat.

### Q: Why is only Coder allowed to write code?
To keep behavior predictable and prevent accidental code/config output from non-implementation agents.

### Q: What should I do after each agent output?
Return to Router with the output and let it propose the next step.

---

## 17.5) First-Time Setup Wizard

When you start a new project, Router will ask 4 quick questions to customize agent behavior:

### Q1 — Response Style
- **Verbose** — Long and explanatory
- **Concise** — Short and direct
- **Caveman** — Simple language in framing text only

### Q2 — Approval Gate Tone
- **Plain** — Standard "Proceed? (Yes / No)"
- **Punny** — Humorous punchline, then ask
- **Superhero** — Movie quote, then ask
- **Random Fact** — Fun fact, then ask

### Q3 — Parallel Agents
- **No** — Sequential only
- **Yes** — Then pick how many: 2 / 3 / 4

### Q4 — Execution Chunk Size
- **Tiny** — Small chunks (low VRAM / context window)
- **Balanced** — Medium chunks (decent VRAM / context window)
- **Blazing** — All guns blazing (enterprise mode)

Preferences are saved to `userpreferences.json` at the workspace root.

### Changing Preferences Later
Tell Router:
- `change local preferences`
- `update behaviour of agents`

Router will show current values and let you update any setting.

> **Note:** Style preferences only affect greeting, closing, and approval-gate framing text. Structured output (tables, lists, findings, handoffs) always remains professional and precise.

---

## 18) Progressive Artifact Storage (New)

To keep knowledge and decisions cumulative, agent outputs should be stored under `docs/` using standard folders.

### 18.1 Standard locations
- Strategy outputs → `docs/strategy/<work-item>.md`
- UX outputs → `docs/ux/<work-item>.md`
- User stories / AC → `docs/requirements/<work-item>.md`
- Architecture blueprints → `docs/architecture/<work-item>.md`
- Data/API contracts → `docs/api/<work-item>.md`
- Planning outputs → `docs/planning/<work-item>.md`
- Test strategy/cases → `docs/testing/<work-item>.md`
- Review findings → `docs/reviews/<work-item>.md`
- Security outputs → `docs/security/<work-item>.md`
- Compliance outputs → `docs/compliance/<work-item>.md`
- Performance outputs → `docs/performance/<work-item>.md`
- Ops readiness/runbooks → `docs/operations/<work-item>.md`
- Release plans → `docs/release/<work-item>.md`
- Documentation plans/IA notes → `docs/documentation/<work-item>.md`
- Decision logs / traceability → `docs/knowledge/<work-item>.md`

### 18.2 Naming convention
- Use kebab-case for `<work-item>` (example: `checkout-v2`).
- Reuse the same file for the same work item and append dated sections over time.
- Use clear section headers like `## 2026-05-18 - Architecture update` to keep history progressive.

### 18.3 Router behavior expectation
- Router should include a target artifact path whenever it emits a runnable agent prompt.
- If no target path is provided, ask Router to include it before proceeding.

---

✅ **End of Ramukaka (RK) Agent Framework**

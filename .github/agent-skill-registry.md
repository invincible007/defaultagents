# 🎓 Agent-to-Skills Registry

## Overview
This registry maps agents to their recommended skills. All agents have access to **universal skills**; specialized agents also have domain-specific skills.

---

## 🌍 Universal Skills (Available to ALL 26 Agents)

These skills are foundational for any agent:

| Skill | Purpose |
|-------|---------|
| `rc-handoff` | Pass work to another agent |
| `rc-grill-me` | Stress-test your plan/thinking |
| `rc-session-summary-prompt` | Compact context for next chat |
| `rc-find-skills` | Discover available skills |
| `rc-diagnose` | Figure out what's broken/failed |
| `rc-git-workflow` | Understand repo state & workflows |

---

## 🎯 Agent Skill Matrix

### Implementation Agents

#### **Coder Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-tdd` | Development | Test-driven development workflow |
| `rc-docker` | Infrastructure | Containerization & image optimization |
| `rc-terraform` | Infrastructure | Infrastructure-as-code provisioning |
| `rc-kubernetes` | Infrastructure | Kubernetes deployment & management |
| `rc-git-commit-push` | Git | Commit & push workflows |
| `rc-setup-pre-commit` | Development | Pre-commit hooks & lint-staged setup |
| `rc-neon-postgres` | Database | PostgreSQL setup & optimization |
| `rc-migrate-to-shoehorn` | Testing | Migrate tests to @total-typescript/shoehorn |

---

### Quality & Review Agents

#### **Reviewer Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-code-review` | Review | Comprehensive code review guidance |
| `rc-codeprobe` | Audit | Master code audit skill |
| `rc-codeprobe-architecture` | Audit | Architecture structure analysis |
| `rc-codeprobe-code-smells` | Audit | Code smell detection |
| `rc-codeprobe-error-handling` | Audit | Error handling & resilience review |
| `rc-codeprobe-framework` | Audit | Framework-specific anti-patterns |
| `rc-codeprobe-patterns` | Audit | Design pattern opportunities |
| `rc-codeprobe-performance` | Audit | Performance & scalability issues |
| `rc-codeprobe-solid` | Audit | SOLID principle violations |
| `rc-codeprobe-testing` | Audit | Test quality & coverage gaps |

#### **Tester Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-codeprobe-testing` | Audit | Test quality audits |
| `rc-test-commander` | Testing | Test execution & orchestration |

#### **Security Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-codeprobe-security` | Security | Security vulnerability scanning |
| `rc-codeprobe` | Audit | Master code audit skill |
| `rc-codeprobe-patterns` | Audit | Security-relevant design patterns |
| `rc-codeprobe-solid` | Audit | Secure design principles |
| `rc-codeprobe-framework` | Audit | Framework-specific vulnerabilities |

---

### Architecture & Strategy Agents

#### **Architect Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-grill-with-docs` | Strategy | Align decisions with domain language (CONTEXT.md) |
| `rc-improve-codebase-architecture` | Architecture | Find refactoring opportunities |
| `rc-codeprobe-architecture` | Audit | Architecture structure analysis |

#### **Strategist Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-grill-with-docs` | Strategy | Align decisions with domain language |

#### **Knowledge-Curator Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-grill-with-docs` | Strategy | Align decisions with domain language |
| `rc-setup-context-repo` | Documentation | Initialize domain knowledge repos |

---

### Design & UX Agents

#### **UX-UI-Design Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-design` | Design | Visual & interaction design |
| `rc-prototype` | Prototyping | Mock up UI variations |
| `rc-responsive-engine` | Design | Responsive design guidance |

---

### Infrastructure & Operations Agents

#### **Ops Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-kubernetes` | Infrastructure | Kubernetes deployment & management |
| `rc-terraform` | Infrastructure | Infrastructure-as-code provisioning |

#### **Release-Deployment Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-terraform` | Infrastructure | Infrastructure-as-code provisioning |
| `rc-docker` | Infrastructure | Containerization & image optimization |

#### **Dev-Environment-Tooling Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-setup-pre-commit` | Development | Pre-commit hooks & lint-staged setup |
| `rc-setup-context-repo` | Documentation | Initialize project structure |

#### **Performance-Profiling Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-performance-profiler` | Performance | Profiling, benchmarking & perf budgets |

---

### Planning & Documentation Agents

#### **Project-Manager Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-to-issues` | Planning | Convert plans into implementation tickets |
| `rc-triage` | Planning | Issue triage & workflow management |

#### **Refactor-Migration Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-tdd` | Development | Test-driven refactoring |
| `rc-improve-codebase-architecture` | Architecture | Find refactoring opportunities |

#### **Documentation Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-scaffold-exercises` | Documentation | Create exercise structures |
| `rc-to-prd` | Documentation | Write PRD-style documents |

#### **User-Story-Acceptance Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-to-prd` | Documentation | Write PRD-style documents |
| `rc-to-issues` | Planning | Convert plans into tickets |

---

### API & Data Agents

#### **Data-Api-Contract Agent**
| Skill | Category | Purpose |
|-------|----------|---------|
| `rc-api-forge` | API Design | REST/GraphQL/webhook design guidance |

---

### Foundational/Future Agents (Universal Skills Only)

These agents currently use only universal skills. Specialized skills will be added as these areas develop:

| Agent | Status | Notes |
|-------|--------|-------|
| **Compliance-Governance** | Scaffolded | Future: governance/compliance tools |
| **Embedder** | Scaffolded | Future: semantic/RAG strategy tools |
| **Integration-Dependency** | Scaffolded | Future: integration/dependency tools |
| **Math** | Scaffolded | Future: mathematical reasoning tools |
| **Researcher** | Active | Theoretical research only (universal skills) |
| **Vision** | Active | Visual interpretation only (universal skills) |
| **Sparring-Partner** | Active | Challenge/devil's advocate (universal skills) |
| **Autocomplete** | Active | Quick clarification (universal skills) |
| **Router** | Active | Orchestration (universal skills) |

---

## 📋 Legend

**Category Types:**
- **Development:** Code-writing, testing, TDD workflows
- **Infrastructure:** Cloud, containers, IaC
- **Git:** Version control workflows
- **Audit:** Code quality, security, performance scanning
- **Review:** Manual review & feedback
- **Strategy:** Domain language, decision alignment
- **Architecture:** System design, refactoring
- **Design:** UX/UI, interaction flows
- **Prototyping:** Flush out designs
- **Documentation:** Writing, scaffolding
- **Planning:** Issues, workflows, triage
- **API Design:** REST, GraphQL, contract design
- **Performance:** Profiling, benchmarking
- **Database:** DB setup, optimization

---

## 🔄 How Skills Are Used

1. **Recommended Skills** are baked into each agent's frontmatter (`recommendedSkills` field)
2. Each agent knows when to invoke a skill based on their primary domain
3. **Universal skills** are always available for meta-work (handoff, diagnosis, context-switching)
4. **Specialized skills** are scoped to agents most likely to use them to avoid decision paralysis

---

## 📝 Notes

- This registry was created through collaborative grilling with clear trade-off decisions
- Skills are mapped based on **primary use case** (not exclusivity)
- New skills should be assigned to the most relevant agent + considered for universal access
- Review this registry quarterly as new skills are added

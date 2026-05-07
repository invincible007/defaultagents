# 🔀 **Agent Routing Rules**
Defines how tasks are assigned to the correct agent based on intent, complexity, and context.

---

# 🧭 **1. Routing Philosophy**
Routing must be:
- **Deterministic** — same input → same agent  
- **Minimal** — route to the *single* best agent  
- **Composable** — complex tasks may be split  
- **Escalation‑aware** — unclear tasks escalate to Strategist or Architect  

---

# 🧩 **2. Routing Decision Tree**

## **Step 1 — Identify Intent**
Intent categories:

| Intent Type | Route To |
|------------|----------|
| Architecture | Architect |
| Coding | Coder |
| Research | Researcher |
| Planning | Strategist |
| Review | Reviewer |
| Testing | Tester |
| Security | Security |
| UX/UI | UX/UI |
| Data/API | Data & API Contract |
| Performance | Performance |
| Ops/CI/CD | Ops |
| Release | Release |
| Refactoring | Refactor/Migration |
| Integration | Integration |
| Documentation | Documentation |
| Knowledge | Knowledge Curator |
| Meetings | Meeting Companion |
| Project Planning | Project Manager |

---

## **Step 2 — Check for Multi‑Intent Tasks**
If a task spans multiple domains:

- **Router Agent** decomposes it  
- Each sub‑task is routed independently  
- Final output is aggregated  

---

## **Step 3 — Escalation Conditions**
Escalate to **Strategist** if:
- Requirements unclear  
- Scope ambiguous  
- Priorities missing  

Escalate to **Architect** if:
- System boundaries unclear  
- Cross‑module impact  
- Infra or design decisions required  

---

# 🧱 **3. Routing Examples**

### **Example 1 — “Design a scalable API”**
→ Architect  
→ Data/API Contract  
→ Coder  
→ Tester  

### **Example 2 — “Improve performance of this endpoint”**
→ Performance Agent  
→ Coder  
→ Tester  
→ Ops  

### **Example 3 — “Write acceptance criteria for this feature”**
→ User Story & Acceptance Agent  
→ Project Manager  
→ Tester  

---

# 🏁 **4. Routing Output Format**
Router must output:

```
Task: <summary>
Primary Agent: <agent>
Secondary Agents: <list>
Reasoning: <why>
Subtasks: <if any>
```

---

# 🎯 **5. Guiding Principle**
**Route to the most specialized agent that can fully own the task.**
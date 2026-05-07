# 🧩 Agent Design Handbook
A complete guide for designing, extending, and maintaining agents within the **AI‑Agents Multi‑Agent Engineering System**.

This handbook ensures every agent is:
- consistent  
- predictable  
- collaborative  
- maintainable  
- aligned with system conventions  

Use this document when creating new agents or modifying existing ones.

---

# 🧠 1. Agent Philosophy

Agents are designed around four core principles:

### **1. Single Responsibility**
Each agent owns one domain and performs one category of tasks.

### **2. Deterministic Behavior**
Given the same input, the agent should always produce the same type of output.

### **3. Collaboration Over Autonomy**
Agents are not isolated; they collaborate through orchestration rules.

### **4. Convention‑Driven**
Agents follow shared coding, documentation, and communication conventions.

---

# 🧱 2. Agent Structure

Every agent file follows the same structure:

```
# Agent Name

## Purpose
## Responsibilities
## Inputs
## Outputs
## Operating Rules
## Constraints
## Anti‑Patterns
## Collaboration Patterns
## Escalation Logic
## Example Prompts
## Example Responses
## Edge Cases
## Failure Modes
## Versioning Notes
```

This ensures consistency across all 27+ agents.

---

# 🧩 3. Purpose (What the Agent Is)

The **Purpose** section defines:
- the domain the agent owns  
- the type of problems it solves  
- the boundaries of its responsibility  

A good purpose statement is:
- short  
- domain‑specific  
- unambiguous  

Example:
```
The Architect Agent defines high-level system structure, module boundaries, and integration patterns.
```

---

# 🧠 4. Responsibilities (What the Agent Does)

Responsibilities must be:
- actionable  
- domain‑specific  
- non‑overlapping with other agents  

Example responsibilities:
- “Design module boundaries”  
- “Define API contracts”  
- “Generate acceptance criteria”  

Avoid vague responsibilities like:
- “Help with architecture”  
- “Improve code”  

---

# 🔌 5. Inputs (What the Agent Needs)

Define:
- required inputs  
- optional inputs  
- context expectations  

Examples:
- “Feature description”  
- “Existing architecture”  
- “Code snippet”  

Agents should **never assume** missing context.

---

# 📤 6. Outputs (What the Agent Produces)

Outputs must be:
- structured  
- predictable  
- aligned with templates and conventions  

Examples:
- architecture diagrams  
- code blocks  
- test cases  
- acceptance criteria  

---

# ⚙️ 7. Operating Rules

Operating rules define how the agent behaves.

Examples:
- follow coding-style.md  
- follow project-conventions.md  
- use templates when applicable  
- maintain consistent formatting  

These rules ensure deterministic behavior.

---

# 🚫 8. Constraints (What the Agent Must NOT Do)

Constraints prevent agents from:
- stepping outside their domain  
- duplicating other agents  
- producing inconsistent output  

Examples:
- “Do not write code” (for Strategist)  
- “Do not design architecture” (for Coder)  
- “Do not modify requirements” (for Tester)  

---

# ❌ 9. Anti‑Patterns

Anti‑patterns describe common mistakes the agent must avoid.

Examples:
- mixing high‑level and low‑level detail  
- producing unstructured output  
- ignoring conventions  
- solving tasks outside its domain  

---

# 🔗 10. Collaboration Patterns

Defines how the agent works with others.

Examples:
- Architect → Coder  
- Coder ↔ Reviewer  
- Coder → Tester  
- Strategist → Architect  

Patterns include:
- sequential  
- parallel  
- cyclic  
- multi‑agent pipelines  

---

# 📈 11. Escalation Logic

Escalation ensures tasks are handled by the correct agent.

Examples:
- Coder → Architect (architecture needed)  
- Coder → Security (security concerns)  
- Any agent → Knowledge Curator (documentation needed)  
- Strategist → Requirements (missing details)  

Escalation must be:
- explicit  
- predictable  
- documented  

---

# 💬 12. Example Prompts

Each agent includes example prompts that:
- demonstrate usage  
- clarify boundaries  
- show typical tasks  

Example:
```
Design the high-level architecture for a multi-tenant analytics platform.
```

---

# 📝 13. Example Responses

Example responses show:
- structure  
- formatting  
- conventions  
- tone  

They serve as a reference for expected output quality.

---

# 🧪 14. Edge Cases

Edge cases define how the agent behaves when:
- input is incomplete  
- requirements conflict  
- context is ambiguous  
- multiple domains overlap  

Agents must:
- request clarification  
- escalate appropriately  
- avoid guessing  

---

# 💥 15. Failure Modes

Failure modes describe:
- what can go wrong  
- how the agent should respond  
- how to recover  

Examples:
- missing context  
- invalid input  
- conflicting requirements  
- ambiguous tasks  

---

# 🧬 16. Versioning Notes

Each agent includes:
- version number  
- change history  
- rationale for updates  

This ensures long‑term maintainability.

---

# 🛠️ 17. Creating a New Agent (Step‑By‑Step)

1. Copy:
```
ai-agents/templates/agent-template.md
```

2. Fill in:
- purpose  
- responsibilities  
- inputs/outputs  
- rules  
- constraints  
- collaboration  
- escalation  
- examples  
- edge cases  
- failure modes  

3. Save under:
```
ai-agents/core/   or   ai-agents/extended/
```

4. Update:
- routing rules  
- collaboration patterns  
- escalation matrix  

5. Commit with:
```
feat(agent): add <AgentName> agent
```

---

# 🧭 18. Quality Checklist

Before finalizing an agent:

- [ ] Single responsibility  
- [ ] Clear purpose  
- [ ] Non‑overlapping responsibilities  
- [ ] Structured outputs  
- [ ] Follows conventions  
- [ ] Defined collaboration  
- [ ] Defined escalation  
- [ ] Includes examples  
- [ ] Includes edge cases  
- [ ] Includes failure modes  
- [ ] Versioned  

---

# 🏁 19. Summary

This handbook ensures every agent is:
- well‑designed  
- predictable  
- collaborative  
- maintainable  
- aligned with the system’s architecture  

Use it whenever you create or modify agents to keep the system scalable and consistent.

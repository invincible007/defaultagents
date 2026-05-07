# 🔀 Agent Routing Rules
Defines how tasks should be routed to the correct agent.

---

## 🧭 1. Routing Philosophy
Routing must be:
- Deterministic  
- Minimal  
- Composable  
- Escalation‑aware  

---

## 🧩 2. Routing Decision Tree

### Step 1 — Identify Intent
Map user intent → agent (see system-behavior.md).

### Step 2 — Multi‑Intent Tasks
If a task spans multiple domains:
- Decompose  
- Route each sub‑task  
- Aggregate results  

### Step 3 — Escalation
Escalate to:
- Strategist → unclear requirements  
- Architect → unclear system boundaries  
- Security → sensitive logic  
- Ops → deployment/infra issues  

---

## 🧱 3. Routing Output Format
```
Task: <summary>
Primary Agent: <agent>
Secondary Agents: <list>
Reasoning: <why>
Subtasks: <if any>
```

---

## 🎯 4. Guiding Principle
Route to the **most specialized agent** that can fully own the task.

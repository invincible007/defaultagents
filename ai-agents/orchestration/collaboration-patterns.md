# 🤝 **Agent Collaboration Patterns**
Defines how agents work together on multi‑step tasks.

---

# 🧩 **1. Core Collaboration Loops**

## **A. Architecture → Coding → Review → Testing**
Used for most feature implementations.

Flow:
1. Architect defines structure  
2. Coder implements  
3. Reviewer validates  
4. Tester ensures correctness  

---

## **B. Strategy → Architecture → Project Management**
Used for new features or unclear requirements.

Flow:
1. Strategist clarifies scope  
2. Architect designs  
3. Project Manager breaks into tasks  

---

## **C. Research → Strategy → Architecture**
Used for technology decisions.

Flow:
1. Researcher compares options  
2. Strategist aligns with goals  
3. Architect finalizes design  

---

## **D. UX → Architecture → Coding**
Used for UI/UX‑heavy features.

Flow:
1. UX/UI proposes flows  
2. Architect integrates into system  
3. Coder implements  

---

# 🔄 **2. Extended Collaboration Loops**

## **E. Refactor → Architect → Coder → Tester**
Used for modernization.

## **F. Performance → Coder → Ops**
Used for optimization.

## **G. Security → Coder → Ops → Tester**
Used for sensitive logic.

## **H. Release → Ops → Project Manager**
Used for deployment cycles.

---

# 🧠 **3. Collaboration Rules**
- Each agent must **only** operate within its domain  
- Handoffs must be explicit  
- No agent overrides another’s domain  
- Conflicts escalate to Strategist or Architect  

---

# 📦 **4. Handoff Format**
Each handoff must include:

```
Context:
Decisions:
Constraints:
Open Questions:
Next Agent:
```

---

# 🏁 **5. Collaboration Principle**
**Agents collaborate like a real engineering team — each with a clear domain and boundaries.**
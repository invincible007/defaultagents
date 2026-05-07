# 🧠 **Context Loading Guidelines**
Defines how agents load, share, and maintain context across tasks.

---

# 📦 **1. Types of Context**

## **A. Local Context**
- File being edited  
- Current task  
- Recent messages  

## **B. Project Context**
- Architecture  
- API contracts  
- Data models  
- Coding conventions  

## **C. Historical Context**
- Decisions  
- Meeting notes  
- Knowledge base entries  

---

# 🔄 **2. Context Flow Between Agents**

| From | To | Purpose |
|------|----|---------|
| Strategist | Architect | Requirements & priorities |
| Architect | Coder | System design |
| Coder | Reviewer | Code correctness |
| Reviewer | Tester | Edge cases |
| Meeting Companion | Knowledge Curator | Decisions |
| Researcher | Strategist | Options & trade‑offs |

---

# 🧩 **3. Context Loading Rules**
- Load **only** the context needed for your domain  
- Do not duplicate context  
- Do not override decisions from higher‑level agents  
- Always reference the source of context  

---

# 📝 **4. Context Packet Format**
Each agent must pass context in this structure:

```
Summary:
Decisions:
Constraints:
Dependencies:
Risks:
Next Agent:
```

---

# 🎯 **5. Guiding Principle**
**Context must flow like a pipeline — clean, structured, and minimal.**
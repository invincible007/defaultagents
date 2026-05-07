# 👋 Developer Onboarding Guide
Welcome to the **AI‑Agents Multi‑Agent Engineering System**.  
This guide helps new developers understand the system quickly and become productive within minutes.

---

# 🚀 1. What This System Is
This repository contains a **complete, tool‑agnostic multi‑agent framework** designed to enhance software engineering workflows.

It provides:
- 27 specialized engineering agents  
- A full orchestration layer  
- Universal behavior and routing rules  
- Coding and project conventions  
- Templates for structured work  
- Visual diagrams for system understanding  

The system works with:
- GitHub Copilot  
- Continue.dev  
- Cursor  
- Windsurf  
- LM Studio  
- ChatGPT  
- Claude Desktop  
- Any future AI tool  

---

# 🧠 2. How the System Works (High‑Level)
The system is built from four layers:

### **1. Instruction Layer**
Defines global behavior, routing rules, coding conventions, and project conventions.

### **2. Orchestration Layer**
Controls:
- agent selection  
- collaboration patterns  
- escalation logic  
- context flow  

### **3. Agent Layer**
27 specialized agents with clear roles and responsibilities.

### **4. Templates & Knowledge Layer**
Reusable structures for tickets, documentation, meetings, and knowledge entries.

Visual diagrams are available in:

```
ai-agents/diagram/
```

---

# ⚙️ 3. Repository Structure

```
ai-agents/
  core/               # Core agents (18)
  extended/           # Extended agents (9)
  orchestration/      # Routing, collaboration, escalation rules
  instructions/       # Behavior, conventions, master loader
  templates/          # Tickets, KB entries, meetings, agent template
  diagram/            # Excalidraw diagrams
  QUICKSTART.md       # Quick usage guide
  DEVELOPER-ONBOARDING.md  # This file
```

---

# 🚀 4. Getting Started (First 2 Minutes)

### **Step 1 — Load the System**
In your AI tool, paste:

```
Load the multi-agent system from ai-agents/instructions/master-instructions.md
```

### **Step 2 — Try a Simple Command**
```
Break down this feature into tasks and acceptance criteria.
```

### **Step 3 — Call a Specific Agent**
```
@Architect
Design the high-level architecture for the new billing module.
```

You’re now fully operational.

---

# 🧩 5. How to Work With Agents

### **Auto‑Routing**
Just describe your task:

```
Refactor this module for readability.
```

The system selects the correct agent automatically.

### **Explicit Invocation**
```
@Coder
Implement the service layer using the project conventions.
```

### **Multi‑Agent Workflow**
```
1. Clarify requirements.
2. Design the architecture.
3. Generate acceptance criteria.
4. Provide test cases.
```

The system orchestrates the agents in sequence.

---

# 📁 6. Using Templates

Templates live in:

```
ai-agents/templates/
```

Available templates:
- agent-template.md  
- ticket-template.md  
- knowledge-base-entry-template.md  
- meeting-minutes-template.md  

Example:
```
Use the ticket template to create a new ticket for the authentication module.
```

---

# 🧱 7. Coding & Project Conventions

All conventions live in:

```
ai-agents/instructions/
```

Includes:
- coding-style.md  
- project-conventions.md  
- agent-routing.md  
- system-behavior.md  
- custom-instructions.md  
- master-instructions.md  

Always reference these when writing code or documentation.

---

# 🧩 8. Creating a New Agent

1. Copy:
```
ai-agents/templates/agent-template.md
```

2. Fill in:
- role  
- responsibilities  
- constraints  
- collaboration rules  
- activation triggers  

3. Save under:
```
ai-agents/core/   or   ai-agents/extended/
```

The system will load it automatically.

---

# 🖼️ 9. Understanding the System Visually

Diagrams are located in:

```
ai-agents/diagram/
```

Includes:
- High‑Level Diagram  
- Medium Detail Diagram  
- Full Detail Diagram  

Use these to understand:
- agent relationships  
- orchestration flows  
- escalation paths  
- system boundaries  

---

# 🧭 10. Best Practices for Developers

- Keep tasks small and focused  
- Use explicit agents for precision  
- Use auto‑routing for speed  
- Reference conventions for consistency  
- Use templates for structured outputs  
- Use diagrams for architectural clarity  
- Commit new agents or rules with documentation  

---

# 🏁 11. Summary

You now have:
- a full engineering team  
- consistent workflows  
- reusable patterns  
- tool‑agnostic behavior  
- clear documentation  
- visual diagrams  

This system is designed to scale with your team and your projects.

Welcome aboard.

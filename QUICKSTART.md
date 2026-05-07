# 🚀 AI‑Agents Quick Start Guide
A fast, practical guide to using the multi‑agent engineering system.

This guide teaches you how to:
- load the system  
- call agents  
- run multi‑agent workflows  
- use templates  
- extend the system  
- integrate with AI tools  

Anyone can get productive in minutes.

---

# 🧠 1. Load the Multi‑Agent System
In ANY AI tool (Copilot, Continue.dev, Cursor, LM Studio, ChatGPT, Claude, etc.), paste:

```
Load the multi-agent system from ai-agents/instructions/master-instructions.md
```

This loads:
- foundational behavior  
- operational behavior  
- routing logic  
- all 27 agents  
- orchestration rules  
- coding conventions  
- project conventions  

Your AI tool now behaves like a **full engineering team**.

---

# 🎯 2. How to Use the System

## A) Natural Language (Auto‑Routing)
Just describe what you want:

```
Break down this feature into tasks and acceptance criteria.
```

The system will:
- detect intent  
- select the correct agent  
- escalate if needed  
- maintain consistency  

---

## B) Explicit Agent Invocation
Call a specific agent:

```
@Architect
Design the high-level architecture for a multi-tenant analytics platform.
```

Or:

```
@Coder
Implement the controller using the conventions in project-conventions.md.
```

---

## C) Multi‑Agent Workflow
Ask for a coordinated sequence:

```
1. Break this feature into tasks.
2. Design the architecture.
3. Generate acceptance criteria.
4. Provide test cases.
```

The system orchestrates the agents in the correct order.

---

# 🧩 3. Common Agent Commands

### Architecture
```
@Architect
Design the module boundaries for the new billing system.
```

### Coding
```
@Coder
Generate the service layer using the project conventions.
```

### Refactoring
```
@Refactor
Improve readability and reduce complexity in this file.
```

### Testing
```
@Tester
Write unit tests for this service.
```

### Planning
```
@Strategist
Clarify requirements and identify missing details.
```

### Documentation
```
@KnowledgeCurator
Document this module using the KB template.
```

---

# 📁 4. Using Templates
Templates live in:

```
ai-agents/templates/
```

Available templates:
- agent-template.md  
- ticket-template.md  
- knowledge-base-entry-template.md  
- meeting-minutes-template.md  

### Example
```
Use the ticket template to create a new ticket for the authentication module.
```

---

# 🧱 5. Repository Awareness
The system understands:

```
ai-agents/core/
ai-agents/extended/
ai-agents/orchestration/
ai-agents/instructions/
ai-agents/templates/
```

You can reference files directly:

```
Use the conventions from ai-agents/instructions/coding-style.md
```

Or:

```
Follow the escalation rules in ai-agents/orchestration/escalation-matrix.md
```

---

# 🔀 6. Creating a New Agent

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

The system will load it automatically next time.

---

# 🧭 7. Best Practices
- Keep tasks small and focused  
- Use explicit agents for precision  
- Use auto‑routing for speed  
- Reference conventions to maintain consistency  
- Use templates for structured outputs  
- Use diagrams for system understanding  

---

# 🖼️ 8. Visual Architecture
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

# 🏁 9. Summary
This system gives you:
- a full engineering team  
- consistent outputs  
- structured workflows  
- reusable patterns  
- tool‑agnostic behavior  

Load it once, and every AI tool becomes a **multi‑agent engineering assistant**.

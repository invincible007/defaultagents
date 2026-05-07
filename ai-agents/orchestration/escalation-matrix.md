# ⚠️ **Escalation Matrix**
Defines when and how agents escalate tasks to higher‑level agents.

---

# 🧭 **1. Escalation Philosophy**
Escalation is required when:
- Requirements unclear  
- Conflicts between agents  
- Cross‑domain decisions needed  
- Risks exceed agent authority  

---

# 🧱 **2. Escalation Levels**

| Level | Escalate To | When |
|------|-------------|------|
| L1 | Strategist | Requirements unclear, scope issues |
| L2 | Architect | System design, cross‑module impact |
| L3 | Security | Sensitive logic, vulnerabilities |
| L4 | Ops | Deployment, infra, CI/CD issues |
| L5 | Project Manager | Timeline, coordination issues |

---

# 🧩 **3. Escalation Triggers**

## **A. Strategist Escalation**
Triggered when:
- User intent unclear  
- Conflicting requirements  
- Missing priorities  

## **B. Architect Escalation**
Triggered when:
- Architecture needed  
- System boundaries unclear  
- Multi‑service impact  

## **C. Security Escalation**
Triggered when:
- Sensitive data  
- Auth/crypto logic  
- Potential vulnerabilities  

## **D. Ops Escalation**
Triggered when:
- Deployment blockers  
- CI/CD failures  
- Infra constraints  

## **E. Project Manager Escalation**
Triggered when:
- Timeline issues  
- Resource conflicts  
- Multi‑agent coordination needed  

---

# 📝 **4. Escalation Output Format**
```
Issue:
Trigger:
Escalated To:
Reason:
Proposed Next Steps:
```

---

# 🎯 **5. Guiding Principle**
**Escalate early, escalate clearly, escalate with context.**
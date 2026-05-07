# 📁 Project Conventions
Defines naming, folder structure, and architectural patterns.

---

## 🧱 1. Folder Structure
Recommended baseline:

```
src/
  modules/
  services/
  utils/
  api/
  domain/
tests/
ai-agents/
  core/
  extended/
  orchestration/
  templates/
  instructions/
```

---

## 🧩 2. Naming Conventions
- Files: `kebab-case`
- Classes: `PascalCase`
- Functions: `camelCase`
- Constants: `UPPER_SNAKE_CASE`
- Types/interfaces: `PascalCase`

---

## 🧠 3. Architectural Patterns
- Prefer modular architecture.
- Keep domain logic isolated.
- Avoid circular dependencies.
- Use dependency injection where appropriate.

---

## 🔄 4. Versioning & Change Management
- Use semantic versioning.
- Document breaking changes.
- Maintain changelogs.

---

## 🎯 5. Guiding Principle
Consistency > Preference.

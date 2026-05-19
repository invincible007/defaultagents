# Output Artifact Standard

## Purpose
Define standard locations and update rules for agent outputs so project documentation evolves progressively during delivery.

## Core Rules
- Persist durable outputs under docs/ using the mapped folder.
- Use one file per work item slug and append updates over time.
- Use date-stamped section headers for each update.
- Keep prior decisions as history; supersede with explicit notes instead of deleting context.

## Work Item Slug
- Required for all persisted artifacts.
- Format: kebab-case, short and stable.
- Example: checkout-v2

## Path Mapping
- Strategist -> docs/strategy/<work-item>.md
- UX/UI Design -> docs/ux/<work-item>.md
- User Story & Acceptance Criteria -> docs/requirements/<work-item>.md
- Architect -> docs/architecture/<work-item>.md
- Data & API Contract -> docs/api/<work-item>.md
- Project Manager -> docs/planning/<work-item>.md
- Tester -> docs/testing/<work-item>.md
- Reviewer -> docs/reviews/<work-item>.md
- Security -> docs/security/<work-item>.md
- Compliance & Governance -> docs/compliance/<work-item>.md
- Performance & Profiling -> docs/performance/<work-item>.md
- Ops -> docs/operations/<work-item>.md
- Release & Deployment -> docs/release/<work-item>.md
- Documentation -> docs/documentation/<work-item>.md
- Knowledge Curator -> docs/knowledge/<work-item>.md

## Update Mode
- create: first artifact for a work item in that folder.
- append: all subsequent updates to preserve progressive history.

## Minimum Artifact Header
Each artifact should begin with:
- Title
- Work item slug
- Agent
- Date
- Status (draft/approved/superseded)

## Suggested Section Header Style
## YYYY-MM-DD - <short update title>

## Router Requirement
Router should always include:
- artifact target path
- artifact type
- update mode
before asking for approval on a step.

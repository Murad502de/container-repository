# Specs

This folder stores project-level requirements, system design, and technical design documents.

## Purpose

Specs document what the system must do, how a solution is designed, and how implementation should proceed when the scope is project-wide or cross-direction.

## What Belongs Here

- Project-level or cross-direction requirements.
- Project-level or cross-direction system designs.
- Project-level or cross-direction technical designs when truly needed.

## What Does Not Belong Here

- Service-only specs. Put them in the owning source repository.
- ADRs. Put decisions in [../adr](../adr/README.md).
- API/event/integration contracts. Put them in [../contracts](../contracts/README.md).

## Index

| Folder | Purpose |
| --- | --- |
| [requirements](requirements/README.md) | Requirements and acceptance criteria. |
| [system-design](system-design/README.md) | System-level solution designs. |
| [technical-design](technical-design/README.md) | Implementation plans. |

## Templates

- [requirements-template.md](../templates/requirements-template.md)
- [system-design-template.md](../templates/system-design-template.md)
- [technical-design-template.md](../templates/technical-design-template.md)

## Maintenance Rules

- Keep requirements, system design, and technical design separate.
- Link related ADRs, contracts, diagrams, and open questions.
- Do not use specs to duplicate business context or architecture.

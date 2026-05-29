# Specs

This folder stores requirements, system design, and technical design documents owned by this container boundary.

## Purpose

Specs document what this boundary must do, how a solution is designed, and how implementation should proceed when the scope belongs to this container.

## What Belongs Here

- Requirements owned by this container boundary.
- System designs owned by this container boundary.
- Technical designs owned by this container boundary when truly needed.

## What Does Not Belong Here

- Parent-owned or child-owned specs. Put them in the owning repository.
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
- Link contract-impact analysis when specs affect public contracts.
- Do not use specs to duplicate business context or architecture.

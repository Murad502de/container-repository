# Architecture Decision Records

This folder stores project-level Architecture Decision Records.

## Purpose

ADRs record accepted, proposed, rejected, or superseded architecture decisions that apply at the container/project level.

## What Belongs Here

- Project-wide architecture decisions.
- Cross-direction or cross-service decisions.
- Decisions that affect shared contracts, boundaries, security, data ownership, or operational principles.

## What Does Not Belong Here

- Direction-specific or service-specific decisions. Put them in the owning repository's `docs/adr`.
- Open questions. Put them in [open-questions.md](../open-questions.md).
- Full architecture documentation. Put it in [architecture.md](../architecture.md).

## Index

| Path | Purpose |
| --- | --- |
| [ADR-0001-example.md](ADR-0001-example.md) | Example ADR format; not a real project decision. |

## Template

Use [adr-template.md](../templates/adr-template.md) for new ADRs.

## Maintenance Rules

- Keep one decision per ADR.
- Link related architecture, contracts, diagrams, requirements, and open questions.
- When an open question is resolved by an ADR, update [open-questions.md](../open-questions.md) with the ADR link.

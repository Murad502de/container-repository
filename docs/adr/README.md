# Architecture Decision Records

This folder stores Architecture Decision Records owned by this container boundary.

## Purpose

ADRs record accepted, proposed, rejected, or superseded architecture decisions that apply to this container boundary.

## What Belongs Here

- Architecture decisions owned by this container boundary.
- Cross-child or cross-boundary decisions.
- Decisions that affect shared contracts, boundaries, security, data ownership, or operational principles.

## What Does Not Belong Here

- Parent-owned or child-owned decisions. Put them in the owning repository's `docs/adr`.
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
- Link contract-impact analysis when a decision changes public contracts.
- When an open question is resolved by an ADR, update [open-questions.md](../open-questions.md) with the ADR link.

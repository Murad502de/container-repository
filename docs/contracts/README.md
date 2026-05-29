# Contracts

This folder stores project-level API, event, and integration contracts.

## Purpose

Contracts define agreements at system boundaries. They are source-of-truth documents for interface behavior, not implementation plans.

## What Belongs Here

- Project-level or cross-direction API contracts.
- Project-level or cross-direction event contracts.
- Project-level or cross-direction integration contracts.
- Shared contract standards that affect multiple repositories.

## What Does Not Belong Here

- Service-only contracts. Put them in the owning source repository.
- High-level integration summaries. Put them in [integration-map.md](../integration-map.md).
- Implementation plans. Put them in [technical design specs](../specs/technical-design/README.md).

## Index

| Folder | Purpose |
| --- | --- |
| [api](api/README.md) | HTTP/API contracts. |
| [events](events/README.md) | Event contracts. |
| [integrations](integrations/README.md) | Integration agreements with external or internal systems. |

## Templates

- [api-contract-template.md](../templates/api-contract-template.md)
- [event-contract-template.md](../templates/event-contract-template.md)
- [integration-contract-template.md](../templates/integration-contract-template.md)

## Maintenance Rules

- Keep detailed payloads and behavior in contracts, not in integration maps.
- Link related requirements, designs, ADRs, and diagrams.
- Mark contract status clearly.

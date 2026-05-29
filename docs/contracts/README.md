# Contracts

This folder stores API, event, and integration contracts owned by this container boundary.

## Purpose

Contracts define agreements at system boundaries. They are source-of-truth documents for interface behavior, not implementation plans.

## What Belongs Here

- API contracts owned by this container boundary.
- Event contracts owned by this container boundary.
- Integration contracts owned by this container boundary.
- Shared contract standards that affect direct child repositories.

## What Does Not Belong Here

- Parent-owned or child-owned contracts. Put them in the owning repository.
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
- Declare contract scope and registry ownership according to [contract impact](../contract-impact.md).
- Link related requirements, designs, ADRs, and diagrams.
- Mark contract status clearly.

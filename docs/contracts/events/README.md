# Event Contracts

This folder stores event contract documents owned by this container boundary.

## What Belongs Here

- Event contracts owned by this container boundary.
- Event payload schemas, producers, consumers, delivery guarantees, and compatibility rules shared across repositories.

## What Does Not Belong Here

- HTTP/API contracts. Use [../api](../api/README.md).
- Integration-wide agreements. Use [../integrations](../integrations/README.md).
- Parent-owned or child-owned event contracts. Put them in the owning repository.

## Template

Use [event-contract-template.md](../../templates/event-contract-template.md).

## Related Documents

- [Contracts index](../README.md)
- [Contract registry](../registry.md)
- [Integration map](../../integration-map.md)
- [Contract impact model](../../contract-impact.md)
- [Architecture](../../architecture.md)

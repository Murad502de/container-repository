# Event Contracts

This folder stores project-level event contract documents.

## What Belongs Here

- Project-level or cross-direction events.
- Event payload schemas, producers, consumers, delivery guarantees, and compatibility rules shared across repositories.

## What Does Not Belong Here

- HTTP/API contracts. Use [../api](../api/README.md).
- Integration-wide agreements. Use [../integrations](../integrations/README.md).
- Service-only event contracts. Put them in the owning source repository.

## Template

Use [event-contract-template.md](../../templates/event-contract-template.md).

## Related Documents

- [Contracts index](../README.md)
- [Integration map](../../integration-map.md)
- [Architecture](../../architecture.md)

# Integration Contracts

This folder stores integration agreements owned by this container boundary.

## What Belongs Here

- Agreements with external systems owned by this container boundary.
- Cross-child or cross-boundary internal system agreements.
- Auth, environments, data exchange, quotas, error handling, and ownership for shared integrations.

## What Does Not Belong Here

- High-level integration summaries. Use [integration-map.md](../../integration-map.md).
- Single API endpoint contracts. Use [../api](../api/README.md).
- Single event payload contracts. Use [../events](../events/README.md).
- Parent-owned or child-owned integration contracts. Put them in the owning repository.

## Template

Use [integration-contract-template.md](../../templates/integration-contract-template.md).

## Related Documents

- [Contracts index](../README.md)
- [Contract registry](../registry.md)
- [Integration map](../../integration-map.md)
- [Contract impact model](../../contract-impact.md)
- [Architecture](../../architecture.md)

# Integration Contracts

This folder stores project-level integration agreements.

## What Belongs Here

- Project-level agreements with external systems.
- Cross-direction or cross-service internal system agreements.
- Auth, environments, data exchange, quotas, error handling, and ownership for shared integrations.

## What Does Not Belong Here

- High-level integration summaries. Use [integration-map.md](../../integration-map.md).
- Single API endpoint contracts. Use [../api](../api/README.md).
- Single event payload contracts. Use [../events](../events/README.md).
- Service-only integration contracts. Put them in the owning source repository.

## Template

Use [integration-contract-template.md](../../templates/integration-contract-template.md).

## Related Documents

- [Contracts index](../README.md)
- [Integration map](../../integration-map.md)
- [Architecture](../../architecture.md)

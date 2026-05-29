# API Contracts

This folder stores project-level HTTP/API contract documents.

## What Belongs Here

- Project-level or cross-direction API contracts.
- Stable request/response behavior at shared system boundaries.
- API standards shared by multiple repositories.

## What Does Not Belong Here

- Event schemas. Use [../events](../events/README.md).
- External integration agreements. Use [../integrations](../integrations/README.md).
- Service-only API contracts. Put them in the owning source repository.

## Template

Use [api-contract-template.md](../../templates/api-contract-template.md).

## Related Documents

- [Contracts index](../README.md)
- [Integration map](../../integration-map.md)
- [Architecture](../../architecture.md)

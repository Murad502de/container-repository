# API Contracts

This folder stores HTTP/API contract documents owned by this container boundary.

## What Belongs Here

- API contracts owned by this container boundary.
- Stable request/response behavior at shared system boundaries.
- API standards shared by direct child repositories.

## What Does Not Belong Here

- Event schemas. Use [../events](../events/README.md).
- External integration agreements. Use [../integrations](../integrations/README.md).
- Parent-owned or child-owned API contracts. Put them in the owning repository.

## Template

Use [api-contract-template.md](../../templates/api-contract-template.md).

## Related Documents

- [Contracts index](../README.md)
- [Contract registry](../registry.md)
- [Integration map](../../integration-map.md)
- [Contract impact model](../../contract-impact.md)
- [Architecture](../../architecture.md)

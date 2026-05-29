# Documentation

This folder contains engineering memory for `<container-name>`.

Use this README as the documentation navigation hub. It should help humans and AI agents find the right source document without turning this folder into a duplicate knowledge base.

## Responsibility

This folder is responsible for:

- current container context and responsibility boundary;
- documentation model, operational model, AI collaboration model, and working principles;
- current state, architecture, integration maps, data model, glossary, open questions, ADRs, contracts, diagrams, specs, archive, and templates owned by this container;
- routes to parent or child repository documentation when the topic belongs outside this boundary.

This folder is not responsible for:

- implementation details owned by a child repository;
- documenting all descendants at arbitrary depth;
- duplicating parent or child repository documentation.

## Recommended Reading Route

1. [AI collaboration model](ai-collaboration.md)
2. [Operational model](operational-model.md)
3. [Documentation model](documentation-model.md)
4. [Working principles](working-principles.md)
5. [Task format](task-format.md)
6. [Repository relationships](repository-relationships.md)
7. [Contract impact model](contract-impact.md)
8. [Technology stack](technology-stack.md)
9. [System overview](system-overview.md)
10. [Business context](business-context.md)
11. [Architecture](architecture.md)
12. [Integration map](integration-map.md)
13. [Data model](data-model.md)
14. [Open questions](open-questions.md)
15. [Repositories index](../repositories/README.md)

## Document Index

| Document | Responsibility |
| --- | --- |
| [ai-collaboration.md](ai-collaboration.md) | Rules for AI-assisted work and context recovery. |
| [operational-model.md](operational-model.md) | Roles, workflow, decision-making, execution, handoff, acceptance, and documentation impact rules. |
| [documentation-model.md](documentation-model.md) | Responsibility boundaries, ownership, links, and anti-duplication rules. |
| [working-principles.md](working-principles.md) | Stable principles for future work in this container. |
| [task-format.md](task-format.md) | Required structure for formal work requests. |
| [repository-relationships.md](repository-relationships.md) | Parent-child repository relationships for self-nesting containers. |
| [contract-impact.md](contract-impact.md) | Contract-based impact analysis model. |
| [technology-stack.md](technology-stack.md) | Stack-agnostic documentation rules and technology stack ownership. |
| [current-state.md](current-state.md) | Observed facts and constraints for this container boundary. |
| [system-overview.md](system-overview.md) | Short orientation to this container boundary. |
| [business-context.md](business-context.md) | Business goals, actors, scenarios, and constraints relevant to this container. |
| [architecture.md](architecture.md) | Target architecture for this container boundary when defined. |
| [integration-map.md](integration-map.md) | Integration map with links to contracts. |
| [data-model.md](data-model.md) | Domain data model and ownership within this container boundary. |
| [glossary.md](glossary.md) | Terms and definitions owned by this container. |
| [open-questions.md](open-questions.md) | Unresolved questions owned by this container. |

## Folder Index

| Folder | Responsibility |
| --- | --- |
| [adr](adr/README.md) | Architecture Decision Records owned by this container. |
| [contracts](contracts/README.md) | API, event, and integration contracts owned by this container. |
| [diagrams](diagrams/README.md) | Visual documentation that supports source documents. |
| [specs](specs/README.md) | Requirements, system design, and technical design documents. |
| [templates](templates/README.md) | Local documentation templates and writing standards. |
| [archive](archive/README.md) | Historical material that is not current source of truth. |

## Related Boundaries

- Container root: [../README.md](../README.md)
- Child repositories index: [../repositories/README.md](../repositories/README.md)

## Working Rules

- Keep this README as a navigation hub.
- Put detailed knowledge into focused documents.
- Link to related documents instead of copying their content.
- Keep knowledge at the nearest container boundary that owns it.
- Use [templates](templates/README.md) when creating or normalizing documents.

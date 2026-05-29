# Documentation

This folder contains project-level engineering memory for `<project-name>`.

Use this README as the documentation navigation hub. It should help humans and AI agents find the right source document without turning this folder into a duplicate knowledge base.

## Responsibility

This folder is responsible for:

- project-wide and system-wide context;
- documentation model, operational model, AI collaboration model, and working principles;
- project-level current state, architecture, integration maps, data model, glossary, open questions, ADRs, contracts, diagrams, specs, archive, and templates;
- routes to direction-level or service-level documentation when the topic becomes more specific.

This folder is not responsible for:

- concrete service implementation details;
- source code;
- duplicating direction-level or service-level documentation.

## Recommended Reading Route

1. [AI collaboration model](ai-collaboration.md)
2. [Operational model](operational-model.md)
3. [Documentation model](documentation-model.md)
4. [Working principles](working-principles.md)
5. [Task format](task-format.md)
6. [Repository pairing](repository-pairing.md)
7. [Technology stack](technology-stack.md)
8. [System overview](system-overview.md)
9. [Business context](business-context.md)
10. [Architecture](architecture.md)
11. [Integration map](integration-map.md)
12. [Data model](data-model.md)
13. [Open questions](open-questions.md)
14. [Services index](../services/README.md)

## Document Index

| Document | Responsibility |
| --- | --- |
| [ai-collaboration.md](ai-collaboration.md) | Rules for AI-assisted work and context recovery. |
| [operational-model.md](operational-model.md) | Roles, workflow, decision-making, execution, handoff, acceptance, and documentation impact rules. |
| [documentation-model.md](documentation-model.md) | Documentation levels, ownership, links, and anti-duplication rules. |
| [working-principles.md](working-principles.md) | Stable principles for future work in this project. |
| [task-format.md](task-format.md) | Required structure for formal work requests. |
| [repository-pairing.md](repository-pairing.md) | Rules for linking container and source repositories. |
| [technology-stack.md](technology-stack.md) | Stack-agnostic documentation rules and technology stack ownership. |
| [current-state.md](current-state.md) | Project-level observed facts and constraints. |
| [system-overview.md](system-overview.md) | Short project/system orientation. |
| [business-context.md](business-context.md) | Project-wide business goals, actors, scenarios, and constraints. |
| [architecture.md](architecture.md) | Project-level target architecture when defined. |
| [integration-map.md](integration-map.md) | Project-level integration map with links to contracts. |
| [data-model.md](data-model.md) | Project-level domain data model and ownership. |
| [glossary.md](glossary.md) | Project-wide terms and definitions. |
| [open-questions.md](open-questions.md) | Project-level unresolved questions. |

## Folder Index

| Folder | Responsibility |
| --- | --- |
| [adr](adr/README.md) | Project-level Architecture Decision Records. |
| [contracts](contracts/README.md) | Project-level API, event, and integration contracts. |
| [diagrams](diagrams/README.md) | Visual documentation that supports source documents. |
| [specs](specs/README.md) | Requirements, system design, and technical design documents. |
| [templates](templates/README.md) | Local documentation templates and writing standards. |
| [archive](archive/README.md) | Historical material that is not current source of truth. |

## Related Levels

- Container root: [../README.md](../README.md)
- Services index: [../services/README.md](../services/README.md)

## Working Rules

- Keep this README as a navigation hub.
- Put detailed knowledge into focused documents.
- Link to related documents instead of copying their content.
- Keep project-wide context here; move direction or service details to the owning repository.
- Use [templates](templates/README.md) when creating or normalizing documents.

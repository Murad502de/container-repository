# Templates

This folder stores reusable Markdown templates for engineering documentation.

Templates are part of the documentation environment. They define how humans and AI agents should create or normalize project memory.

## Purpose

- Keep document types consistent across repositories.
- Make each document's responsibility clear before content is added.
- Prevent duplication by routing knowledge to its source document.
- Keep repositories reusable while preserving a shared documentation model.

## Template Set

| Template | Use for |
| --- | --- |
| [readme-template.md](readme-template.md) | Repository README files as navigation hubs. |
| [folder-readme-template.md](folder-readme-template.md) | Folder README files and indexes. |
| [documentation-model-template.md](documentation-model-template.md) | Documentation levels, ownership, links, and anti-duplication rules. |
| [operational-model-template.md](operational-model-template.md) | Roles, workflow, decision-making, handoff, and documentation impact. |
| [ai-collaboration-template.md](ai-collaboration-template.md) | Rules for AI-assisted work and context recovery. |
| [working-principles-template.md](working-principles-template.md) | Stable project principles. |
| [task-format-template.md](task-format-template.md) | Formal task description format. |
| [repository-pairing-template.md](repository-pairing-template.md) | Container/source repository pairing rules. |
| [technology-stack-template.md](technology-stack-template.md) | Stack-agnostic technology documentation. |
| [current-state-template.md](current-state-template.md) | Observed current state and existing facts. |
| [system-overview-template.md](system-overview-template.md) | Short orientation to a project, direction, or service. |
| [business-context-template.md](business-context-template.md) | Business goals, scenarios, stakeholders, and constraints. |
| [architecture-template.md](architecture-template.md) | Target architecture at a specific responsibility level. |
| [integration-map-template.md](integration-map-template.md) | High-level integration maps with links to contracts. |
| [data-model-template.md](data-model-template.md) | Domain entities, relationships, ownership, and lifecycle. |
| [glossary-template.md](glossary-template.md) | Shared vocabulary and term definitions. |
| [open-questions-template.md](open-questions-template.md) | Managed unresolved questions. |
| [adr-template.md](adr-template.md) | Architecture Decision Records. |
| [api-contract-template.md](api-contract-template.md) | HTTP/API contracts. |
| [event-contract-template.md](event-contract-template.md) | Event contracts. |
| [integration-contract-template.md](integration-contract-template.md) | External or internal integration agreements. |
| [requirements-template.md](requirements-template.md) | Requirements and acceptance criteria. |
| [system-design-template.md](system-design-template.md) | Component-level solution design. |
| [technical-design-template.md](technical-design-template.md) | Implementation planning. |
| [diagram-template.md](diagram-template.md) | Mermaid and architecture diagram documentation. |
| [archive-readme-template.md](archive-readme-template.md) | Archive README files. |

## Anti-Duplication Rules

- Every document has one primary responsibility.
- Do not duplicate knowledge that has a dedicated source document.
- Use links to related documents instead of copying content.
- README files are navigation hubs.
- Open questions belong in `open-questions.md`.
- Accepted architecture decisions belong in ADR files.
- Terms belong in `glossary.md`.
- API, event, and integration agreements belong in `docs/contracts`.
- Architecture can summarize decisions but must link to ADRs.
- Integration maps can summarize integrations but must link to contracts.
- Requirements can link to design docs but must not include implementation design.
- If a section starts duplicating another document, replace it with a short summary and a link.

## Related Documents Section

Use `Related Documents` sections only for links to source documents.

Do not duplicate content from linked documents.

## Repository Autonomy

Direction and service repositories should keep their own local copies of these templates so they remain usable when opened outside the container repository.

When templates are updated in one template repository, synchronize the same template names and core rules across related template repositories.

## Maintenance Rules

- Add a template when a new recurring document type is introduced.
- Update this index when templates are added, removed, or renamed.
- Keep template guidance practical and specific to the document type.
- Do not use templates to invent project architecture, APIs, domain model, or implementation details.

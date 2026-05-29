# Documentation Model

This document defines how documentation is organized inside a self-nesting repository container.

Documentation structure and responsibility boundaries are governed together with the [operational model](operational-model.md). Operational roles, workflows, decision-making, execution, handoff, acceptance, and documentation impact are defined there.

This document focuses on ownership boundaries, links, document responsibility, and anti-duplication rules.

## Goal

Documentation should be readable by humans, useful to AI agents, and ready for future retrieval-based workflows.

The documentation should be structured enough to recover local container context without relying on a single chat thread or one person's memory.

## README Files Are Hubs

Every README is a navigation hub for its own responsibility boundary.

A README should contain:

- a short description of the repository, folder, or boundary;
- its responsibility boundary;
- links to the most important documents;
- the recommended reading route for that boundary;
- pointers to parent or child repository READMEs when the context belongs elsewhere.

A README should not contain every detail. If content grows too large, move it into a focused document and link to it.

## Single Source Of Truth

Container documentation is a connected network of source documents, not a set of duplicated summaries.

Every document has one primary responsibility. If another document already owns a type of knowledge, link to it instead of copying it.

Core rules:

- Do not duplicate knowledge that has a dedicated source document.
- Use links to related documents instead of copying content.
- README files are navigation hubs.
- Open questions belong in the nearest relevant `open-questions.md`.
- Accepted architecture decisions belong in ADR files.
- Terms belong in the nearest relevant `glossary.md`.
- API, event, and integration agreements belong in `docs/contracts`.
- Architecture can summarize decisions but must link to ADRs.
- Integration maps can summarize integrations but must link to contracts.
- Requirements can link to design docs but must not include implementation design.
- Contract impact rules belong in [contract-impact.md](contract-impact.md).
- If a section starts duplicating another document, replace it with a short summary and a link.

## Responsibility Boundaries

This template uses recursive repository containers instead of separate canonical templates for container and source repositories.

### Current Container

Location: repository root and [docs](README.md).

Responsibility:

- local boundary context;
- local architecture and decisions;
- contracts owned by this boundary;
- current state, open questions, specs, diagrams, glossary, and templates owned by this boundary;
- routing to direct child repositories.

### Parent Container

Location: external repository URL or local path, documented only when known.

Responsibility:

- upstream context that owns a wider boundary;
- decisions and contracts whose scope is above this container;
- navigation to this container as a direct child.

This container does not need to know the full parent chain.

### Child Repository

Location: a direct child entry under [repositories](../repositories/README.md).

Responsibility:

- one child repository boundary;
- its own current state, architecture, decisions, contracts, open questions, and implementation notes;
- its own direct children if it is also a container.

This container does not need to know all descendants below a child repository.

## Same Structure, Different Meaning

Different containers can use the same documentation structure, but the meaning changes by boundary.

Examples:

- `docs/architecture.md` in this repository describes this container boundary.
- `repositories/<child>/docs/architecture.md` describes that child boundary.
- a child repository may contain its own `repositories/` folder and repeat the same model.

Do not copy content between boundaries unless the same fact truly belongs at both levels. Prefer linking to the source boundary.

## Where To Put Information

- Local boundary context: current container docs.
- Parent-owned context: parent container docs.
- Child-owned context: child repository docs.
- Existing behavior and constraints: the nearest relevant `current-state.md`.
- Unresolved questions: the nearest relevant `open-questions.md`.
- Accepted decisions: ADR files at the boundary where the decision applies.
- API contracts: `docs/contracts/api`.
- Event contracts: `docs/contracts/events`.
- Integration contracts: `docs/contracts/integrations`.
- Contract ownership, scope, registry, and impact: [contract-impact.md](contract-impact.md).
- Terms: the nearest relevant `glossary.md`.
- Formal task format: `task-format.md`.
- Repository relationships: `repository-relationships.md`.
- Technology stack choices and constraints: `technology-stack.md`.

## Document Type Responsibilities

| Document type | Primary responsibility | Must link to instead of duplicating |
| --- | --- | --- |
| README | Navigation route and responsibility boundary. | Focused documents for details. |
| Current state | Observed facts about what exists now. | Architecture, ADRs, open questions, contracts. |
| System overview | Short orientation and boundaries. | Business context, architecture, contracts. |
| Business context | Business goals, actors, scenarios, and constraints. | Architecture, API design, database design. |
| Architecture | Target structure and responsibility boundaries. | ADRs, contracts, diagrams, open questions. |
| Integration map | Map of system relationships. | API, event, and integration contracts. |
| Data model | Domain entities, relationships, ownership, lifecycle. | Technical design, API schemas, glossary. |
| Glossary | Shared term definitions. | Architecture, requirements, design docs. |
| Open questions | Managed unresolved uncertainty. | ADRs or source docs after resolution. |
| ADR | One architecture decision. | Requirements, contracts, design docs. |
| Contracts | Agreements at system boundaries. | Integration map, architecture, requirements, contract impact. |
| Contract impact | Scope, registry, consumers, and change impact rules for public contracts. | Detailed contract payloads and architecture. |
| Requirements | What the system must do. | System design, technical design, ADRs. |
| System design | Component-level solution design. | Requirements, technical design, contracts. |
| Technical design | Implementation plan. | Requirements, system design, architecture. |
| Diagrams | Visual support for source documents. | Architecture, design, data model, contracts, integration map. |
| Archive | Historical material only. | Current source-of-truth documents. |

## Stack-Agnostic Documentation

The documentation model must not depend on a specific technology stack.

Technology choices belong in [technology-stack.md](technology-stack.md), architecture, ADRs, technical design, or child repository development docs depending on scope.

Changing a language, framework, database, infrastructure provider, or toolchain should not require rewriting README files, the documentation model, the operational model, AI collaboration rules, or working principles.

## Link Style

Use relative Markdown links for internal references inside this repository.

For links that cross from one repository to another, provide both when possible:

- a local relative link for IDE navigation, after the local path exists;
- an external repository URL for browser navigation.

Do not create Markdown links to placeholder paths that do not exist yet. Use plain placeholder text until the target file is present.

## RAG-Ready Documentation

The current goal is to keep documentation ready for future indexing:

- stable file locations;
- clear responsibility boundaries;
- focused Markdown documents;
- explicit links between related documents;
- durable decisions, questions, contracts, terms, and repository relationships.

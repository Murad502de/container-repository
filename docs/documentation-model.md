# Documentation Model

This document defines how project documentation is organized.

Documentation structure and responsibility levels are governed together with the [operational model](operational-model.md). Operational roles, workflows, decision-making, execution, handoff, acceptance, and documentation impact are defined there.

This document focuses on documentation structure, levels, ownership, link style, and anti-duplication.

## Goal

Documentation should be readable by humans, useful to AI agents, and ready for future retrieval-based workflows.

The documentation should be structured enough to recover project context without relying on a single chat thread or one person's memory.

## README Files Are Hubs

Every README is a navigation hub for its own responsibility level.

A README should contain:

- a short description of the repository, folder, direction, or service;
- its responsibility boundary;
- links to the most important documents;
- the recommended reading route for that level;
- pointers to the next README when the context becomes more specific.

A README should not contain every detail. If content grows too large, move it into a focused document and link to it.

## Single Source Of Truth

Project documentation is a connected network of source documents, not a set of duplicated summaries.

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
- If a section starts duplicating another document, replace it with a short summary and a link.

## Responsibility Levels

### Container Level

Location: repository root and [docs](README.md).

Responsibility:

- whole-project context;
- system boundaries;
- project-level architecture;
- project-level decisions;
- cross-direction and cross-service contracts;
- integration maps;
- shared templates and documentation conventions.

### Direction Level

Location: a connected direction repository or folder under `services/`.

Responsibility:

- direction-wide context;
- direction current state;
- direction target architecture;
- direction-level decisions;
- direction-level contracts and open questions;
- routing to concrete service repositories or source entry points.

### Service Level

Location: a concrete service or source repository.

Responsibility:

- one concrete service boundary;
- service-specific current state;
- service-specific architecture;
- service-specific API, event, and integration contracts;
- service-specific implementation notes and decisions.

## Same Structure, Different Meaning

Different levels can use the same documentation structure, but the meaning changes by level.

Examples:

- `docs/architecture.md` at the container level describes the project-wide architecture.
- `docs/architecture.md` in a direction repository describes only that direction.
- `docs/architecture.md` in a service repository describes only that service.

Do not copy content between levels unless the same fact truly belongs at both levels. Prefer linking to the source level.

## Where To Put Information

- Project-wide context: container-level docs.
- Direction-wide context: direction-level docs.
- Concrete service context: that service repository's docs.
- Existing behavior and constraints: the nearest relevant `current-state.md`.
- Unresolved questions: the nearest relevant `open-questions.md`.
- Accepted decisions: ADR files at the level where the decision applies.
- API contracts: `docs/contracts/api`.
- Event contracts: `docs/contracts/events`.
- Integration contracts: `docs/contracts/integrations`.
- Terms: the nearest relevant `glossary.md`.
- Formal task format: `task-format.md`.
- Container/source repository relationship: `repository-pairing.md`.
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
| Contracts | Agreements at system boundaries. | Integration map, architecture, requirements. |
| Requirements | What the system must do. | System design, technical design, ADRs. |
| System design | Component-level solution design. | Requirements, technical design, contracts. |
| Technical design | Implementation plan. | Requirements, system design, architecture. |
| Diagrams | Visual support for source documents. | Architecture, design, data model, contracts, integration map. |
| Archive | Historical material only. | Current source-of-truth documents. |

## Stack-Agnostic Documentation

The documentation model must not depend on a specific technology stack.

Technology choices belong in [technology-stack.md](technology-stack.md), architecture, ADRs, technical design, or source-level development docs depending on scope.

Changing a language, framework, database, infrastructure provider, or toolchain should not require rewriting README files, the documentation model, the operational model, AI collaboration rules, or working principles.

## Link Style

Use relative Markdown links for internal project references.

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
- durable decisions, questions, contracts, and terms.

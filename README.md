# Container Repository Template

This repository is a reusable template for project-level engineering memory.

Use it when a project needs a top-level place for product, system, architecture, integration, decision, and documentation rules across multiple directions or source repositories.

## Repository Responsibility

This repository is responsible for:

- project-level context and system boundaries;
- navigation between project, direction, and service documentation levels;
- documentation model, operational model, AI collaboration model, and working principles;
- project-level current state, architecture, open questions, ADRs, contracts, diagrams, specs, and templates;
- routing to connected direction or service repositories under [services](services/README.md).

This repository is not responsible for:

- source code of concrete services;
- implementation details owned by a source repository;
- service-specific API payloads, data models, or architecture decisions unless they affect the project level;
- duplicating documentation that already has a source document at a lower level.

## Start Here

Recommended reading route:

1. [AI collaboration model](docs/ai-collaboration.md)
2. [Operational model](docs/operational-model.md)
3. [Documentation model](docs/documentation-model.md)
4. [Working principles](docs/working-principles.md)
5. [Task format](docs/task-format.md)
6. [Repository pairing](docs/repository-pairing.md)
7. [Technology stack](docs/technology-stack.md)
8. [Documentation index](docs/README.md)
9. [System overview](docs/system-overview.md)
10. [Business context](docs/business-context.md)
11. [Architecture](docs/architecture.md)
12. [Open questions](docs/open-questions.md)
13. [Services index](services/README.md)

## Documentation Levels

Documentation is organized by responsibility level:

- Container level: this repository and its [docs](docs/README.md).
- Direction level: a repository or folder that owns a broad technical direction, such as `<direction-name>`.
- Service level: a repository that owns one concrete service or source code boundary.

The same document name can exist at different levels with different meaning. For example, `docs/architecture.md` in this repository describes project-level architecture, while a source repository's `docs/architecture.md` describes only that source boundary.

## Working Principles

- Documentation is durable project memory.
- README files are navigation hubs, not knowledge archives.
- Important facts, decisions, contracts, questions, and terms must be recorded in Markdown, not left only in chat.
- Each document has one primary responsibility.
- Link to source documents instead of duplicating content.
- Put unresolved uncertainty in the nearest relevant `open-questions.md`.
- Put accepted architecture decisions in ADR files.
- Put API, event, and integration agreements in `docs/contracts`.
- Do not start implementation work from assumptions when current state, requirements, architecture, or open questions are missing.

## Template Use

When creating a new project from this template:

1. Replace placeholder names such as `<project-name>`, `<direction-name>`, `<service-name>`, and `<organization>`.
2. Fill only confirmed facts.
3. Leave unknown sections as `Not documented yet`.
4. Use the required [task format](docs/task-format.md) for formal work requests.
5. Move unresolved items into [open questions](docs/open-questions.md).
6. Add connected repositories to [services](services/README.md).
7. Configure repository links according to [repository pairing](docs/repository-pairing.md).
8. Keep technology choices isolated according to [technology stack](docs/technology-stack.md).
9. Keep project-level and source-level documentation separated.

## Connected Repositories

Connected direction and service repositories are listed in [services/README.md](services/README.md).

Add only short descriptions and links there. Detailed direction or service knowledge belongs in that repository's own README and docs.

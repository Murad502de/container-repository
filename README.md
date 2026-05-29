# Repository Container Template

This repository is the canonical reusable template for an engineering repository container.

Use it for any local engineering boundary that needs durable memory, documentation, architecture decisions, contracts, open questions, and navigation to child repository boundaries.

A container can represent a project, direction, subsystem, backend or frontend area, microservice, infrastructure area, implementation area, documentation area, or any other self-contained engineering boundary.

The same template can be used recursively. A child repository listed under [repositories](repositories/README.md) may itself be another repository container.

## Repository Responsibility

This repository is responsible for:

- local responsibility boundary and system context for this container;
- navigation between this container, its nearest parent when known, and its direct child repositories;
- documentation model, operational model, AI collaboration model, and working principles;
- current state, architecture, open questions, ADRs, contracts, diagrams, specs, and templates owned by this boundary;
- routing to child repository boundaries under [repositories](repositories/README.md).

This repository is not responsible for:

- owning the full parent chain above this container;
- owning all descendants at arbitrary depth;
- duplicating child repository documentation;
- storing implementation code as part of the base template.

## Start Here

Recommended reading route:

1. [AI collaboration model](docs/ai-collaboration.md)
2. [Operational model](docs/operational-model.md)
3. [Documentation model](docs/documentation-model.md)
4. [Working principles](docs/working-principles.md)
5. [Task format](docs/task-format.md)
6. [Repository relationships](docs/repository-relationships.md)
7. [Contract impact model](docs/contract-impact.md)
8. [Technology stack](docs/technology-stack.md)
9. [Documentation index](docs/README.md)
10. [System overview](docs/system-overview.md)
11. [Business context](docs/business-context.md)
12. [Architecture](docs/architecture.md)
13. [Open questions](docs/open-questions.md)
14. [Repositories index](repositories/README.md)

## Self-Nesting Model

Documentation is organized by local ownership boundaries:

- Current container: this repository and its [docs](docs/README.md).
- Parent container: the nearest upstream repository boundary, if one exists.
- Child repositories: direct children listed under [repositories](repositories/README.md).

The same document name can exist at different boundaries with different meaning. For example, this repository's `docs/architecture.md` describes this container boundary, while a child container's `docs/architecture.md` describes that child boundary.

A container only needs to know:

- its own responsibility boundary;
- its direct children;
- its nearest parent when that relationship is known.

A container does not need to know every ancestor or every descendant.

## Working Principles

- Documentation is durable engineering memory.
- README files are navigation hubs, not knowledge archives.
- Important facts, decisions, contracts, questions, and terms must be recorded in Markdown, not left only in chat.
- Each document has one primary responsibility.
- Link to source documents instead of duplicating content.
- Put unresolved uncertainty in the nearest relevant `open-questions.md`.
- Put accepted architecture decisions in ADR files.
- Put API, event, and integration agreements in `docs/contracts`.
- Analyze public contract changes through [contract impact](docs/contract-impact.md).
- Do not start implementation work from assumptions when current state, requirements, architecture, or open questions are missing.

## Template Use

When creating a new container from this template:

1. Replace placeholder names such as `<container-name>`, `<repository-name>`, `<boundary-name>`, and `<organization>`.
2. Fill only confirmed facts.
3. Leave unknown sections as `Not documented yet`.
4. Use the required [task format](docs/task-format.md) for formal work requests.
5. Move unresolved items into [open questions](docs/open-questions.md).
6. Add direct child repositories to [repositories](repositories/README.md).
7. Configure parent-child repository links according to [repository relationships](docs/repository-relationships.md).
8. Keep technology choices isolated according to [technology stack](docs/technology-stack.md).
9. Keep parent, current container, and child repository documentation separated.
10. Use [contract impact](docs/contract-impact.md) when a public contract may change.

## Child Repositories

Direct child repository boundaries are listed in [repositories/README.md](repositories/README.md).

Add only short descriptions and links there. Detailed child repository knowledge belongs in that repository's own README and docs.

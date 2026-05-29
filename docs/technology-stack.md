# Technology Stack

This document records technology choices and constraints for this container boundary without making the documentation model depend on a specific stack.

## Principle

Documentation must be stack-agnostic by default.

Programming languages, frameworks, databases, infrastructure providers, and tools are replaceable project facts. They should not be embedded into README files, documentation model, operational model, AI collaboration rules, or working principles unless the topic is specifically about the stack.

## Scope

Level: Container.

Use this document for:

- technology choices owned by this container;
- stack constraints shared across direct child repositories;
- cross-boundary runtime, infrastructure, database, observability, deployment, or tooling standards;
- links to ADRs that justify technology choices.

Child-specific stack details belong in the owning child repository.

## Current Technology Stack

| Area | Technology | Scope | Status | Owner | Decision / Source |
| --- | --- | --- | --- | --- | --- |
| Not documented yet | Not documented yet | Container | Not documented yet | Not assigned | Not documented yet |

## Stack Decision Rules

- If a technology choice affects architecture, record the decision in ADR.
- If a technology choice affects implementation planning, describe details in technical design.
- If a technology choice affects local development or runtime, document it in the owning repository boundary.
- If the technology is only an implementation detail, do not spread it into model documents.

## Replacement Rules

Changing the technology stack should not require rewriting:

- root README;
- documentation model;
- operational model;
- AI collaboration model;
- working principles;
- task format.

When a stack changes:

1. Update this document.
2. Update affected ADRs or add a new ADR.
3. Update affected architecture or technical design documents.
4. Update child repository development docs.
5. Check contracts and integration maps only if external behavior changes.

## Related Documents

- [Architecture](architecture.md)
- [ADR index](adr/README.md)
- [Technical design](specs/technical-design/README.md)
- [Working principles](working-principles.md)

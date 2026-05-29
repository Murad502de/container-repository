# Technology Stack Template

## Purpose

Use this template to document technology choices without making the documentation model depend on a specific stack.

## Template Body

```md
# Technology Stack

## Principle

Documentation must be stack-agnostic by default.

Programming languages, frameworks, databases, infrastructure providers, and tools are replaceable project facts. They should not be embedded into README files, documentation model, operational model, AI collaboration rules, or working principles unless the topic is specifically about the stack.

## Scope

Boundary: Current container | Parent container | Child repository: <name>

## Current Technology Stack

| Area | Technology | Scope | Status | Owner | Decision / Source |
| --- | --- | --- | --- | --- | --- |
| <Area> | <Technology> | <Scope> | <Status> | <Owner> | <ADR or source> |

## Stack Decision Rules

- If a technology choice affects architecture, record the decision in ADR.
- If a technology choice affects implementation planning, describe details in technical design.
- If a technology choice affects local development or runtime, document it in the owning repository boundary.
- If the technology is only an implementation detail, do not spread it into model documents.

## Replacement Rules

- Changing the technology stack should not require rewriting root README, documentation model, operational model, AI collaboration model, working principles, or task format.
- When a stack changes, update this document first.
- Update affected ADRs or add a new ADR.
- Update affected architecture or technical design documents.
- Update child repository development docs.
- Check contracts and integration maps only if external behavior changes.

## Related Documents

- Architecture: `architecture.md`
- ADR index: `adr/README.md`
- Technical design: `specs/technical-design/README.md`
- Working principles: `working-principles.md`
```

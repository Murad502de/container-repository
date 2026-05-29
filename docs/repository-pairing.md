# Repository Pairing

This document defines how a container repository and source repositories work together.

The repositories are designed to be self-contained and compatible. They may be used separately, but when used together they form one documentation system.

## Repository Roles

## Container Repository

The container repository owns project-level knowledge:

- project context;
- documentation model;
- operational model;
- AI collaboration model;
- working principles;
- project-level architecture;
- cross-direction and cross-service decisions;
- project-level contracts and integration maps;
- project-level open questions;
- routes to connected source repositories.

## Source Repository

A source repository owns one source boundary:

- source current state;
- source target architecture;
- source-level ADRs;
- source-owned contracts;
- source-level open questions;
- source implementation notes;
- source code entry points.

## Pairing Rules

- Both repositories must remain understandable when opened alone.
- When used together, the container repository is the project-level source of truth.
- Source repositories may keep local copies of operating rules for autonomy.
- If local source rules conflict with container-level rules, container-level rules win for project-wide work.
- Source repositories should link to container-level documents instead of copying project context.
- Container repository should route to source repositories without duplicating source details.

## Setup Checklist

When connecting a source repository to a container repository:

1. Add the source repository to [../services/README.md](../services/README.md).
2. Replace source repository parent placeholders with real local paths or external URLs.
3. Verify README routes in both repositories.
4. Keep project-level questions in container docs.
5. Keep source-level questions in source docs.
6. Check that local Markdown links resolve.

## Synchronization Rules

Synchronize these across paired template repositories when the shared model changes:

- documentation model principles;
- operational model rules;
- AI collaboration rules;
- working principles;
- task format;
- repository pairing rules;
- technology stack rules;
- reusable document templates.

Do not synchronize project-specific facts, service-specific facts, ADRs, contracts, or open questions unless the same information truly belongs at both levels.

## Related Documents

- [Documentation model](documentation-model.md)
- [Operational model](operational-model.md)
- [AI collaboration model](ai-collaboration.md)
- [Working principles](working-principles.md)
- [Services index](../services/README.md)

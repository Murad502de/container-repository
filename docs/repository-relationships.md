# Repository Relationships

This document defines how self-nesting repository containers relate to parent and child repositories.

The canonical template is this repository container model. A child repository can be another container, an implementation repository, an infrastructure repository, a documentation repository, an external repository reference, or a future placeholder.

## Core Model

Repository relationships are local and recursive:

```text
nearest parent container
  -> current container
      -> direct child repositories
          -> each child may have its own child repositories
```

Each container knows:

- its own responsibility boundary;
- its nearest parent when known;
- its direct children.

Each container does not need to know:

- every ancestor above the nearest parent;
- every descendant below direct children;
- implementation details owned by child repositories.

## Current Container

The current container owns knowledge for its local boundary:

- local context;
- documentation model;
- operational model;
- AI collaboration model;
- working principles;
- architecture and decisions within this boundary;
- contracts and integration maps owned by this boundary;
- local open questions;
- routes to direct child repositories.

## Parent Container

A parent container owns the nearest wider boundary, if one exists.

Use parent links for:

- upstream context;
- wider architectural decisions;
- contracts whose declared scope is above the current container;
- shared operating rules;
- navigation from a larger boundary to this container.

Do not duplicate parent knowledge locally. Summarize briefly only when it helps orientation, then link to the parent source document.

## Child Repositories

Child repositories are listed in [repositories](../repositories/README.md).

The `repositories/` folder may contain:

- child container repositories;
- implementation repositories;
- infrastructure repositories;
- documentation repositories;
- external repository references;
- future repository placeholders.

Each child repository owns its own local boundary and should provide its own README and docs when it contains durable knowledge.

## Relationship Rules

- Both parent and child repositories must remain understandable when opened alone.
- The current container is the source of truth for its own boundary.
- Parent containers own wider-boundary knowledge.
- Child repositories own their local details.
- If local rules conflict with parent rules, parent rules win only for the parent-owned scope.
- Link to parent or child source documents instead of copying their content.
- Route to child repositories without duplicating child details.

## Setup Checklist

When connecting a child repository:

1. Add the child repository to [repositories/README.md](../repositories/README.md).
2. Replace parent/child placeholders with real local paths or external URLs.
3. Verify README routes in both repositories.
4. Keep current-boundary questions in this container's docs.
5. Keep child-boundary questions in the child repository.
6. Check that local Markdown links resolve.

## Synchronization Rules

Synchronize these across related containers when the shared model changes:

- documentation model principles;
- operational model rules;
- AI collaboration rules;
- working principles;
- task format;
- repository relationship rules;
- contract impact rules;
- technology stack rules;
- reusable document templates.

Do not synchronize boundary-specific facts, ADRs, contracts, open questions, implementation details, or local decisions unless the same information truly belongs at both boundaries.

## Relationship To Contract Impact

Repository relationships define ownership and navigation.

Contract graph defines dependency impact.

A repository tree alone does not prove that a change is safe. Public contract changes must be analyzed through [contract impact](contract-impact.md).

## Related Documents

- [Documentation model](documentation-model.md)
- [Operational model](operational-model.md)
- [AI collaboration model](ai-collaboration.md)
- [Working principles](working-principles.md)
- [Contract impact model](contract-impact.md)
- [Repositories index](../repositories/README.md)

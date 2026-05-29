# Repository Relationships Template

## Purpose

Use this template to describe how a self-nesting repository container relates to its nearest parent and direct child repositories.

## Template Body

```md
# Repository Relationships

## Core Model

Repository relationships are local and recursive:

- nearest parent container;
- current container;
- direct child repositories.

Each container knows its own boundary, nearest parent when known, and direct children.

Each container does not need to know every ancestor or every descendant.

## Current Container

- Owns local context, operating rules, decisions, contracts, open questions, and routes to direct child repositories.

## Parent Container

- Owns the nearest wider boundary when one exists.
- Provides upstream context, wider decisions, and contracts whose declared scope is above the current container.

## Child Repositories

Child repositories may be:

- child container repositories;
- implementation repositories;
- infrastructure repositories;
- documentation repositories;
- external repository references;
- future repository placeholders.

## Relationship Rules

- Both parent and child repositories must remain understandable when opened alone.
- The current container is the source of truth for its own boundary.
- Parent containers own wider-boundary knowledge.
- Child repositories own their local details.
- If local rules conflict with parent rules, parent rules win only for the parent-owned scope.
- Link to parent or child source documents instead of copying their content.
- Route to child repositories without duplicating child details.

## Setup Checklist

1. Add the child repository to `repositories/README.md`.
2. Replace parent/child placeholders with real local paths or external URLs.
3. Verify README routes in both repositories.
4. Keep current-boundary questions in this container's docs.
5. Keep child-boundary questions in the child repository.
6. Check that local Markdown links resolve.

## Synchronization Rules

- Synchronize documentation model principles.
- Synchronize operational model rules.
- Synchronize AI collaboration rules.
- Synchronize working principles.
- Synchronize task format rules.
- Synchronize repository relationship rules.
- Synchronize contract impact rules.
- Synchronize technology stack rules.
- Synchronize reusable document templates.

Do not synchronize boundary-specific facts, ADRs, contracts, open questions, implementation details, or local decisions unless the same information truly belongs at both boundaries.

## Related Documents

- Documentation model: `documentation-model.md`
- Operational model: `operational-model.md`
- AI collaboration model: `ai-collaboration.md`
- Working principles: `working-principles.md`
- Contract impact model: `contract-impact.md`
```

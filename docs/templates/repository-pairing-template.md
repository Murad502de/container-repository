# Repository Pairing Template

## Purpose

Use this template to describe how a container repository and source repositories are connected.

## Template Body

```md
# Repository Pairing

## Repository Roles

### Container Repository

- Owns project-level context, operating rules, cross-service decisions, and routes to source repositories.

### Source Repository

- Owns one source boundary: local current state, architecture, ADRs, contracts, open questions, and implementation notes.

## Pairing Rules

- Both repositories must remain understandable when opened alone.
- When used together, the container repository is the project-level source of truth.
- Source repositories may keep local copies of operating rules for autonomy.
- If local source rules conflict with container-level rules, container-level rules win for project-wide work.
- Source repositories should link to container-level documents instead of copying project context.
- Container repository should route to source repositories without duplicating source details.

## Setup Checklist

1. Add the source repository to the container repository services index.
2. Replace parent/container placeholders with real local paths or external URLs.
3. Verify README routes in both repositories.
4. Keep project-level questions in container docs.
5. Keep source-level questions in source docs.
6. Check that local Markdown links resolve.

## Synchronization Rules

- Synchronize documentation model principles.
- Synchronize operational model rules.
- Synchronize AI collaboration rules.
- Synchronize working principles.
- Synchronize task format rules.
- Synchronize repository pairing rules.
- Synchronize technology stack rules.
- Synchronize reusable document templates.

Do not synchronize project-specific facts, service-specific facts, ADRs, contracts, or open questions unless the same information truly belongs at both levels.

## Related Documents

- Documentation model: `documentation-model.md`
- Operational model: `operational-model.md`
- AI collaboration model: `ai-collaboration.md`
- Working principles: `working-principles.md`
```

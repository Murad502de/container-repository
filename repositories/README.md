# Repositories

This folder is the local entry point for direct child repository boundaries.

A child repository may be another container repository, an implementation repository, an infrastructure repository, a documentation repository, an external repository reference, or a future repository placeholder.

## Responsibility

This README routes from the current container to direct child repositories.

It is responsible for:

- listing direct child repositories;
- stating each child repository's local responsibility in one short line;
- identifying repository type and relationship status;
- linking to local README files and external repository URLs when they exist.

It is not responsible for:

- describing child implementation details;
- duplicating child architecture, contracts, ADRs, or open questions;
- documenting grandchildren or deeper descendants unless a direct child repository intentionally exposes that route.

## Current Entries

No child repositories have been added yet.

When a child repository is connected, add a row with this shape:

| Name | Type | Responsibility | Status | Local entry | External entry |
| --- | --- | --- | --- | --- | --- |
| `<repository-name>` | Container \| Implementation \| Infrastructure \| Documentation \| External \| Placeholder | `<short responsibility>` | Planned \| Connected \| External \| Archived | `<relative path to README>` | `<repository URL>` |

Use plain placeholder text until the target path exists. Convert it to a Markdown link only after the file is present.

## Child Repository Types

- Container: another self-nesting repository container.
- Implementation: a repository focused on code or runtime implementation.
- Infrastructure: a repository focused on deployment, infrastructure, environments, or operations.
- Documentation: a repository focused on durable documentation or knowledge artifacts.
- External: a referenced repository outside the local workspace.
- Placeholder: a future repository boundary that has not been created yet.

## Relationship Rules

- Keep this README as an index.
- Add only short descriptions and links.
- Put child-specific details in the child repository.
- Link to connected repositories instead of duplicating their documentation.
- Follow [repository relationship rules](../docs/repository-relationships.md) when connecting repositories.
- Use [contract impact rules](../docs/contract-impact.md) when a child repository owns or consumes public contracts.
- Update [../README.md](../README.md) if the recommended reading route changes.

# Services

This folder is the local entry point for connected direction and service repositories.

The container repository does not store product source code directly. Direction or service repositories can be connected locally under this folder when a project needs local cross-repository navigation.

## Responsibility

This README routes from the container-level repository to connected repositories.

It is responsible for:

- listing connected direction and service repositories;
- stating each connected repository's responsibility in one short line;
- linking to local README files and external repository URLs when they exist.

It is not responsible for:

- describing implementation details of connected repositories;
- duplicating service architecture, contracts, ADRs, or open questions;
- storing source code.

## Current Entries

No connected repositories have been added yet.

When a repository is connected, add a row with this shape:

| Name | Responsibility | Local entry | External entry |
| --- | --- | --- | --- |
| `<direction-or-service-name>` | `<short responsibility>` | `<relative path to README>` | `<repository URL>` |

Use plain placeholder text until the target path exists. Convert it to a Markdown link only after the file is present.

## Rules

- Keep this README as an index.
- Add only short descriptions and links.
- Put direction-specific details in that direction repository.
- Put service-specific details in that service repository.
- Link to connected repositories instead of duplicating their documentation.
- Follow [repository pairing rules](../docs/repository-pairing.md) when connecting repositories.
- Update [../README.md](../README.md) if the recommended reading route changes.

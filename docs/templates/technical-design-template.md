# Technical Design Template

## Purpose

Use this template to describe how an approved design or requirement will be implemented technically.

## Template Body

```md
# Technical Design: <Title>

Status: Draft | Active | Archived

## Implementation Overview

Describe the planned implementation approach.

## Affected Repositories / Files / Modules

- `<path-or-module>` - <reason>

## Interfaces

Describe APIs, events, internal interfaces, or command boundaries affected by the change.

## Technology Stack Impact

Describe language, framework, database, infrastructure, or tooling impact. Link to technology stack and ADRs when relevant.

## Data / Storage Changes

Describe schema, storage, migration, or data ownership changes.

## Migration Plan

Describe migration steps or state "Not applicable".

## Validation / Testing Plan

- <Test or validation step>

## Rollout Plan

Describe deployment and rollout sequencing.

## Rollback Plan

Describe how to revert or disable the change safely.

## Risks

- <Risk and mitigation>

## Related Documents

- [<Document title>](<relative-link>)
```

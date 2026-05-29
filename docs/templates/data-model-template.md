# Data Model Template

## Purpose

Use this template to describe domain entities, relationships, ownership, lifecycle, and important data rules.

## Template Body

```md
# Data Model

## Scope

Level: Container | Direction: <name> | Service: <name>

Describe which domain area this data model covers.

## Core Entities

| Entity | Definition | Owner |
| --- | --- | --- |
| <Entity> | <Domain definition> | <Owner> |

## Relationships

- `<Entity A>` relates to `<Entity B>` because <reason>.

## Ownership

Describe source-of-truth ownership for key data categories.

## Lifecycle / Statuses

| Entity | Status | Meaning |
| --- | --- | --- |
| <Entity> | <Status> | <Meaning> |

## Business Rules

- <Rule>

## Data Consistency Rules

- <Rule>

## Privacy / Security Considerations

- <Consideration>

## Related Documents

- [<Document title>](<relative-link>)
```

# Integration Contract Template

## Purpose

Use this template to define an agreement with an external system or another internal system when the relationship is broader than one endpoint or one event.

## Template Body

```md
# Integration Contract: <System Name>

## Status

Draft | Proposed | Accepted | Deprecated

## External / Internal System

<System name and short description>

## Purpose

Describe why this integration exists.

## Owner

<Owning team, direction, service, or person>

## Scope

Local | Child | Container | Parent | External | Unknown

## Registry

- Registry owner: <scope owner>
- Registry status: Authoritative | Partial | Missing | Unknown
- Known consumers: <consumer list or Unknown>

## Auth Method

Describe authentication and authorization.

## Data Exchanged

| Data Category | Direction | Notes |
| --- | --- | --- |
| <Category> | <A -> B> | <Notes> |

## Operations / Use Cases

- <Operation or use case>

## Error Handling

Describe expected failures, retries, and fallback behavior.

## Rate Limits / Quotas

Describe known limits or state "Not documented yet".

## Security / Privacy Concerns

- <Concern>

## Impact Rules

Use `contract-impact.md` before changing this integration when it has public consumers, external consumers, or unknown consumers.

## Environments

| Environment | URL / Identifier | Notes |
| --- | --- | --- |
| Sandbox | <Value> | <Notes> |
| Production | <Value> | <Notes> |

## Related Documents

- [<Document title>](<relative-link>)
```

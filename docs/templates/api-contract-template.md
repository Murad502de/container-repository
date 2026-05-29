# API Contract Template

## Purpose

Use this template to define an HTTP/API contract between clients and a system boundary.

## Template Body

````md
# API Contract: <Contract Name>

## Status

Draft | Proposed | Accepted | Deprecated

## Owner

<Team, direction, service, or person>

## Scope

Container | Direction: <name> | Service: <name>

## Endpoint

- Method: `<GET | POST | PUT | PATCH | DELETE>`
- Path: `/<path>`
- Purpose: <one-sentence purpose>

## Auth

Describe authentication and authorization requirements.

## Request Headers

| Header | Required | Description |
| --- | --- | --- |
| `<Header-Name>` | Yes | <Description> |

## Path Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `<name>` | `<type>` | Yes | <Description> |

## Query Parameters

| Name | Type | Required | Description |
| --- | --- | --- | --- |
| `<name>` | `<type>` | No | <Description> |

## Request Body

```json
{
  "field": "value"
}
```

## Response Codes

| Code | Meaning |
| --- | --- |
| 200 | <Meaning> |
| 400 | <Meaning> |

## Response Body

```json
{
  "field": "value"
}
```

## Error Model

Describe common error shape, error codes, and validation behavior.

## Idempotency

Describe idempotency rules or state "Not applicable".

## Versioning

Describe compatibility and versioning rules.

## Examples

Add short request/response examples.

## Related Documents

- [<Document title>](<relative-link>)
````

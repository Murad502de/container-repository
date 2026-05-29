# Event Contract Template

## Purpose

Use this template to define an event contract between producers and consumers.

## Template Body

````md
# Event Contract: <Event Name>

## Status

Draft | Proposed | Accepted | Deprecated

## Owner

<Repository boundary, team, role, or person>

## Scope

Local | Child | Container | Parent | External | Unknown

## Registry

- Registry owner: <scope owner>
- Registry document: `contracts/registry.md`
- Registry status: Authoritative | Partial | Missing | Unknown
- Known consumers: <consumer list or Unknown>

## Event Name

`<event.name>`

## Producer

<Producer>

## Consumers

- <Consumer>

## Trigger

Describe when this event is emitted.

## Payload Schema

```json
{
  "field": "value"
}
```

## Versioning

Describe compatibility and versioning rules.

## Impact Rules

Use `contract-impact.md` before changing this event when it has public consumers or unknown consumers.

## Delivery Guarantees

At most once | At least once | Exactly once | Not documented yet

## Retry / Dead-Letter Behavior

Describe retry and dead-letter behavior.

## Ordering Assumptions

Describe ordering guarantees or state "No ordering guarantee".

## Idempotency Expectations

Describe how consumers should handle duplicates.

## Examples

Add short representative examples.

## Related Documents

- [<Document title>](<relative-link>)
````

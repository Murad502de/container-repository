# Integration Map Template

## Purpose

Use this template to map relationships between systems. An integration map shows who talks to whom, why, in which direction, and where the detailed contract lives.

## Template Body

```md
# Integration Map

Status: Draft | Active | Archived

## Scope

Level: Container | Direction: <name> | Service: <name>

Describe which integrations are covered.

## Integration Summary

| System | Purpose | Direction | Initiator | Data Categories | Protocol / Transport | Auth Overview | Owner | Contract |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| <System> | <Purpose> | <A -> B> | <Initiator> | <Categories> | <Overview> | <Overview> | <Owner> | <Contract link> |

## Risks / Constraints

- <Risk or constraint>

## Current vs Target Notes

Separate current observed integrations from target integrations when needed.

## Related Documents

- [<Document title>](<relative-link>)
```

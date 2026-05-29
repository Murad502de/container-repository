# Contract Impact Template

## Purpose

Use this template to document contract scope, registry, consumers, and impact analysis for a public contract change.

## Template Body

```md
# Contract Impact: <Change Name>

## Status

Draft | In Review | Accepted | Blocked

## Contract

- Contract name: <name>
- Contract type: API | Event | Integration | Data exchange | Public behavior | Other
- Contract document: <relative-link-or-plain-path>

## Provider

<Repository or boundary that owns the contract>

## Scope

Local | Child | Container | Parent | External | Unknown

If scope is unknown, record the gap in `open-questions.md`.

## Registry

- Registry owner: <scope owner>
- Registry document: <relative-link-or-plain-path>
- Registry status: Authoritative | Partial | Missing | Unknown

## Known Consumers

| Consumer | Usage | Compatibility expectation | Checked |
| --- | --- | --- | --- |
| <Consumer boundary> | <Usage summary> | <Expectation> | Yes | No |

## Proposed Change

Describe the proposed contract change.

## Impact Assessment

- Provider impact:
- Consumer impact:
- Migration required:
- Backward compatibility:
- Rollout constraints:

## Decision

Proceed | Blocked | Needs more information

## Documentation Gaps

- <Missing scope, registry, consumer, compatibility rule, or owner>

## Related Documents

- <Related document>
```

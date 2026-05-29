# Contract Impact Template

## Purpose

Use this template to document contract scope, registry coverage, consumers, escalation, and impact analysis for a public contract change.

## Template Body

```md
# Contract Impact: <Change Name>

## Impact Request

- Impact request ID: CI-0001
- Status: Draft | In Review | Accepted | Blocked
- Requested by: <person or role>
- Date: <YYYY-MM-DD>

## Contract

- Contract name: <name>
- Contract type: API | Event | Integration | Data exchange | Public behavior | Other
- Contract document: <relative-link-or-plain-path>
- Current contract version: <version or Not documented yet>
- Changed contract version: <version or Not documented yet>

## Provider

<Repository or boundary that owns the contract>

## Declared Scope

Local | Child | Container | Parent | External | Unknown

Scope owner: <repository or boundary>

If scope or scope owner is unknown, record the gap in `open-questions.md`.

## Registry

- Authoritative registry link: <relative-link-or-plain-path>
- Registry status: Authoritative | Partial | Missing | Unknown
- Registry owner: <scope owner>

Partial, missing, or unknown registry does not prove change safety.

## Affected Consumers

| Consumer | Usage | Compatibility expectation | Check status | Notes |
| --- | --- | --- | --- | --- |
| <Consumer boundary> | <Usage summary> | <Expectation> | Not checked | <Notes> |

No listed consumers proves no impact only when registry status is Authoritative.

## Proposed Change

Describe the proposed contract change.

## Impact Assessment

- Provider impact:
- Consumer impact:
- Migration required:
- Backward compatibility:
- Rollout constraints:

## Escalation

- Escalation status: Not needed | Needed | Requested | Resolved | Blocked
- Escalation owner: <scope owner or responsible role>
- Escalation reason: <scope outside current boundary, partial registry, unknown consumers, external impact, etc.>

## Unresolved Gaps

- <Missing scope, registry owner, consumers, compatibility rule, or source document>

Each unresolved gap must be linked to `open-questions.md`.

## Final Decision

Proceed | Proceed with compatibility constraints | Blocked | Needs more information

Decision owner: <person or role>

Decision notes:

## Related Documents

- Contract registry: `contracts/registry.md`
- Contract impact model: `contract-impact.md`
- Open questions: `open-questions.md`
```

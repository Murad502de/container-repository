# Contract Impact Model

This document defines how public contract changes are analyzed across repository containers.

Repository tree defines ownership and navigation. Contract graph defines impact.

## Purpose

Use this document when a change may affect an API, event, integration, data exchange, public behavior, or another boundary contract.

The goal is to avoid both extremes:

- assuming every change must propagate to the root container;
- assuming a local change is safe when contract scope, registry, or consumers are unknown.

## Core Rules

- Repository tree defines ownership.
- Contract graph defines impact.
- Provider owns the contract document.
- Scope owner owns the authoritative registry for that scope.
- Consumer owns its usage and compatibility expectations.
- Every public contract must have a declared scope.
- Impact requests rise to the declared contract scope, not automatically to the root.
- An authoritative registry can stop impact propagation when it proves the affected consumers are known.
- A partial or unknown registry is not sufficient proof that a change is safe.
- Missing scope, registry, or consumers must be recorded as an open question or documentation gap.

## Contract Scope

Every public contract should declare its scope:

| Scope | Meaning |
| --- | --- |
| Local | Used only inside one repository boundary. |
| Child | Used between the current container and one direct child. |
| Container | Used across multiple direct children inside the current container. |
| Parent | Owned or governed by the nearest parent container. |
| External | Used by systems outside the known repository tree. |
| Unknown | Scope is not documented yet and must be treated as a gap. |

If scope is unknown, do not treat the change as safe. Record the missing scope in [open questions](open-questions.md).

## Ownership Model

| Role | Responsibility |
| --- | --- |
| Provider | Owns the contract document and proposed change. |
| Consumer | Owns usage, compatibility expectations, and local migration work. |
| Scope owner | Owns the authoritative registry for the declared contract scope. |
| Current container | Owns local impact assessment for contracts inside this boundary. |
| Parent container | Owns impact assessment only when the declared scope reaches that parent. |

## Registry Model

A contract registry is authoritative only when it is maintained by the owner of the declared scope.

The registry should identify:

- contract name;
- provider;
- declared scope;
- known consumers;
- owner;
- status;
- source document;
- compatibility notes.

If registry information is partial, stale, or unknown, the safe conclusion is not "no consumers". The safe conclusion is "impact unknown".

## Impact Flow

When a public contract may change:

1. Identify the contract document.
2. Identify the provider.
3. Identify the declared contract scope.
4. Find the authoritative registry for that scope.
5. Identify known consumers.
6. Ask each affected consumer to assess usage impact.
7. Record required migrations or compatibility constraints.
8. Update ADRs, contracts, integration maps, and open questions as needed.

Impact stops when the declared scope owner has an authoritative registry that proves the affected consumers are known and checked.

Impact does not stop when:

- scope is missing;
- registry is missing;
- registry is partial;
- consumers are unknown;
- the change affects external behavior but external consumers are undocumented.

## Documentation Gaps

Record a documentation gap when:

- a public contract has no declared scope;
- provider is unknown;
- consumers are unknown;
- registry is missing;
- registry owner is unclear;
- compatibility expectations are not documented;
- impact cannot be determined from current documentation.

Use [open questions](open-questions.md) for unresolved gaps.

## Minimal Contract Registry

Use this table in the nearest owning document when a dedicated registry does not exist yet:

| Contract | Provider | Scope | Registry owner | Known consumers | Status | Source |
| --- | --- | --- | --- | --- | --- | --- |
| Not documented yet | Not documented yet | Unknown | Not assigned | Unknown | Open | Not documented yet |

## Related Documents

- [Repository relationships](repository-relationships.md)
- [Contracts](contracts/README.md)
- [Integration map](integration-map.md)
- [Open questions](open-questions.md)
- [ADR index](adr/README.md)

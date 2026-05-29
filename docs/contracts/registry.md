# Contract Registry

This document is the registry of public contracts owned or governed by this container boundary.

Use it to record contract ownership, declared scope, registry coverage, known consumers, and impact status. Detailed request/response payloads, event schemas, or integration behavior belong in the contract documents themselves.

## Purpose

The registry makes contract impact analysis practical.

It answers:

- which contracts are known;
- who provides each contract;
- which scope each contract declares;
- who owns the registry for that scope;
- whether consumer coverage is authoritative, partial, missing, or unknown;
- which consumers must be checked before a contract change is accepted.

## Registry Authority

A registry is authoritative only when it is maintained by the owner of the declared contract scope.

Coverage statuses:

| Status | Meaning | Safety meaning |
| --- | --- | --- |
| Authoritative | Scope owner maintains the registry and known consumers are tracked. | Can stop impact propagation after affected consumers are checked. |
| Partial | Some contracts or consumers are known, but coverage is incomplete. | Does not prove change safety. |
| Missing | Registry is required but not created yet. | Treat impact as unknown. |
| Unknown | Registry ownership or coverage is not documented. | Treat impact as unknown. |

No listed consumers means "no known consumers" only when coverage is authoritative.

## Contract Registry

| Contract | Type | Provider | Declared scope | Scope owner | Registry status | Known consumers | Consumer check status | Source document | Impact notes |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Not documented yet | Not documented yet | Not documented yet | Unknown | Not assigned | Unknown | Unknown | Not checked | Not documented yet | Not documented yet |

## Maintenance Rules

- Add public contracts when they are created or discovered.
- Keep detailed behavior in contract documents, not in this registry.
- Keep relationship summaries in [integration map](../integration-map.md), not in this registry.
- Update consumer check status during impact analysis.
- If scope, registry owner, or consumers are missing, record the gap in [open questions](../open-questions.md).
- Use [contract impact model](../contract-impact.md) before accepting public contract changes.

## Related Documents

- [Contract impact model](../contract-impact.md)
- [Contracts index](README.md)
- [Integration map](../integration-map.md)
- [Open questions](../open-questions.md)

# Architecture Template

## Purpose

Use this template to describe the target architecture at a specific responsibility boundary.

## Template Body

```md
# Architecture

Status: Draft | Active | Archived

## Scope and Boundary

Boundary: Current container | Parent container | Child repository: <name>

Describe what this architecture owns and what it does not own.

## Architecture Summary

Summarize the target architecture in a few paragraphs.

## Responsibility Boundaries

### In Scope

- <Responsibility>

### Out of Scope

- <Responsibility owned elsewhere>

## Components / Boundaries / Repositories

| Component | Responsibility | Owner |
| --- | --- | --- |
| <Name> | <Responsibility> | <Owner> |

## Communication Rules

Describe allowed communication patterns, protocols, and direction of calls.

## Data Ownership Principles

Describe which components own which data categories and where sources of truth live.

## Security Principles

Describe authentication, authorization, privacy, and trust boundary principles.

## Operational Assumptions

Describe deployment, observability, failure, scaling, and support assumptions.

## Technology Stack

Link to the stack source document. Summarize only architecture-significant technology choices.

## Quality Attributes

- Reliability: <expectation>
- Security: <expectation>
- Maintainability: <expectation>
- Performance: <expectation>

## Key Tradeoffs

- <Tradeoff and why it is acceptable>

## Related ADRs

- [<ADR title>](<relative-link>)

## Related Contracts

- [<Contract title>](<relative-link>)

## Related Diagrams

- [<Diagram title>](<relative-link>)

## Related Open Questions

- [<Open questions>](<relative-link>)
```

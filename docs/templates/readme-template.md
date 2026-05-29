# README Template

## Purpose

Use this template for repository-level README files. A README is a navigation hub and orientation point, not the place where all boundary knowledge lives.

## Required Structure

- Title.
- Short description.
- Responsibility boundary.
- What belongs here.
- What does not belong here.
- Recommended reading route.
- Links to related levels.
- Working rules.
- Maintenance notes.

## Anti-Duplication Rules

- Do not store full architecture, business context, contracts, or open questions in README.
- Use short summaries plus links.
- README files should point to source documents, not copy them.

## Template Body

```md
# <Repository or Container Name>

Short description of what this repository container or child repository is.

## Responsibility

This repository is responsible for:

- <Responsibility>

It is not responsible for:

- <Out-of-scope item>

## Start Here

Recommended reading route:

1. [<Document title>](<relative-link>)
2. [<Document title>](<relative-link>)

## Related Levels

- Parent: <local path or repository URL>
- Child: <local path or repository URL>

## Working Rules

- Keep this README as a navigation hub.
- Put detailed knowledge in focused documents.
- Link to the source of truth instead of copying content.

## Maintenance Notes

- Update this README when document routes or repository relationships change.
```

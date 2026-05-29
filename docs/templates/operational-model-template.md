# Operational Model Template

## Purpose

Use this template to define roles, workflow, decision-making, execution, handoff, acceptance, and documentation impact rules.

## Template Body

```md
# Operational Model

## Purpose

Describe why this operating model exists.

## Roles

| Role | Responsibility |
| --- | --- |
| Technical Owner | <Responsibility> |
| Business Owner | <Responsibility> |
| Architecture Partner | <Responsibility> |
| Codex Executor | Applies approved changes in the local development environment. |
| Human Contributors | <Responsibility> |

## Workflow

1. Discussion and analysis.
2. Engineering summary.
3. Execution.
4. Engineering handoff.
5. Acceptance review.

## Execution Rules

- Read the nearest README and related source documents first.
- Determine the owning documentation boundary before changing files.
- Check contract impact when a public contract may change.
- Change only files in the approved scope.
- Avoid inventing architecture, APIs, domain model, or business logic.
- Use templates when creating new documents.
- Preserve links instead of duplicating knowledge.

## Explicit Execution Permission

Codex Executor must not change files during analysis, discussion, review, comparison, or clarification unless the user explicitly asks to make changes.

Questions, analysis requests, reviews, comparisons, and planning prompts are not execution permission.

Valid execution permission examples:

- "Вноси изменения"
- "Обнови файлы"
- "Исправь это"
- "Применяй"
- "Делай"
- "Можно править"

If permission is unclear, Codex Executor must ask for confirmation before editing files.

Formal task descriptions define scope and acceptance criteria, but they still do not grant execution permission unless the user explicitly asks Codex Executor to apply changes.

## Handoff Format

- Context:
- Files created:
- Files updated:
- Checks performed:
- Constraints preserved:
- Documentation impact:
- Open questions:

## Documentation Impact

- Updated:
- Not updated because:
- New open questions:
- ADR needed:
- Contracts affected:
- Contract impact checked:
- Glossary affected:
- Next documentation step:
```

# AI Collaboration Template

## Purpose

Use this template to define how AI agents recover context, avoid assumptions, and keep engineering memory durable.

## Template Body

```md
# AI Collaboration Model

## Purpose

Describe how AI should support this repository container.

## Core Rules

- Start from the nearest relevant README.
- Follow documentation links before inferring architecture from code.
- Do not treat chat history as source of truth.
- Do not change files without explicit execution permission from the user.
- Write durable facts, decisions, questions, and contracts into Markdown.
- Keep parent, current container, and child repository boundaries separated.

## Context Recovery Route

1. Root README: `../README.md`
2. Documentation model: `documentation-model.md`
3. Operational model: `operational-model.md`
4. Task format: `task-format.md`
5. Repository relationships: `repository-relationships.md`
6. Contract impact model: `contract-impact.md`
7. Current state: `current-state.md`
8. Architecture: `architecture.md`
9. Open questions: `open-questions.md`

## Explicit Execution Permission

AI agents working as Codex Executor must not edit files just because the user asked a question, requested a review, asked for criticism, compared options, or discussed a possible change.

The user must explicitly ask for execution before files are changed.

Examples of execution permission:

- "Вноси изменения"
- "Обнови файлы"
- "Исправь это"
- "Применяй"
- "Делай"
- "Можно править"

When permission is ambiguous, ask for confirmation before editing.

## What AI Should Avoid

- Do not generate code from assumptions alone.
- Do not duplicate the same context across documentation boundaries.
- Do not leave important decisions only in chat.
- Do not silently change files outside the approved scope.
- Do not treat a formal task description as permission to edit unless the user explicitly asks for execution.
```

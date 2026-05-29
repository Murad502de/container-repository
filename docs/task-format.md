# Task Format

This document defines the required format for formal task descriptions.

The format is used to prepare clear work for humans and AI agents. It defines scope and acceptance criteria, but it does not grant Codex Executor permission to edit files unless the user explicitly asks for execution.

## Required Sections

Formal tasks must use these sections:

1. [Наименование задачи](#наименование-задачи)
2. [Описание](#описание)
3. [Действия](#действия)
4. [Результат](#результат)
5. [Критерии](#критерии)

## Наименование задачи

Short and precise task name without verbs.

The name should be understandable in a task list and reflect the essence of the task.

## Описание

Expanded task statement with context.

This section describes:

- why the task appeared;
- what problem or limitation exists now;
- which project the task belongs to;
- which business context matters;
- which inputs the executor must know.

Rules:

- Do not describe what must be done in this section.
- Do not use phrases like "необходимо", "требуется", or "нужно реализовать".
- Keep this section focused on problem statement and context.

## Действия

Structured list of execution steps.

Steps should be ordered in the expected execution sequence.

Use a numbered list when order matters.

## Результат

Expected final state after completion.

Write this section in positive form:

- what will be obtained;
- what will change;
- which artifact or solution will appear;
- which business problem this will help solve.

## Критерии

Acceptance criteria must always be a numbered list.

Each criterion must be objectively verifiable.

Example:

1. Document is prepared and placed in the agreed location.
2. All specified entities are transferred without data loss.
3. No errors are found during verification.
4. Result is approved by the responsible person.
5. All links and dependencies are checked and work correctly.

## Execution Permission

A task written in this format is not automatically permission to edit files.

Codex Executor may change files only after explicit execution permission from the user.

Examples:

- "Вноси изменения"
- "Обнови файлы"
- "Исправь это"
- "Применяй"
- "Делай"
- "Можно править"

If permission is unclear, Codex Executor must ask for confirmation.

## Related Documents

- [Operational model](operational-model.md)
- [AI collaboration model](ai-collaboration.md)
- [Working principles](working-principles.md)

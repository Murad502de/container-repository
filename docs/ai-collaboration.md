# AI Collaboration Model

This document defines how AI tools should work with this repository container.

AI collaboration rules are part of the broader [operational model](operational-model.md). This document focuses on context recovery, safe execution, and durable project memory.

## Purpose

AI should act as an engineering accelerator, not as a source of undocumented architecture.

Repository documentation is the source of truth. AI agents must use it to recover context, route work to the correct boundary, and keep engineering memory durable across chats, IDE sessions, devices, and contributors.

## Core Rules

- Start from the nearest relevant README.
- Follow README links before inferring architecture from code.
- Do not treat chat history as the only source of truth.
- Treat Markdown documentation as durable project memory.
- Do not change files without explicit execution permission from the user.
- Do not start implementation work before the relevant current state, target model, and open questions are understood.
- Do not mix parent, current container, and child repository documentation.
- Write important new knowledge into the right Markdown document.
- Keep README files as navigation hubs.
- Link to source documents instead of copying their content.
- Prefer focused documents over large catch-all documents.

## Context Recovery Route

When starting from the repository root, read:

1. [Root README](../README.md)
2. [Operational model](operational-model.md)
3. [Documentation model](documentation-model.md)
4. [Working principles](working-principles.md)
5. [Task format](task-format.md)
6. [Repository relationships](repository-relationships.md)
7. [Contract impact model](contract-impact.md)
8. [Technology stack](technology-stack.md)
9. [System overview](system-overview.md)
10. [Business context](business-context.md)
11. [Architecture](architecture.md)
12. [Open questions](open-questions.md)
13. [Repositories index](../repositories/README.md)

When the work concerns a child repository, continue from that repository's README.

## Documentation Before Code

Before writing or changing code, document or verify:

- the current state of the relevant system area;
- working scenarios that must be preserved;
- known problems and risks;
- requirements and constraints;
- target architecture and boundaries;
- unresolved questions;
- accepted architecture decisions.

## Decision Handling

Use the correct document type for each kind of knowledge:

- Current state goes to `current-state.md`.
- Unresolved questions go to `open-questions.md`.
- Accepted decisions go to ADR files.
- API, event, and integration agreements go to contracts.
- Contract scope, registry, consumers, and impact go to `contract-impact.md`.
- Terms go to `glossary.md`.
- Long explanations should become focused documents and be linked from README hubs.

## Chat To Repository Workflow

Chat is useful for discussion, but it is not the source of truth.

When a discussion produces durable project knowledge:

1. Convert the discussion into a concise engineering summary.
2. Put each type of knowledge into the correct Markdown document.
3. Link related documents instead of duplicating the same content.
4. Use ADRs only for accepted decisions.
5. Use `open-questions.md` for unresolved questions.
6. Commit documentation updates through the normal project workflow.

## Collaboration With The Project Owner

For substantial changes, the default workflow is:

1. Read the relevant documentation and code.
2. Explain findings or propose a change package.
3. Wait for approval when the task requires it.
4. Apply the approved changes.
5. Run checks.
6. Summarize what changed and what remains open.

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
- Do not create large generic documents without a clear owner.
- Do not duplicate the same context across boundaries.
- Do not duplicate source documents when a link is enough.
- Do not move child repository details into the current container README.
- Do not leave important decisions only in chat.
- Do not silently change files outside the approved scope.
- Do not treat a formal task description as permission to edit unless the user explicitly asks for execution.

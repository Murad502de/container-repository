# Working Principles

This document records stable principles for future work in this repository container.

Use it for durable rules that should guide decisions across repositories, contributors, and AI sessions.

## Principles

### Documentation Is Engineering Memory

Important facts, decisions, questions, contracts, and terms must live in Markdown documentation.

Chats and local notes can support discussion, but they are not source of truth until the relevant knowledge is recorded in the right document.

### Boundaries Come First

Before changing architecture, contracts, or implementation, identify the local responsibility boundary:

- parent container;
- current container;
- child repository.

Put information at the nearest boundary that owns it.

### Current State Is Not Target Architecture

Current state documents observed facts.

Architecture documents intended target structure.

Do not present existing behavior as the desired future unless that decision is explicit.

### Open Questions Stay Visible

Uncertainty should not be hidden in implementation.

Put unresolved questions in the nearest relevant `open-questions.md` and link to them from related documents.

### Decisions Need Durable Records

Architecture decisions belong in ADR files.

Do not leave accepted decisions only in chat, issue comments, or commit messages.

### Contracts Own Boundaries

API, event, and integration behavior belongs in `docs/contracts`.

Architecture and integration maps may summarize contracts, but they must link to the contract documents.

Public contract changes must follow [contract impact](contract-impact.md): repository tree defines ownership, contract graph defines impact.

### README Files Route Readers

README files answer:

- where am I;
- what does this level own;
- where should I read next.

They should not become large archives of detailed knowledge.

### Links Beat Duplication

If a source document already owns the knowledge, link to it.

If a section starts duplicating another document, replace it with a short summary and a link.

### Placeholders Are Better Than Invented Facts

Use placeholders such as `<project-name>` or `Not documented yet` when facts are unknown.

Do not invent client, domain, API, architecture, or implementation details to make a template look complete.

### Execution Requires Explicit Permission

Analysis, discussion, criticism, comparison, and planning do not authorize file changes.

Codex Executor may edit files only after the user explicitly asks for execution.

If permission is unclear, Codex Executor must ask for confirmation.

### Documentation Is Stack-Agnostic

The documentation model must not depend on a specific programming language, framework, database, infrastructure provider, or toolchain.

Technology choices should be isolated in [technology-stack.md](technology-stack.md), ADRs, architecture, technical design, or child repository development docs.

Changing the stack should not require rewriting README files, documentation model, operational model, AI collaboration rules, or working principles.

## Related Documents

- [Documentation model](documentation-model.md)
- [Operational model](operational-model.md)
- [AI collaboration model](ai-collaboration.md)
- [Task format](task-format.md)
- [Repository relationships](repository-relationships.md)
- [Contract impact model](contract-impact.md)
- [Technology stack](technology-stack.md)

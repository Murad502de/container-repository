# Operational Model

This document defines how project participants work together.

The key principle is: repository documentation is the project source of truth. Chats, verbal discussions, local notes, and AI conclusions are not source of truth until important decisions, facts, questions, or constraints are recorded in the appropriate Markdown document.

## Purpose

This model keeps project work controlled, consistent, and reviewable.

It exists so that:

- decisions are not lost in chat;
- assumptions are not treated as facts;
- implementation does not start without context;
- AI and human contributors understand their roles;
- documentation remains durable project memory;
- acceptance review can verify work against clear operating rules.

## Participants And Roles

Use the roles that match the project. A small project may assign several roles to one person.

### Technical Owner

The Technical Owner owns technical direction, priorities, architecture acceptance, and final technical decisions.

The Technical Owner:

- sets the project direction;
- approves key decisions;
- corrects wrong conclusions;
- accepts work results;
- defines priorities;
- makes the final decision when participants disagree.

### Business Owner

The Business Owner defines business goals, constraints, users, and product expectations.

Business input must be translated into durable requirements, open questions, business context, or decisions before implementation relies on it.

### Architecture Partner

The Architecture Partner helps analyze, challenge, structure, and verify decisions.

This role may be performed by a human architect, ChatGPT, or another AI assistant.

The Architecture Partner must:

- distinguish facts, hypotheses, and decisions;
- identify contradictions and risks;
- propose simpler and more stable options;
- recommend where conclusions must be documented;
- prepare engineering summaries for execution.

### Codex Executor

Codex Executor applies approved changes in the local development environment.

Codex Executor must:

- read current README files and related documents first;
- work from repository documentation as source of truth;
- avoid changing files outside the agreed scope;
- propose a change plan before substantial changes;
- apply changes in manageable batches;
- run relevant checks;
- return an engineering handoff after execution.

### Human Contributors

Human contributors work from the same source of truth as AI assistants.

They must:

- read current README files before starting work;
- check related documents;
- record important decisions and questions in documentation;
- avoid duplicating knowledge between documents;
- raise contradictions for discussion.

## Main Workflow Cycle

Project work is performed cyclically:

1. Discussion and analysis.
2. Engineering summary.
3. Execution.
4. Engineering handoff.
5. Acceptance review.

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

Formal task descriptions written in the [task format](task-format.md) define scope and acceptance criteria, but they still do not grant execution permission unless the user explicitly asks Codex Executor to apply changes.

## Discussion And Analysis

Discussion is used to understand the task, identify risks, determine documentation level, and decide whether the work creates:

- a fact for `current-state.md`;
- a question for `open-questions.md`;
- a decision for an ADR;
- a term for `glossary.md`;
- a contract for `docs/contracts`;
- a requirement for `docs/specs/requirements`;
- an architecture statement for `architecture.md`;
- an engineering summary for execution.

## Engineering Summary

Before substantial execution, prepare a summary that answers:

- what was discussed;
- which conclusions were reached;
- which decisions were accepted;
- which questions remain open;
- which documents must be updated;
- which files must not be changed;
- which checks must be performed;
- what result is expected.

## Execution Rules

During execution:

- read the nearest README;
- read related source documents;
- determine the documentation level;
- change only files in scope;
- avoid inventing architecture, APIs, domain model, or business logic;
- use templates when creating new documents;
- preserve links instead of duplication;
- update documentation together with code when code affects project memory.

## Engineering Handoff

After completing a task, return a handoff with:

- task context;
- files created;
- files updated;
- what was not done;
- checks performed;
- constraints preserved;
- documentation impact;
- open questions;
- suggested next step.

## Acceptance Review

Acceptance review checks:

- whether the result matches the task;
- whether documentation levels were preserved;
- whether knowledge duplication was avoided;
- whether invented facts appeared;
- whether unrelated files changed;
- whether links work correctly;
- whether documentation impact was handled.

## Documentation Impact Rule

Every task must end with a documentation impact check.

Use this format:

```md
Documentation impact:
- Updated:
- Not updated because:
- New open questions:
- ADR needed:
- Contracts affected:
- Glossary affected:
- Next documentation step:
```

If documentation was not updated, state why.

## Decision-Making Rules

When priorities conflict, use this order:

```text
Correctness > agreement
Facts > assumptions
Simplicity > excess
System thinking > local decisions
Documentation > chat memory
```

## Decision Recording Rules

A decision is accepted only after:

1. it has been discussed;
2. alternatives or constraints have been checked;
3. the responsible owner has confirmed it;
4. it has been recorded in the appropriate document.

If the decision is architectural, record it in ADR.

If the decision concerns product behavior, record it in business context, requirements, or another appropriate document.

If the decision concerns system interaction, record it in contracts or integration map.

## Related Documents

- [Documentation model](documentation-model.md)
- [AI collaboration model](ai-collaboration.md)
- [Working principles](working-principles.md)
- [Task format](task-format.md)
- [Repository pairing](repository-pairing.md)
- [Technology stack](technology-stack.md)
- [Open questions](open-questions.md)

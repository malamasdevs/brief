---
name: trim
description: Use when reviewing AI-generated code to catch architectural drift — naming, patterns, abstractions, and boundary violations that don't fit the existing codebase.
---

# trim

You are reviewing AI-generated code for architectural consistency.

Your job is not to judge whether the code works.
Your job is to check whether it fits the codebase it is going into.

For every change, check:

## Naming

Does it follow the naming conventions already used in this codebase?
Use domain language — not generic names like `data`, `result`, `temp`.
If the codebase calls it an invoice, call it an invoice.

## Patterns

Does it use the same patterns as the surrounding code?
If the codebase uses async/await, use async/await.
If data access goes through a repository, don't query the DB directly.
If there is a service layer, don't bypass it.

## Abstractions

Does it reuse existing utilities, hooks, or helpers?
Search the codebase before creating something new.
If a utility already exists for this, flag it and point to it.

## Boundaries

Does logic belong in the layer where it was added?
Business logic should not leak into UI components.
Infrastructure concerns should not appear in business logic.
Domain logic should not live in controllers or route handlers.

## Drift

Does this PR move the codebase away from how it was designed?
Flag anything that is technically correct but architecturally inconsistent with the rest of the codebase.

## Important

Do not rewrite. Flag and explain. The engineer decides.
This file guides — it does not enforce on its own.
Use it in your code review flow, in Claude Code, or in Cursor before merging AI-generated changes.

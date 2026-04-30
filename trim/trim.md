# trim

A skill file for keeping AI-generated code consistent with your existing codebase.

## What problem this solves

AI generates code based on what it sees in context.
If your existing patterns are not in the window, it invents its own.

Over time this produces:

- naming that doesn't match your domain language
- patterns that bypass layers the rest of the codebase uses
- utilities that already exist, rebuilt from scratch
- logic that ends up in the wrong layer

None of it breaks. It just makes the codebase harder to read, change, and hand off.

## What trim does

It gives the AI context about your existing patterns before it generates new code.

It checks:

- **naming** — does it match your domain language?
- **patterns** — does it use the layers already in place?
- **abstractions** — does it reuse what already exists?
- **boundaries** — is logic in the right layer?

It flags drift. It does not catch bad logic or security issues — those are different problems.
You still review everything. You still decide what ships.

## How to use it

Drop `SKILL.md` where your tool expects skills.

Works with Claude Code, Cursor, and most agent-based coding tools.

If your tool doesn't support skills directly, copy the rules into your system prompt or project instructions.

## What this doesn't do

- Does not catch broken logic
- Does not catch security issues
- Does not enforce anything automatically
- Does not replace code review

## Part of the malamasdevs skill collection

- `brief.md` — cleaner AI output
- `trim.md` — consistent AI code

# malamasdevs skills

A small collection of skill files for working better with AI.

Each skill is a focused, copy-paste-ready instruction set. Drop the `SKILL.md` where your tool expects skills (Claude Code, Cursor, etc.) or paste the rules into your system prompt.

## Skills

- [**brief**](./brief/brief.md) — cleaner AI output. Fewer words, faster reading, lower token cost.
- [**trim**](./trim/trim.md) — consistent AI code. Catches drift in naming, patterns, abstractions, and boundaries before it compounds.

## Repo layout

Each skill folder contains:

- `SKILL.md` — the operational prompt the AI reads
- `<skill>.md` — the human-readable explainer

```
.
├── brief/
│   ├── SKILL.md
│   └── brief.md
└── trim/
    ├── SKILL.md
    └── trim.md
```

## How to use

1. Pick the skill you want.
2. Drop its `SKILL.md` into your tool's skills directory.
3. Or copy the rules into your system prompt or project instructions.

## License

MIT

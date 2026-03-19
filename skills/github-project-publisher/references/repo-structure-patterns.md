# Repo Structure Patterns

Use these as lightweight patterns, not strict templates.

## Pattern 1 — Skill collection repo

```text
project/
├── README.md
├── docs/
├── skills/
└── dist/
```

Use when publishing AgentSkills plus packaged `.skill` outputs.

## Pattern 2 — Project + docs repo

```text
project/
├── README.md
├── docs/
├── src/
└── assets/
```

Use when the project includes implementation code plus user-facing docs.

## Pattern 3 — Contest submission repo

```text
project/
├── README.md
├── docs/
├── assets/
├── demo/
└── deliverables/
```

Use when the repo must support judges, submission forms, and demos.

## Rule of thumb
Choose the smallest structure that still makes the project understandable.

# Project Agent Template

Use this template as the default starting point for a focused child-agent repository.

## Minimum recommended structure

```text
<agent>/
├── AGENTS.md
├── README.md
├── docs/
│   ├── principles/
│   ├── workflow/
│   └── quality/
└── projects/        # only when instance-specific state is needed
```

Do not create empty directories or vendor-specific files without a real need.

## Creation checklist

Before generating files, define:

- purpose
- non-goals
- core priorities
- common task types
- acceptance criteria
- what belongs in always-on context
- what belongs in on-demand guidance
- what belongs in project state

After the first real task, audit the repository before adding more structure.

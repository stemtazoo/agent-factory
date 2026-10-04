# Agent Factory Research Changelog

This file records methodology-level research findings and why they matter.

Do not treat every entry as a permanent rule. Durable lessons should be promoted into `docs/principles/` or `docs/patterns/`.

## 2026-10-04 — Initial architecture

Initial design direction:

- Keep `AGENTS.md` as a concise routing and priority document.
- Store detailed guidance outside always-on instructions.
- Separate reusable methodology from child-agent domain knowledge.
- Separate vendor-neutral principles from vendor-specific capabilities.
- Avoid converting one-off corrections directly into global rules.
- Use the first real child agent as an architecture test before adding advanced mechanisms such as many skills, subagents, hooks, or automation.

Primary vendors to monitor:

- OpenAI
- Anthropic
- GitHub

Research notes should prefer official primary sources and record the date checked.

## 2026-10-04 — Google and Microsoft supplementary review

Added Google and Microsoft as supplementary architecture references.

Google findings:

- Treat agent work as a lifecycle that includes evaluation and observability.
- Keep task-specific operational knowledge modular.
- Combine agent behavior with tests, linting, evaluation datasets, and other measurable checks where practical.

Microsoft findings:

- Use agents where reasoning or ambiguity adds value.
- Prefer deterministic code for validation, routing, transformation, and other known-correct operations.
- Define delegation, approval, and responsibility boundaries explicitly.
- Do not introduce additional agents without a clear responsibility that justifies orchestration cost.

Decision:

- Do not add Google or Microsoft to the README primary-reference list yet.
- Keep them under `docs/vendors/` as supplementary sources.
- Revisit promotion into shared principles after practical validation in child-agent projects.

## 2026-10-04 — First practical audit feedback

Applied Agent Factory principles to `stemtazoo/python-app-starter-kit`.

Observed result:

- The repository's overall methodology was already sound.
- The main issue was information placement rather than missing policy.
- `AGENTS.md` contained many detailed procedures that were also represented in task-specific docs.
- Refactoring `AGENTS.md` toward priorities, MUSTs, boundaries, and routing reduced always-on content substantially without removing the beginner-support behavior that defined the agent.
- Adding a docs index clarified which file was the canonical home for each detailed rule.
- Medium-priority improvements were intentionally deferred after the two highest-value changes were completed.

Promoted lessons:

1. Use **MUST / HOW separation** as an audit test:
   - always-on instructions hold priorities and non-negotiable behavior
   - detailed docs hold procedures and examples
2. Give every detailed rule **one canonical home** and reference it elsewhere instead of duplicating full guidance.
3. Treat audits as prioritization exercises, not automatic full rewrites. Implement the smallest high-value change first and validate it before expanding.

Not promoted:

- No fixed maximum size or line count for `AGENTS.md`.
- Size alone is not the target; relevance to most tasks is the deciding factor.

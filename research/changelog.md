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

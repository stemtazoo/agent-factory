# Agent Design Principles

These are durable, vendor-neutral principles for repositories managed by Agent Factory.

## 1. Give the agent a narrow job

An agent repository should have a clear purpose, boundaries, and definition of success.

If the repository is responsible for too many unrelated activities, split responsibilities before adding more instructions.

## 2. Keep always-on context small

Instructions that are loaded for every task should contain only information needed for most tasks.

Detailed procedures, references, examples, vendor notes, and rare edge cases belong in separate files loaded when relevant.

A useful working distinction is:

- `AGENTS.md` should primarily hold **MUSTs, priorities, boundaries, and routing guidance**.
- Detailed docs should primarily hold **HOWs, examples, task procedures, and environment-specific details**.

This is a design test, not a rigid file-size rule. An instruction belongs in always-on context only when most tasks genuinely need it.

## 3. Separate instruction layers

Use three conceptual layers:

1. **Global rules** — stable priorities and boundaries.
2. **Task guidance** — workflows used for a class of tasks.
3. **Project state** — temporary or instance-specific requirements, observations, and decisions.

A lower layer may refine a higher layer but should not silently override core priorities.

## 4. Give each detailed rule one canonical home

Every detailed rule should have one primary source of truth.

For example:

- repository-wide priorities may live in `AGENTS.md`
- troubleshooting details may live in a troubleshooting guide
- vendor-specific findings may live under `docs/vendors/`
- project-specific revisions may live with that project

Other files may link to or summarize the canonical rule, but should avoid maintaining a second full copy.

This reduces drift, conflicting updates, and duplicated context.

## 5. Prefer explicit priority over accumulated exceptions

When instructions compete, establish an order of priority.

Do not solve every conflict by adding another exception.

## 6. Promote rules cautiously

One failure is evidence about one case, not proof of a universal rule.

Promote a lesson only after deciding whether it is:

- project-specific
- a repeated failure pattern
- a reusable pattern
- a durable global principle

## 7. Make success testable

Where practical, define acceptance criteria that can be reviewed or checked mechanically.

Prefer deterministic validation for dimensions, schemas, file structure, formatting, tests, and other measurable constraints.

## 8. Keep vendor-specific behavior at the edges

Use common repository concepts for the core methodology.

Add vendor-specific files only when a vendor needs behavior that cannot be expressed cleanly through shared instructions.

## 9. Preserve useful history without loading it every time

Keep research notes, revision history, and failure examples available, but do not make them mandatory context for unrelated tasks.

## 10. Audit before expanding

When an agent underperforms, first determine whether the cause is:

- missing information
- conflicting instructions
- excessive context
- unclear priority
- weak workflow
- missing validation
- tool limitations

Do not automatically respond by making the prompt longer.

## 11. Let real work shape the architecture

Start small. Add structure after actual tasks reveal a recurring need.

An audit may identify several valid improvements, but that does not mean all of them should be implemented immediately. Prefer the smallest change that solves the observed problem, then validate it in real use before expanding further.

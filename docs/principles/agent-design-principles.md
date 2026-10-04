# Agent Design Principles

These are durable, vendor-neutral principles for repositories managed by Agent Factory.

## 1. Give the agent a narrow job

An agent repository should have a clear purpose, boundaries, and definition of success.

If the repository is responsible for too many unrelated activities, split responsibilities before adding more instructions.

## 2. Keep always-on context small

Instructions that are loaded for every task should contain only information needed for most tasks.

Detailed procedures, references, examples, vendor notes, and rare edge cases belong in separate files loaded when relevant.

## 3. Separate instruction layers

Use three conceptual layers:

1. **Global rules** — stable priorities and boundaries.
2. **Task guidance** — workflows used for a class of tasks.
3. **Project state** — temporary or instance-specific requirements, observations, and decisions.

A lower layer may refine a higher layer but should not silently override core priorities.

## 4. Prefer explicit priority over accumulated exceptions

When instructions compete, establish an order of priority.

Do not solve every conflict by adding another exception.

## 5. Promote rules cautiously

One failure is evidence about one case, not proof of a universal rule.

Promote a lesson only after deciding whether it is:

- project-specific
- a repeated failure pattern
- a reusable pattern
- a durable global principle

## 6. Make success testable

Where practical, define acceptance criteria that can be reviewed or checked mechanically.

Prefer deterministic validation for dimensions, schemas, file structure, formatting, tests, and other measurable constraints.

## 7. Keep vendor-specific behavior at the edges

Use common repository concepts for the core methodology.

Add vendor-specific files only when a vendor needs behavior that cannot be expressed cleanly through shared instructions.

## 8. Preserve useful history without loading it every time

Keep research notes, revision history, and failure examples available, but do not make them mandatory context for unrelated tasks.

## 9. Audit before expanding

When an agent underperforms, first determine whether the cause is:

- missing information
- conflicting instructions
- excessive context
- unclear priority
- weak workflow
- missing validation
- tool limitations

Do not automatically respond by making the prompt longer.

## 10. Let real work shape the architecture

Start small. Add structure after actual tasks reveal a recurring need.

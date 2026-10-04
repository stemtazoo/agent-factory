# Instruction Priority

Use this model when designing or auditing a child agent.

## Recommended hierarchy

```text
Core purpose and non-negotiable priorities
                  ↓
Reusable task workflow
                  ↓
Project-specific requirements
                  ↓
Current revision request
```

A current revision request may change a local detail, but it must not silently break higher-priority constraints.

## Example

For a papercraft agent:

1. The model must be buildable.
2. Dimensions must remain consistent.
3. Vehicle proportions should be preserved.
4. Vehicle-specific details should be represented.
5. A revision may request larger rear lights.

The fifth instruction cannot justify violating the first two.

## Conflict handling

When two instructions conflict:

1. Identify their levels.
2. Apply the higher-priority rule.
3. Explain the tradeoff when it materially affects the output.
4. If the conflict recurs, fix the architecture rather than adding another exception.

## Avoid instruction duplication

A rule should have one canonical home.

Other files may link to it or summarize why it matters, but should not maintain separate divergent copies.

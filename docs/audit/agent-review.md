# Agent Audit

Use this checklist when reviewing a child agent.

## Scope

- Is the purpose clear?
- Are non-goals or boundaries clear?
- Does another agent already serve the same role?

## Instructions

- Is `AGENTS.md` acting as an entry point rather than a knowledge dump?
- Are global priorities explicit?
- Are detailed workflows separated from always-on rules?
- Does `AGENTS.md` mainly contain MUSTs, priorities, boundaries, and routing rather than long HOW-to procedures?
- Are there duplicated or conflicting instructions?
- Does each detailed rule have one canonical home?
- Have one-off corrections leaked into global rules?

## Context

- Is every always-loaded instruction needed for most tasks?
- Could examples, history, vendor notes, environment-specific procedures, or long troubleshooting steps move to on-demand files?
- Are project-specific details stored separately?
- Is context being reduced because it is unnecessary, rather than merely to hit an arbitrary size target?

## Duplication and canonical ownership

For repeated guidance, identify which file should be authoritative.

Examples:

- `AGENTS.md`: non-negotiable rules, priorities, routing
- task docs: detailed workflow and examples
- vendor docs: vendor-specific capabilities and findings
- project files: instance-specific state and revisions

Prefer links and short summaries over maintaining multiple full copies of the same rule.

## Validation

- Are acceptance criteria defined?
- Can deterministic checks replace subjective prompt instructions?
- Are failure modes documented without forcing every failure example into context?

## Vendor freshness

- Are vendor-specific assumptions still current?
- Are official primary sources used where practical?
- Is a vendor-specific feature being mistaken for a universal best practice?

## Result

Classify recommendations as:

- no change
- local cleanup
- workflow improvement
- architecture change
- vendor-specific update

Prioritize recommendations by expected benefit and urgency.

An audit is **not** a mandate to implement every improvement found. Prefer the smallest change that solves the current problem, then observe the result before making lower-priority changes.

When appropriate, leave medium- or low-priority findings explicitly deferred rather than expanding the agent immediately.

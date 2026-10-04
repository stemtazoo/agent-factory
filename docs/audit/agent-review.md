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
- Are there duplicated or conflicting instructions?
- Have one-off corrections leaked into global rules?

## Context

- Is every always-loaded instruction needed for most tasks?
- Could examples, history, or vendor notes be moved to on-demand files?
- Are project-specific details stored separately?

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

Prefer the smallest change that solves the observed problem.

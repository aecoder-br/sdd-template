---
name: sdd-quality-review
description: Quality review for Spec Driven Design implementation plans, tasks, and diffs. Use when Codex must evaluate tests, clean code, SOLID fit, simplicity, over-engineering, maintainability, Definition of Done, and validation evidence.
---

# SDD Quality Review

Use this skill to review whether a feature is ready to implement or merge. Stay
stack-agnostic and judge against the repository's existing architecture.

## Review Focus

- Requirements are traceable from spec to plan to tasks.
- Tests match risk: unit for logic, contract for interfaces, integration for
  critical flows, E2E only for high-value journeys.
- Implementation preserves local patterns and avoids unnecessary abstraction.
- SOLID and clean-code guidance improves maintainability without forcing a
  pattern the repo does not need.
- Refactors are separated from behavior where practical.
- Definition of Done and quality gates are satisfied or explicitly waived.

## Output

Return:

- blocking findings first;
- non-blocking improvements second;
- missing tests or validation;
- over-engineering or under-engineering risks;
- final readiness assessment.

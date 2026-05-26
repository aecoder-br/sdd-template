<!--
Sync Impact Report
Version change: template -> 1.0.0
Modified principles:
- PRINCIPLE_1_NAME -> I. Code Quality Is a Release Gate
- PRINCIPLE_2_NAME -> II. Tests Define Behavioral Confidence
- PRINCIPLE_3_NAME -> III. User Experience Consistency Is Mandatory
- PRINCIPLE_4_NAME -> IV. Performance Budgets Are Requirements
- PRINCIPLE_5_NAME -> V. Technical Decisions Must Be Traceable
Added sections:
- Implementation Standards
- Delivery Workflow and Quality Gates
Removed sections:
- None
Templates requiring updates:
- .specify/templates/plan-template.md: updated
- .specify/templates/spec-template.md: updated
- .specify/templates/tasks-template.md: updated
- .specify/templates/commands/*.md: not present in this checkout
Follow-up TODOs:
- Fix .specify/extensions/git/scripts/powershell/initialize-repo.ps1 encoding so the
  mandatory before_constitution hook can parse under PowerShell.
-->
# SDD Template Constitution

## Core Principles

### I. Code Quality Is a Release Gate
All implementation work MUST keep the codebase simple, readable, maintainable,
and aligned with the existing architecture. New abstractions MUST be justified by
real duplication, complexity, or a stable domain boundary. Changes MUST preserve
module ownership, naming conventions, error-handling patterns, and formatting
rules already established by the project. Any intentional deviation MUST be
recorded in the plan with the tradeoff and the rejected simpler alternative.

Rationale: Consistent, maintainable code reduces review cost and prevents local
shortcuts from becoming long-term architecture constraints.

### II. Tests Define Behavioral Confidence
Every feature or bug fix MUST define its expected behavior in independently
verifiable terms before implementation is considered complete. Automated tests
MUST cover new business logic, changed contracts, regressions, critical user
journeys, and risk-bearing edge cases. If a test cannot be automated in the
current scope, the plan MUST document the manual verification path, the reason
automation was deferred, and the residual risk. Failing or skipped tests MUST
block delivery unless an explicit documented waiver is approved.

Rationale: Tests are the durable proof that requirements survive refactoring,
integration, and future changes.

### III. User Experience Consistency Is Mandatory
User-facing changes MUST reuse established interaction patterns, terminology,
layout conventions, accessibility expectations, and visual systems before
introducing new UI behavior. Each user story that changes the interface MUST
state how it preserves consistency with adjacent workflows and how users can
complete the primary task without unnecessary friction. Accessibility,
responsive behavior, loading states, empty states, error states, and destructive
actions MUST be accounted for when applicable.

Rationale: A consistent product experience lets users transfer knowledge across
features and reduces support, training, and regression risk.

### IV. Performance Budgets Are Requirements
Performance-sensitive work MUST define measurable targets or preserve existing
budgets for latency, throughput, memory, bundle size, startup time, rendering
stability, or resource consumption as appropriate to the feature. Implementation
plans MUST identify expected scale, hot paths, expensive operations, caching or
batching strategy, and measurement method. Changes that may degrade performance
MUST include evidence from tests, profiling, benchmarks, or reasoned analysis
before release.

Rationale: Performance is a functional requirement when it affects usability,
operating cost, reliability, or scale.

### V. Technical Decisions Must Be Traceable
Material technical decisions MUST be captured in the spec, plan, research notes,
or an architecture decision record with enough context for later maintainers to
understand the chosen approach. The record MUST include constraints, options
considered, implementation consequences, and validation expectations. Decisions
that affect shared contracts, data models, runtime behavior, security posture,
or cross-feature UX MUST be reviewed against this constitution before tasks are
generated.

Rationale: Traceable decisions keep implementation choices tied to requirements
instead of individual memory or hidden assumptions.

## Implementation Standards

Feature work MUST start from the current plan and the real repository structure.
Plans MUST name the concrete files, modules, APIs, schemas, commands, and user
flows affected by the change. Generated specs and tasks MUST avoid vague work
items; each requirement and task needs a clear owner surface, validation method,
and user or system outcome.

Code changes MUST prefer existing project utilities, libraries, components, and
test harnesses. New dependencies, broad refactors, global state, background
work, caching, concurrency, persistence, or network behavior MUST be justified
in the plan and paired with failure-mode handling. Security, privacy, and data
integrity constraints MUST be treated as quality requirements, not polish.

## Delivery Workflow and Quality Gates

Before implementation, the plan MUST pass a Constitution Check covering code
quality, testing strategy, UX consistency, performance targets, and decision
traceability. After design, the same check MUST be repeated with concrete
evidence from the selected architecture and contracts.

Tasks MUST be organized so independently valuable user stories can be built and
verified in priority order. Required tests and validation tasks MUST appear in
the task list before or alongside the implementation they protect. Delivery is
not complete until the documented validation commands or manual checks have
been run, their results recorded, and any unresolved risks called out.

## Governance

This constitution supersedes conflicting project practices for specification,
planning, task generation, implementation, review, and release decisions.
Reviewers and implementers MUST use it as the decision filter whenever tradeoffs
involve scope, architecture, tests, UX, performance, or delivery readiness.

Amendments require a written change to this file, a Sync Impact Report, and a
review of dependent templates and runtime guidance. Versioning follows semantic
versioning: MAJOR for incompatible governance or principle redefinitions, MINOR
for new principles or materially expanded obligations, and PATCH for wording
clarifications that do not change obligations.

Each feature plan MUST document constitution compliance. Any approved exception
MUST name the principle affected, the reason, the mitigation, the owner, and the
expiration or revisit condition. Recurring exceptions MUST trigger a
constitution amendment or a template update rather than remaining informal.

**Version**: 1.0.0 | **Ratified**: 2026-05-26 | **Last Amended**: 2026-05-26

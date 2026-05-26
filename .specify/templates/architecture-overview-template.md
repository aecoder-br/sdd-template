# Architecture Overview: [PROJECT OR FEATURE]

**Date**: [DATE]
**Owner**: [Name or role]
**Related artifacts**: [spec.md, plan.md, ADRs]

## Context

[Describe users, system boundary, external dependencies, and important quality
attributes.]

## C4-Lite View

### System Context

- **Users/Actors**: [List]
- **System**: [Name and responsibility]
- **External systems**: [List]

### Containers or Major Modules

| Module | Responsibility | Interfaces | Data |
|--------|----------------|------------|------|
| [Module] | [What it owns] | [APIs/events/UI] | [Data owned/used] |

## Cross-Cutting Concerns

- **Security**: [Auth, authorization, secrets, data protection]
- **Reliability**: [Failure modes, retries, recovery]
- **Observability**: [Logs, metrics, traces, support signals]
- **Performance**: [Budgets, hot paths, scale expectations]
- **Maintainability**: [Boundaries, naming, dependency rules]

## Decisions and Open Questions

- **ADRs**: [Links]
- **Open questions**: [Items that must be resolved before implementation]

# Definition of Done: [FEATURE NAME]

**Feature**: [Link to spec.md]
**Plan**: [Link to plan.md]
**Tasks**: [Link to tasks.md]
**Owner**: [Name or role]
**Date**: [DATE]

## Requirement Traceability

- [ ] Each delivered behavior maps to a requirement or accepted change
- [ ] Each user story remains independently demonstrable
- [ ] Scope changes are reflected in spec, plan, and tasks
- [ ] Out-of-scope work is documented

## Code Quality

- [ ] Implementation follows existing architecture and naming patterns
- [ ] New abstractions are justified by real duplication or a stable boundary
- [ ] Refactors are separated from behavior changes where practical
- [ ] Error handling and failure modes are intentional
- [ ] No unrelated files or generated artifacts are included

## Testing and Validation

- [ ] Unit tests cover new or changed logic
- [ ] Contract tests cover changed interfaces or APIs
- [ ] Integration tests cover critical flows
- [ ] E2E tests are included only for high-value journeys or documented risk
- [ ] Manual checks are documented with reason and residual risk
- [ ] Required validation commands have been run and recorded

## Security, Privacy, and Operations

- [ ] Input validation, auth/authz, secrets, and sensitive data are addressed
- [ ] Logs avoid secrets and unnecessary personal data
- [ ] Dependency and supply-chain impacts are understood
- [ ] Observability and support needs match the feature risk
- [ ] Runbook or release checklist exists when required by plan.md

## Documentation and Traceability

- [ ] README, docs, examples, or runbooks are updated when behavior changes
- [ ] ADR exists for material architecture, contract, data, security, runtime,
      dependency, performance, or cross-feature UX decisions
- [ ] Final notes include validation evidence and unresolved risks

# Security Review: [FEATURE NAME]

**Feature**: [Link to spec.md]
**Reviewer**: [Name or role]
**Date**: [DATE]

## Scope

- **Changed surfaces**: [APIs, UI, jobs, storage, tools, generated code]
- **Data involved**: [Public, internal, sensitive, personal, secrets, N/A]
- **External systems**: [MCP, SaaS, cloud, package registries, APIs, N/A]

## Review Checklist

- [ ] Inputs are validated and normalized at trust boundaries
- [ ] Authentication and authorization are explicit where required
- [ ] Sensitive data and secrets are not logged or committed
- [ ] Dependencies and generated artifacts are understood
- [ ] Error handling avoids information disclosure
- [ ] Tool permissions follow least agency and least privilege
- [ ] Prompt injection or context poisoning risks are addressed where AI is used
- [ ] Human approval is required for destructive or external mutating actions

## Findings

| ID | Severity | Finding | Mitigation | Owner |
|----|----------|---------|------------|-------|
| SEC-001 | [Low/Med/High] | [Finding] | [Mitigation] | [Owner] |

## Decision

- [ ] Approved
- [ ] Approved with follow-up
- [ ] Blocked

**Notes**: [Rationale and residual risk]

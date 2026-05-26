# Quality Gates: [FEATURE NAME]

**Feature**: [Link to spec.md]
**Created**: [DATE]
**Owner**: [Name or role]

Use this template to decide which gates apply before implementation and before
release. Mark N/A only with a short rationale.

## Planning Gates

| Gate | Required? | Evidence |
|------|-----------|----------|
| Constitution check passed | Yes | [plan.md section] |
| Requirements are testable | Yes | [spec.md section] |
| Ambiguities clarified | [Yes/No/N/A] | [clarification notes] |
| Architecture decision recorded | [Yes/No/N/A] | [ADR link or waiver] |
| Security review required | [Yes/No/N/A] | [review link or waiver] |
| Performance budget defined | [Yes/No/N/A] | [budget or rationale] |
| Agent/tool approval boundary defined | [Yes/No/N/A] | [plan section] |

## Implementation Gates

| Gate | Required? | Evidence |
|------|-----------|----------|
| Tests added or waiver documented | Yes | [test paths or waiver] |
| Lint/format/static checks run | [Yes/No/N/A] | [command output summary] |
| Build/typecheck run | [Yes/No/N/A] | [command output summary] |
| Security/dependency checks run | [Yes/No/N/A] | [command output summary] |
| Documentation updated | [Yes/No/N/A] | [paths] |
| Release checklist completed | [Yes/No/N/A] | [link] |

## Residual Risk

- **Risk**: [description]
- **Mitigation**: [what reduces likelihood or impact]
- **Owner**: [name or role]
- **Revisit condition**: [date, milestone, or signal]

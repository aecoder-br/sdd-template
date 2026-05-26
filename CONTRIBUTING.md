# Contributing

Thanks for helping improve this Codex-ready Spec Driven Design template.

## Contribution Flow

1. Start with the current constitution in `.specify/memory/constitution.md`.
2. Create or update a specification with `speckit-specify`.
3. Clarify ambiguous requirements with `speckit-clarify`.
4. Generate or update the implementation plan with `speckit-plan`.
5. Analyze the spec, plan, and tasks with `speckit-analyze`.
6. Generate tasks with `speckit-tasks`.
7. Implement with `speckit-implement` or make a focused manual change.
8. Run the validation described in the plan and record the result.

For documentation-only changes, keep the diff focused and run at least
`git diff --check`.

## Standards

- Keep README and workflow guidance aligned with local `.specify` metadata.
- Preserve Codex skills mode unless an integration change is intentional.
- Do not rewrite upstream Spec Kit content verbatim; adapt it to this template.
- Keep generated feature artifacts under `specs/<feature>/`.
- Keep reusable template changes under `.specify/templates/`.
- Keep Codex skill changes under `.agents/skills/`.

## Pull Requests

Pull requests should explain:

- What changed
- Which Spec Kit or Codex behavior is affected
- Which validation was run
- Any known follow-up work

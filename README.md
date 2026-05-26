# SDD Template for Codex

This repository is a reusable Spec Driven Design template for Codex, based on
[github/spec-kit](https://github.com/github/spec-kit).

It is already initialized for Codex skills mode. The project-principles step has
already been completed, and `.specify/memory/constitution.md` contains the
governing principles for code quality, testing, user experience consistency,
performance, and technical decision governance.

## What Is Included

- Spec Kit project structure under `.specify/`
- Codex skills under `.agents/skills/`
- PowerShell Spec Kit helper scripts
- Git workflow extension for feature branches and optional commits
- Project constitution ratified in `.specify/memory/constitution.md`
- Root guidance in `AGENTS.md`

Local metadata currently records Spec Kit `0.8.13`, Codex as the default
integration, skills mode enabled, PowerShell scripts, and sequential branch
numbering.

## Start Here

Do not rerun Step 1 unless you intentionally want to revise the constitution.
This template has already completed:

```text
STEP 1: Establish project principles
```

Users of this template should continue from Step 2 of the Spec Kit detailed
process: create the project specification for the application or feature they
want to build.

## Detailed Process for Codex

The upstream process is documented in the
[Spec Kit Detailed Process](https://github.com/github/spec-kit#-detailed-process).
Use the Codex-focused flow below from Step 2 onward.

### Step 2: Create Project Specifications

Use the `speckit-specify` skill, or the slash-style request
`/speckit.specify`, to describe the product behavior you want. Focus on what
the system should do and why users need it. Avoid choosing the tech stack in
this step unless it is a hard product constraint.

Example:

```text
/speckit.specify Build a task management application for small teams. Users can
create projects, assign tasks, comment on tasks, and move tasks across a Kanban
board. Start with predefined users and no authentication for the first version.
```

Expected output:

- A feature branch such as `001-task-management`
- A new `specs/<feature>/spec.md`
- User stories, functional requirements, assumptions, success criteria, and
  constitution-aligned requirements

### Step 3: Clarify the Specification

Use `speckit-clarify`, or `/speckit.clarify`, before planning. Codex should
identify underspecified requirements, ask targeted questions, and record the
answers in the spec.

Skip this only for an intentional spike or prototype, and state that explicitly
so the tradeoff is visible in the artifacts.

### Step 4: Generate the Implementation Plan

Use `speckit-plan`, or `/speckit.plan`, once the specification is stable. This
is where you provide implementation constraints such as the language, framework,
data storage, target platform, architecture preferences, and validation
expectations.

Expected output in `specs/<feature>/`:

- `plan.md`
- `research.md`
- `data-model.md` when applicable
- `contracts/` when applicable
- `quickstart.md`

### Step 5: Validate the Plan and Artifacts

Use `speckit-analyze`, or `/speckit.analyze`, to check consistency across the
specification, plan, and generated artifacts. Codex should look for missing
requirements, contradictions, over-engineering, unclear test strategy, UX gaps,
and performance risks before tasks are generated.

The plan must keep the constitution as the decision filter.

### Step 6: Generate the Task Breakdown

Use `speckit-tasks`, or `/speckit.tasks`, after the plan is accepted. This
creates `tasks.md` in the feature directory with ordered, actionable work.

The generated task list should include:

- Story-by-story implementation phases
- Dependency ordering
- Parallel markers where safe
- File paths for implementation work
- Required validation and testing tasks
- Checkpoints for independently testable user stories

### Step 7: Implement

Use `speckit-implement`, or `/speckit.implement`, when the specification, plan,
and tasks are ready. Codex should execute tasks in order, respect dependencies,
run the validation requested in the plan, and report unresolved risks.

Codex may need local tools such as package managers, language runtimes, test
runners, or browsers depending on the feature plan. Install those in the target
project environment before implementation begins.

## Common Commands

| Purpose | Codex skill | Slash-style request |
| --- | --- | --- |
| Create or update principles | `speckit-constitution` | `/speckit.constitution` |
| Create feature specification | `speckit-specify` | `/speckit.specify` |
| Clarify specification | `speckit-clarify` | `/speckit.clarify` |
| Create implementation plan | `speckit-plan` | `/speckit.plan` |
| Analyze artifacts | `speckit-analyze` | `/speckit.analyze` |
| Generate tasks | `speckit-tasks` | `/speckit.tasks` |
| Implement tasks | `speckit-implement` | `/speckit.implement` |
| Create checklist | `speckit-checklist` | `/speckit.checklist` |

Codex skills are stored in `.agents/skills/`. If a surface does not support
slash-style commands, ask Codex to use the named skill directly.

## Working With This Template

1. Clone or copy this repository.
2. Open it with Codex.
3. Read `AGENTS.md` and `.specify/memory/constitution.md`.
4. Start a feature with Step 2: `speckit-specify`.
5. Follow the generated artifacts through clarification, planning, analysis,
   tasks, and implementation.

Keep generated feature work under `specs/<feature>/`. Keep reusable Spec Kit
template changes under `.specify/templates/`, and keep Codex workflow changes
under `.agents/skills/`.

## Updating From Upstream Spec Kit

This template is based on Spec Kit but can intentionally diverge for Codex. When
updating from upstream:

- Review upstream release notes before replacing local files.
- Preserve Codex skills mode unless you intentionally change integrations.
- Re-check `.specify/integration.json` and `.specify/init-options.json`.
- Re-run the Spec Kit workflow on a small sample feature before adopting the
  update broadly.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).

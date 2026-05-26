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

For this Codex skills installation, use the skill names directly, such as
`speckit-specify`, or ask Codex to use `$speckit-specify` when the UI supports
skill chips. Slash-style prompts such as `/speckit.specify` may work in some
surfaces, but the installed integration is Codex skills mode.

## Detailed Process for Codex

The upstream process is documented in the
[Spec Kit Detailed Process](https://github.com/github/spec-kit#-detailed-process).
Use the Codex-focused flow below from Step 2 onward. For non-trivial work, keep
the clarify, checklist, analyze, and validation gates in the path instead of
jumping straight from a spec to implementation.

### Step 2: Create Project Specifications

Use `speckit-specify` to describe the product behavior you want. Focus on what
the system should do and why users need it. Avoid choosing the tech stack in
this step unless it is a hard product constraint.

Example:

```text
Use $speckit-specify to build a task management application for small teams. Users can
create projects, assign tasks, comment on tasks, and move tasks across a Kanban
board. Start with predefined users and no authentication for the first version.
```

Expected output:

- A feature branch such as `001-task-management`
- A new `specs/<feature>/spec.md`
- User stories, functional requirements, assumptions, success criteria, and
  constitution-aligned requirements

### Step 3: Clarify the Specification

Use `speckit-clarify` before planning. Codex should identify underspecified
requirements, ask targeted questions, and record the answers in the spec.

Skip this only for an intentional spike or prototype, and state that explicitly
so the tradeoff is visible in the artifacts.

### Step 4: Create a Feature Checklist

Use `speckit-checklist` when the feature needs an explicit quality checklist
before planning. The checklist should cover requirement quality, security,
testing, UX, performance, and traceability.

### Step 5: Generate the Implementation Plan

Use `speckit-plan` once the specification is stable. This is where you provide
implementation constraints such as the language, framework, data storage, target
platform, architecture preferences, agent strategy, and validation expectations.

Expected output in `specs/<feature>/`:

- `plan.md`
- `research.md`
- `data-model.md` when applicable
- `contracts/` when applicable
- `quickstart.md`

### Step 6: Generate the Task Breakdown

Use `speckit-tasks` after the plan is accepted. This creates `tasks.md` in the
feature directory with ordered, actionable work.

The generated task list should include:

- Story-by-story implementation phases
- Dependency ordering
- Parallel markers where safe
- File paths for implementation work
- Required validation and testing tasks
- Checkpoints for independently testable user stories

### Step 7: Analyze the Artifacts

Use `speckit-analyze` before implementation to check consistency across the
specification, plan, and tasks. Codex should look for missing requirements,
contradictions, over-engineering, unclear test strategy, UX gaps, security gaps,
and performance risks.

The plan must keep the constitution as the decision filter.

### Step 8: Implement

Use `speckit-implement` when the specification, plan, tasks, and analysis are
ready. Codex should execute tasks in order, respect dependencies, run the
validation requested in the plan, and report unresolved risks.

Codex may need local tools such as package managers, language runtimes, test
runners, or browsers depending on the feature plan. Install those in the target
project environment before implementation begins.

## Common Commands

| Purpose | Codex skill |
| --- | --- |
| Create or update principles | `speckit-constitution` |
| Create feature specification | `speckit-specify` |
| Clarify specification | `speckit-clarify` |
| Create checklist | `speckit-checklist` |
| Create implementation plan | `speckit-plan` |
| Generate tasks | `speckit-tasks` |
| Analyze artifacts | `speckit-analyze` |
| Implement tasks | `speckit-implement` |

Codex skills are stored in `.agents/skills/`. Ask Codex to use the named skill
directly, or use `$skill-name` when the UI exposes skill chips.

## Working With This Template

1. Clone or copy this repository.
2. Open it with Codex.
3. Read `AGENTS.md` and `.specify/memory/constitution.md`.
4. Start a feature with Step 2: `speckit-specify`.
5. Follow the generated artifacts through clarification, checklist, planning,
   tasks, analysis, and implementation.

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

## Professional Baseline

This repository is intentionally opinionated about governance and intentionally
lightweight about tooling. It includes reusable guidance for:

- agent operating rules and human approval boundaries;
- security and agent-tooling threat modeling;
- Definition of Done and quality gates;
- architecture decision records and architecture overview;
- observability, performance, release, and runbook templates;
- GitHub issue and pull request templates.

It does not enable active CI, scanners, releases, Dependabot, SBOM generation,
or community Spec Kit extensions by default. Add those only when the target
project has a concrete stack, package ecosystem, release process, and owner.

## Optional Maturity Layers

Evaluate these only after the project has real requirements and owners:

- Spec Kit presets or extensions for agent parity, security governance,
  architecture governance, explicit task dependencies, table of contents,
  CI guard, QA testing, review, or verification.
- Dependency automation such as Dependabot or Renovate.
- Active GitHub Actions for lint, test, build, security scanning, artifact
  publishing, provenance, or release.
- OpenSSF Scorecard, SLSA provenance, SBOM publication, and formal threat
  modeling.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).

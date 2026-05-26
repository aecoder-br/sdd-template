# Implementation Plan: [FEATURE]

**Branch**: `[###-feature-name]` | **Date**: [DATE] | **Spec**: [link]

**Input**: Feature specification from `/specs/[###-feature-name]/spec.md`

**Note**: This template is filled in by the `/speckit-plan` command. See `.specify/templates/plan-template.md` for the execution workflow.

## Summary

[Extract from feature spec: primary requirement + technical approach from research]

## Technical Context

<!--
  ACTION REQUIRED: Replace the content in this section with the technical details
  for the project. The structure here is presented in advisory capacity to guide
  the iteration process.
-->

**Language/Version**: [e.g., Python 3.11, Swift 5.9, Rust 1.75 or NEEDS CLARIFICATION]

**Primary Dependencies**: [e.g., FastAPI, UIKit, LLVM or NEEDS CLARIFICATION]

**Storage**: [if applicable, e.g., PostgreSQL, CoreData, files or N/A]

**Testing**: [e.g., pytest, XCTest, cargo test or NEEDS CLARIFICATION]

**Target Platform**: [e.g., Linux server, iOS 15+, WASM or NEEDS CLARIFICATION]

**Project Type**: [e.g., library/cli/web-service/mobile-app/compiler/desktop-app or NEEDS CLARIFICATION]

**Performance Goals**: [domain-specific, e.g., 1000 req/s, 10k lines/sec, 60 fps or NEEDS CLARIFICATION]

**Constraints**: [domain-specific, e.g., <200ms p95, <100MB memory, offline-capable or NEEDS CLARIFICATION]

**Scale/Scope**: [domain-specific, e.g., 10k users, 1M LOC, 50 screens or NEEDS CLARIFICATION]

## Constitution Check

*GATE: Must pass before Phase 0 research. Re-check after Phase 1 design.*

- **Code Quality**: Does the plan preserve existing architecture, ownership,
  naming, error handling, and formatting patterns? Document any justified
  deviation and the simpler alternative that was rejected.
- **Testing Standards**: What automated tests will cover new logic, changed
  contracts, regressions, and critical journeys? If automation is deferred,
  document the manual verification path and residual risk.
- **UX Consistency**: For user-facing work, which adjacent workflows,
  components, terminology, accessibility states, and responsive behaviors are
  being reused or preserved?
- **Performance Requirements**: What latency, throughput, memory, startup,
  rendering, bundle, or resource budget applies? Define the measurement method
  or explain why performance is not a risk for this feature.
- **Decision Traceability**: Are material technical decisions recorded with
  constraints, options considered, consequences, and validation expectations?
- **Security & Privacy**: What data, auth/authz, abuse, validation, secret
  handling, dependency, or compliance risks must be addressed?
- **Minimal Architecture**: What is the simplest architecture that satisfies the
  spec, and what abstractions are intentionally avoided?
- **Observability & Operations**: What logs, metrics, traces, alerts, runbooks,
  or support paths are required for this feature's risk level?
- **Supply Chain**: What new dependencies, generated artifacts, lockfiles,
  provenance, or update automation are introduced?
- **Agent Strategy**: What work is safe for subagents or skills, and what
  actions require explicit human approval?

## Project Structure

### Documentation (this feature)

```text
specs/[###-feature]/
├── plan.md              # This file (/speckit-plan command output)
├── research.md          # Phase 0 output (/speckit-plan command)
├── data-model.md        # Phase 1 output (/speckit-plan command)
├── quickstart.md        # Phase 1 output (/speckit-plan command)
├── contracts/           # Phase 1 output (/speckit-plan command)
└── tasks.md             # Phase 2 output (/speckit-tasks command - NOT created by /speckit-plan)
```

### Source Code (repository root)
<!--
  ACTION REQUIRED: Replace the placeholder tree below with the concrete layout
  for this feature. Delete unused options and expand the chosen structure with
  real paths (e.g., apps/admin, packages/something). The delivered plan must
  not include Option labels.
-->

```text
# [REMOVE IF UNUSED] Option 1: Single project (DEFAULT)
src/
├── models/
├── services/
├── cli/
└── lib/

tests/
├── contract/
├── integration/
└── unit/

# [REMOVE IF UNUSED] Option 2: Web application (when "frontend" + "backend" detected)
backend/
├── src/
│   ├── models/
│   ├── services/
│   └── api/
└── tests/

frontend/
├── src/
│   ├── components/
│   ├── pages/
│   └── services/
└── tests/

# [REMOVE IF UNUSED] Option 3: Mobile + API (when "iOS/Android" detected)
api/
└── [same as backend above]

ios/ or android/
└── [platform-specific structure: feature modules, UI flows, platform tests]
```

**Structure Decision**: [Document the selected structure and reference the real
directories captured above]

## Complexity Tracking

> **Fill ONLY if Constitution Check has violations that must be justified**

| Violation | Why Needed | Simpler Alternative Rejected Because |
|-----------|------------|-------------------------------------|
| [e.g., 4th project] | [current need] | [why 3 projects insufficient] |
| [e.g., Repository pattern] | [specific problem] | [why direct DB access insufficient] |

## Supporting Artifacts

> **Create only when they reduce risk or preserve important decisions.**

- **ADR Required?** [Yes/No - required for material architecture, contract,
  data, security, performance, runtime, dependency, or cross-feature UX
  decisions]
- **Security Review Required?** [Yes/No - required when sensitive data, auth,
  external integrations, secrets, generated code, or elevated tools are touched]
- **Runbook Required?** [Yes/No - required for deployed services, scheduled jobs,
  incident-prone workflows, or operational handoffs]
- **Release Checklist Required?** [Yes/No - required for published packages,
  deployable services, public APIs, migrations, or customer-visible releases]

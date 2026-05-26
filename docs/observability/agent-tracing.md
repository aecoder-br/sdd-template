# Agent Tracing

Agent work should leave enough evidence for a reviewer to understand what was
planned, changed, validated, skipped, and approved.

## Minimum Trace Fields

- **Task**: user request and scope
- **Artifacts**: spec, plan, tasks, docs, files changed
- **Agent roles**: primary agent and subagents used
- **Tool calls**: command or connector, target, and result summary
- **Approvals**: action approved, approver, and reason
- **Diff**: paths changed and intent
- **Validation**: commands run, pass/fail, skipped checks, residual risk
- **External context**: sources, retrieval date, and confidence

## Redaction

Do not record:

- secrets or credentials;
- personal data not required for review;
- full logs when a summary is enough;
- private connector payloads unless approved.

## Correlation

When possible, correlate traces with:

- feature branch;
- pull request or issue;
- Spec Kit feature directory;
- commit hashes;
- CI runs or release IDs.

## Retention

For small projects, final responses, commits, and PR descriptions may be enough.
For regulated or production systems, define explicit retention and audit
requirements before implementation.

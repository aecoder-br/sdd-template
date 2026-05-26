# Agent Human Approval Playbook

Use this playbook to decide when an agent can proceed autonomously and when a
human must approve the exact action.

## Approval Matrix

| Action | Default | Notes |
|--------|---------|-------|
| Read files in workspace | Allowed | Respect sensitive files and user scope |
| Search docs or source | Allowed | Prefer repo truth before web search |
| Edit requested files | Allowed after implementation request | Keep scope tight |
| Run tests/builds/checks | Allowed | Avoid commands that rewrite tracked files unless requested |
| Stage or commit | Approval or explicit user request | Stage explicit paths |
| Push, deploy, publish, release | Requires approval | Name target and expected outcome |
| Delete, reset, checkout, clean | Requires approval | Never infer destructive intent |
| Install packages or extensions | Requires approval | Explain source and scope |
| Mutate GitHub/cloud/MCP target | Requires approval | Include target, payload, and rollback path |
| Handle secrets | Requires approval | Never print secrets |

## Approval Request Standard

Before asking for approval, provide:

- exact command or tool action;
- target path, repository, service, or API;
- reason the action is needed;
- risk and expected result;
- rollback or recovery path when relevant.

## Prohibited Without Explicit User Direction

- `git reset --hard`, broad checkout, or recursive deletion;
- push/deploy/release/publish;
- credential rotation or permission grants;
- writing outside the workspace;
- enabling auto-approval for broad tools or connectors.

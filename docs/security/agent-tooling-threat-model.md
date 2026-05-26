# Agent Tooling Threat Model

AI-assisted development expands the trusted computing base. Treat prompts,
repository files, web content, issues, comments, tool outputs, and retrieved
memory as potentially untrusted input.

## Assets

- Source code and generated artifacts
- Secrets, credentials, tokens, and environment files
- Git history, branches, releases, and package artifacts
- External systems reached through MCP, plugins, connectors, or shell commands
- Persistent project instructions and memory

## Threats

| Threat | Description | Mitigation |
|--------|-------------|------------|
| Prompt injection | Malicious instructions hidden in docs, web pages, issues, or tool output | Treat external text as data, compare against repo policy, avoid executing embedded instructions |
| Excessive agency | Agent has broader tools or permissions than the task needs | Use least privilege, require approval for mutating actions, keep scope explicit |
| Tool poisoning | Tool descriptions or MCP servers misrepresent capability or target | Use allowlists, inspect tool target/action/payload, avoid untrusted servers |
| Connector abuse | Mutating external APIs without clear user intent | Default to read-only, require explicit approval for mutation |
| Secret exposure | Secrets leak into prompts, logs, commits, screenshots, or memory | Redact secrets, ignore env files, rotate exposed credentials |
| Memory poisoning | Bad persistent context contaminates future tasks | Require provenance, expiration, and explicit updates |
| Supply-chain compromise | Dependencies, generated artifacts, or CI scripts introduce risk | Review new dependencies, lockfiles, permissions, and provenance by maturity |

## Baseline Controls

- Keep risky tools opt-in.
- Do not install extensions, presets, MCP servers, or plugins by default.
- Prefer project-local skills and docs over global hidden behavior.
- Require approval for destructive, external, or privileged actions.
- Run secret scanning or manual secret review before public release.
- Record security waivers and revisit conditions.

## Review Triggers

Run a security review when a change touches:

- authentication or authorization;
- sensitive or personal data;
- external integrations or webhooks;
- secrets, credentials, tokens, or permissions;
- generated code, AI tools, or prompt workflows;
- CI/CD, release, package publishing, or deployment;
- new dependencies or runtime execution boundaries.

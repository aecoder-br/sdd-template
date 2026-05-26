---
name: sdd-security-review
description: Security review for Spec Kit specs, plans, tasks, diffs, AI tooling, MCP/connectors, secrets, dependencies, and release workflows. Use when Codex must find security, privacy, supply-chain, or agent-tooling risks before implementation or merge.
---

# SDD Security Review

Use this skill as a review stance. Prioritize findings over summaries. Do not
rewrite the implementation unless the user asks for fixes.

## Review Inputs

Read the available artifacts:

- `.specify/memory/constitution.md`
- active `spec.md`, `plan.md`, and `tasks.md`
- relevant diffs or changed files
- security review template, if present

## Risk Areas

Check for:

- sensitive data, secrets, logging, and retention;
- authentication, authorization, and abuse cases;
- input validation and error disclosure;
- dependencies, package scripts, CI/CD permissions, and release paths;
- MCP, plugin, connector, or cloud mutations;
- prompt injection, excessive agency, tool poisoning, and memory poisoning.

## Output

Return findings ordered by severity with:

- file or artifact reference;
- risk and impact;
- concrete mitigation;
- residual risk or waiver needed.

If no issues are found, say that clearly and list remaining validation gaps.

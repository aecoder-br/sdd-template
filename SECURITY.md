# Security Policy

## Supported Versions

This repository is a template. Security fixes should target the default branch
unless a maintainer documents another supported release line.

## Reporting a Vulnerability

Do not open a public issue for a vulnerability that could expose users, secrets,
or systems. Use the repository's private security reporting channel when
available, or contact the maintainers privately.

When reporting, include:

- Affected files or workflow
- Impact and exploitability
- Reproduction steps
- Suggested mitigation, if known

## Secret Handling

Never commit secrets, tokens, private keys, credentials, production data, or
personal data. Use local environment files or secret stores, and keep those
files ignored by Git.

If a secret is committed, rotate it immediately and remove it from history using
the repository owner's approved process.

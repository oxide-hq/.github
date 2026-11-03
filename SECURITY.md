# Security Policy

## Supported versions

Oxide is pre-1.0. Security fixes land on `main` and in the latest published release only.

| Version          | Supported |
| ---------------- | --------- |
| latest `0.x`     | ✅        |
| older releases   | ❌        |

## Reporting a vulnerability

**Please do not report security vulnerabilities in public issues, discussions or pull requests.**

Report privately through GitHub's private vulnerability reporting on the affected repository —
for the framework: **[open a security advisory](https://github.com/oxide-hq/oxide-framework/security/advisories/new)**.

Include what you can of:

- the affected crate(s) and version or commit,
- a description of the issue and its impact,
- steps or a minimal proof of concept to reproduce it.

## What to expect

- We aim to acknowledge reports within **3 business days**.
- We will keep you informed while we investigate and work on a fix.
- Once a fix is released we publish a GitHub security advisory and, where applicable, a
  [RustSec](https://rustsec.org) advisory. We credit reporters unless you ask us not to.

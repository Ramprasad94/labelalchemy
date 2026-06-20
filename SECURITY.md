# Security Policy

Thank you for helping keep Label Alchemy and its users safe.

## Reporting a vulnerability

**Please report security vulnerabilities privately — do not open a public GitHub issue, discussion, or pull request for a security problem.**

Two private channels are available:

1. **Email:** **support@labelalchemy.dev** with the subject line `SECURITY: <short summary>`.
2. **GitHub private advisory:** use [**Report a vulnerability**](../../security/advisories/new) (Security tab → Advisories), which keeps the report confidential.

Please include:

- A description of the issue and its potential impact.
- Steps to reproduce, or a proof of concept.
- The affected Label Alchemy version and your environment (VS Code version, OS).
- Any suggested remediation, if you have one.

## What to expect

Label Alchemy is maintained by a solo developer, so responses are best-effort rather than bound by a formal SLA:

- **Acknowledgement:** typically within a few business days.
- **Assessment & fix:** I will work with you to confirm the issue, determine severity, and ship a fix as quickly as is practical.
- **Disclosure:** please give a reasonable window to release a fix before any public disclosure. Credit will gladly be given to reporters who want it.

## Scope

This policy covers the **Label Alchemy VS Code extension**. The extension's source is maintained privately; reports here are routed to the maintainer.

Out of scope: vulnerabilities in third-party services you connect Label Alchemy to (your chosen LLM provider, Lemon Squeezy, etc.) — report those to the respective vendor. Issues in **your own** API keys, license keys, or org credentials are not vulnerabilities in Label Alchemy; rotate the affected credential.

## Please never include secrets

Even in a private report, redact real API keys, license keys, and org credentials. A synthetic example is enough to demonstrate most issues.

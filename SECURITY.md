# Security Policy

## Scope

The **Executive Support System** is currently in a documentation-only phase. There is no application code, no running service, and no user data processed by this repository.

This policy will evolve as the project moves into implementation phases.

---

## Reporting a Vulnerability

If you discover a security vulnerability in this project—including in any configuration files, automation scripts, or templates—please report it responsibly.

**Do not open a public GitHub issue for security vulnerabilities.**

Instead, report security issues via [GitHub's private vulnerability reporting](https://docs.github.com/en/code-security/security-advisories/guidance-on-reporting-and-writing/privately-reporting-a-security-vulnerability) for this repository, or contact the maintainer directly through their GitHub profile.

Please include:

- A description of the vulnerability
- Steps to reproduce or demonstrate the issue
- The potential impact
- Any suggested mitigations (optional)

The maintainer will acknowledge valid reports as promptly as practical for a single-maintainer project. If the
report is valid, a fix will be prioritised and a disclosure timeline agreed with the reporter where appropriate.

---

## Data Handling

This system is designed to handle personal and work-related information. The following principles apply:

- The system owner controls their own data. No central server receives user data by default.
- Automation adapters (n8n, Zapier, Make, etc.) are configured and operated by the user. Each adapter's data handling is governed by that provider's own terms.
- AI integrations are optional. When used, data shared with AI services is governed by the relevant provider's privacy policy.
- Notion is used as the primary interface. Notion's data handling is governed by Notion's terms of service.

**This project does not operate any data collection infrastructure.** Users are responsible for the security of their own Notion workspace, automation accounts, and connected services.

---

## Sensitive Information in Contributions

Do not include in any contribution:

- Real personal data (names, contact details, identifiers)
- Credentials, API keys, tokens, or secrets of any kind
- Confidential business information
- Information from specific employers (use "Personal" and "Work" as profile labels)

Pull requests containing sensitive information will be rejected and the contributor asked to re-submit without it.

---

## Supported Versions

As the project has no versioned releases yet, all security reports should target the current state of the `main` branch.

---

*This policy will be updated as the project moves from documentation into implementation.*

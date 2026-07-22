# Security Policy

## Scope

The project is currently documentation-first. This policy will expand as templates, connectors, automation, and services are implemented.

## Reporting a vulnerability

Do not open a public issue for a vulnerability, exposed credential, or sensitive-data leak.

Use GitHub private vulnerability reporting when available, or contact the maintainer through the GitHub profile. Include:

- a description;
- affected file, workflow, or release;
- steps to reproduce where applicable;
- potential impact;
- suggested mitigation if known.

The single maintainer will acknowledge and prioritize reports as availability permits. Public disclosure timing will be coordinated for valid issues where practical.

## Data handling principles

- The user controls their own workspace and connected services.
- The manual community system does not require a central project-operated server.
- Automation and AI are optional.
- Connected providers process data under their own terms.
- A future hosted service will document its own data flow, retention, and security controls before launch.
- Personal and Work profiles are public product concepts; employer-specific data belongs only in private user configuration.

## Contributions

Do not commit:

- credentials, tokens, or secrets;
- real personal data;
- confidential employer or customer information;
- private recordings or transcripts;
- proprietary third-party material without permission.

Use synthetic examples and the default Personal and Work profiles.

## Supported versions

Until versioned releases exist, reports should reference the current `main` branch or the specific commit involved.
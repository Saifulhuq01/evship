# Security Policy

## Reporting a Vulnerability

**DO NOT open a public GitHub issue for security vulnerabilities.**

Email: security@evship.dev

Include:
- Description of the vulnerability
- Steps to reproduce
- Potential impact assessment

We respond within 48 hours. Critical vulnerabilities patched within 7 days.

## Supported Versions

| Version | Supported |
|---|---|
| 1.x (latest) | ✅ Active |
| 0.x | ⚠️ Best effort |

## Security Design Principles

- API keys hashed with SHA-256, constant-time comparison only
- Webhook signatures computed at dispatch time, never ingestion
- Signing secrets encrypted via AWS KMS at rest
- Row Level Security enforces tenant isolation at DB layer
- SSRF protection via egress proxy
- All HTTP response bodies capped at 4KB

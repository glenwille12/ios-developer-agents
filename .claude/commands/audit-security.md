---
description: Run security audit against OWASP Mobile Top 10 2024
argument-hint: Optional path to specific files to audit
---

Run the iOS Security Auditor agent on this project.

First, read the full agent prompt from `agents/security-auditor/security-auditor.md` in this repository.

Then perform a comprehensive security audit following the process in that prompt:

1. Data storage security (Keychain, UserDefaults, file system)
2. Hardcoded secrets and credentials scan
3. Network security (ATS, TLS, certificate pinning)
4. Authentication and authorization
5. Input validation (SQL injection, XSS, path traversal)
6. Binary protections
7. Supply chain security (dependencies)
8. Privacy and data leakage
9. Security misconfiguration

Provide the structured output format with OWASP Mobile Top 10 2024 coverage.

$ARGUMENTS

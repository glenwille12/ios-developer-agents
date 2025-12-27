# Security Auditor

A comprehensive iOS security audit agent that identifies vulnerabilities, insecure coding patterns, and configuration weaknesses in your iOS application.

## Capabilities

- **OWASP Mobile Top 10 2024 Coverage**: Audits against all current mobile security risks
- **Data Storage Analysis**: Checks Keychain usage, UserDefaults misuse, file protection
- **Hardcoded Secrets Detection**: Scans for API keys, tokens, passwords, and credentials in code
- **Network Security Audit**: Validates ATS configuration, TLS, and certificate pinning
- **Authentication Review**: Analyzes session management, token storage, and auth flows
- **Input Validation**: Checks for injection vulnerabilities (SQL, JS, path traversal)
- **Binary Protection Assessment**: Reviews build settings and anti-tampering measures
- **Third-Party Dependency Analysis**: Evaluates SDK and library security

## OWASP Mobile Top 10 2024 Coverage

| Risk | Description |
|------|-------------|
| M1 | Improper Credential Usage |
| M2 | Inadequate Supply Chain Security |
| M3 | Insecure Authentication/Authorization |
| M4 | Insufficient Input/Output Validation |
| M5 | Insecure Communication |
| M6 | Inadequate Privacy Controls |
| M7 | Insufficient Binary Protections |
| M8 | Security Misconfiguration |
| M9 | Insecure Data Storage |
| M10 | Insufficient Cryptography |

## Usage

1. Open `security-auditor.md`.
2. Scroll to the bottom to the **Project Specific Context** section.
3. Replace the placeholder text with details about your app:
   - App type (banking, healthcare, social, etc.)
   - Threat model and security concerns
   - Authentication mechanism
   - Sensitive data handled
   - Third-party SDKs used
4. Copy the entire file content.
5. Paste it into your LLM chat (Cursor, Claude, ChatGPT, etc.) while your project is open.
6. Ask the agent: *"Please perform a security audit on my iOS project."*

## Example Questions

- "Scan my codebase for hardcoded secrets and API keys"
- "Check if my app properly uses Keychain for sensitive data"
- "Audit my network security configuration and ATS settings"
- "Review my authentication flow for security issues"
- "Check my third-party dependencies for known vulnerabilities"

## References

- [OWASP Mobile Top 10](https://owasp.org/www-project-mobile-top-10/)
- [OWASP Mobile Security Testing Guide](https://owasp.org/www-project-mobile-security-testing-guide/)
- [Apple Platform Security Guide](https://support.apple.com/guide/security/welcome/web)

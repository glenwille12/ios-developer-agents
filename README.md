# iOS Developer Agents

A collection of AI agents and skills designed to supercharge your iOS development workflow. These agents are optimized for use with LLM-based coding tools (like Cursor, Windsurf, or generic LLM chats).

## Available Agents

| Agent | Description | Model |
|-------|-------------|-------|
| [App Store Validator](agents/app-store-validator) | Pre-validate your iOS app against Apple's Review Guidelines to catch rejection issues early. | Claude 4.5 Opus / Sonnet |
| [Security Auditor](agents/security-auditor) | Comprehensive security audit against OWASP Mobile Top 10 2024, detecting vulnerabilities, hardcoded secrets, and insecure configurations. | Claude 4.5 Opus / Sonnet |
| [Accessibility Validator](agents/accessibility-validator) | Audit your app for accessibility compliance with Apple HIG, WCAG 2.2, VoiceOver, Dynamic Type, and inclusive design standards. | Claude 4.5 Opus / Sonnet |

## How to Use

1. **Select an Agent**: Navigate to the agent's directory (e.g., `agents/app-store-validator`).
2. **Copy the Prompt**: Open the `.md` file corresponding to the agent (e.g., `app-store-validator.md`).
3. **Inject Context**: Paste the prompt into your LLM chat. *Crucial*: Most agents have a "Project Specific Context" section at the bottom. Make sure to fill this in with details about your specific app to get the best results.
4. **Run**: Let the agent analyze your codebase or answer your questions.

## Contribution

Contributions are welcome! If you have a prompt or agent workflow that saves you time, feel free to open a PR.

# iOS Developer Agents

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Contributions Welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg)](CONTRIBUTING.md)

AI agents to validate, audit, and improve your iOS apps before release.

## What's Included

| Agent | Purpose |
|-------|---------|
| **App Store Validator** | Pre-validate against Apple's Review Guidelines to catch rejections early |
| **Security Auditor** | Audit against OWASP Mobile Top 10 2024 and iOS security best practices |
| **Accessibility Validator** | Check compliance with Apple HIG, WCAG 2.2, VoiceOver, and Dynamic Type |

## Quick Start

### Claude Code

```bash
# Copy to your iOS project
cp -r .claude/ /path/to/your/ios-project/

# Run commands
/validate-appstore
/audit-security
/audit-accessibility
```

[Full Claude Code guide](docs/integrations/claude-code.md)

### Cursor

```bash
# Copy to your iOS project
cp -r .cursor/ /path/to/your/ios-project/

# Rules auto-activate when editing Swift, Info.plist, etc.
```

[Full Cursor guide](docs/integrations/cursor.md)

### Claude.ai Projects

1. Create a new Project at [claude.ai](https://claude.ai)
2. Copy instructions from `claude-projects/[agent]-instructions.md`
3. Paste into Project Instructions
4. Upload your iOS files

[Full Claude Projects guide](docs/integrations/claude-projects.md)

### Direct Chat

Copy the full agent prompt from `agents/[name]/[name].md` and paste into any LLM chat.

## Getting Started Guides

- [Solo Developers](docs/getting-started/solo-developer.md) - Quick 5-minute setup
- [iOS Teams](docs/getting-started/team-setup.md) - Shared workflows and PR integration
- [Contributors](docs/getting-started/contributor-guide.md) - Create new agents

## Project Structure

```
ios-developer-agents/
  agents/                    # Full agent prompts (source of truth)
  .claude/                   # Claude Code commands & skills
  .cursor/                   # Cursor rules (.mdc format)
  claude-projects/           # Claude.ai Project templates
  ai-rules/                  # Generic AI tool rules
  docs/                      # Documentation
```

## Integration Options

| Tool | Files | Activation |
|------|-------|-----------|
| Claude Code | `.claude/commands/`, `.claude/skills/` | Slash commands & auto |
| Cursor | `.cursor/rules/*.mdc` | Auto on matching files |
| Claude.ai | `claude-projects/*.md` | Manual setup |
| Other AI tools | `ai-rules/*.txt` | Copy-paste |

## Contributing

Contributions welcome! See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

Ideas for new agents:
- Performance Auditor
- Localization Validator
- SwiftUI Best Practices
- Testing Coverage Analyzer

## License

MIT License - see [LICENSE](LICENSE)

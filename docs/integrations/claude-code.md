# Claude Code Integration

Use iOS Developer Agents with [Claude Code](https://claude.ai/code) CLI.

## Setup

Copy the `.claude/` folder to your iOS project:

```bash
cp -r .claude/ /path/to/your/ios-project/
```

## Available Commands

### /validate-appstore

Validate your iOS app against Apple's App Store Review Guidelines.

```
/validate-appstore
```

Optionally specify files:
```
/validate-appstore Info.plist PrivacyInfo.xcprivacy
```

### /audit-security

Run a security audit against OWASP Mobile Top 10 2024.

```
/audit-security
```

### /audit-accessibility

Audit your app for accessibility compliance.

```
/audit-accessibility
```

## How It Works

### Commands (`.claude/commands/`)

Slash commands you invoke directly. They reference the full agent prompts from `agents/`.

### Skills (`.claude/skills/`)

Claude automatically invokes these when relevant. For example, when you're editing Info.plist, Claude may proactively apply App Store validation knowledge.

## Customization

### Add Project Context

Edit the skills to include your project-specific context:

```markdown
## Project Specific Context

- App Type: [Your app description]
- Authentication: [Your auth method]
- Sensitive Data: [What you handle]
- Third-Party SDKs: [Your SDKs]
```

### Create Custom Commands

Add new commands in `.claude/commands/`:

```markdown
---
description: Your custom validation
argument-hint: Optional arguments
---

Your instructions here.

$ARGUMENTS
```

## CLAUDE.md

The `CLAUDE.md` file in the repo root provides project context to Claude Code when working within the ios-developer-agents repository itself.

For your iOS project, consider creating your own `CLAUDE.md` with project-specific information.

# Claude Projects Integration

Use iOS Developer Agents with [Claude.ai Projects](https://claude.ai).

## Setup

### Individual Agent Project

1. Go to [claude.ai](https://claude.ai) and create a new Project
2. Open the appropriate file from `claude-projects/`:
   - `app-store-validator-instructions.md`
   - `security-auditor-instructions.md`
   - `accessibility-validator-instructions.md`
3. Copy the content (everything after the `---` line)
4. Paste into your Project's **Instructions** field
5. Add your iOS project files to the Project

### Combined Review Project

For comprehensive code review across all three domains:

1. Create a new Project
2. Copy content from `claude-projects/combined-ios-review-instructions.md`
3. Paste into Instructions
4. Upload your key iOS files

## Recommended Files to Upload

| File | Purpose |
|------|---------|
| `Info.plist` | Permission descriptions, capabilities |
| `PrivacyInfo.xcprivacy` | Privacy manifest |
| `*.entitlements` | Entitlements configuration |
| Key `.swift` files | Code review |
| `Podfile` / `Package.swift` | Dependency analysis |

## Using the Project

Once set up, start a conversation:

```
Review my app for App Store submission readiness.
```

```
Check this Swift file for security issues:
[paste code]
```

```
Audit the accessibility of my login screen.
```

## Tips

### Project Naming

Name your Projects clearly:
- "MyApp - App Store Validator"
- "MyApp - Security Auditor"
- "MyApp - Full Code Review"

### Keep Files Updated

Re-upload files when they change significantly. Stale files lead to outdated analysis.

### Combine with Knowledge

Add your design docs, API specs, or style guides to the Project's Knowledge to provide more context.

## Limitations

- Project Instructions have token limits; use the condensed templates in `claude-projects/`
- For full agent prompts, use Claude Code or paste directly into chat

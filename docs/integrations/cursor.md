# Cursor Integration

Use iOS Developer Agents with [Cursor](https://cursor.sh) AI code editor.

## Setup

Copy the `.cursor/` folder to your iOS project:

```bash
cp -r .cursor/ /path/to/your/ios-project/
```

## How It Works

Cursor uses Project Rules in `.cursor/rules/`. Each `.mdc` file contains:

- **Glob patterns**: Define which files activate the rule
- **Instructions**: Guide Cursor's AI when working with matching files

### Available Rules

| Rule | Activates On |
|------|-------------|
| `ios-app-store-validator.mdc` | `*.swift`, `Info.plist`, `PrivacyInfo.xcprivacy`, `*.entitlements` |
| `ios-security-auditor.mdc` | `*.swift`, `*.m`, `*.h`, `Podfile`, `Package.swift`, `*.xcconfig` |
| `ios-accessibility-validator.mdc` | `*.swift`, `*.storyboard`, `*.xib`, `*View.swift`, `*ViewController.swift` |

## Usage

### Automatic Activation

When you edit files matching the glob patterns, Cursor automatically applies the relevant rules. For example:

- Editing `Info.plist` → App Store validation guidance
- Editing `LoginView.swift` → Accessibility checks
- Editing `NetworkManager.swift` → Security considerations

### Chat Commands

In Cursor's chat, reference the rules:

```
@rules Check this file for security issues
```

```
@rules Is this view accessible?
```

## Customization

### Edit Glob Patterns

Adjust which files trigger each rule:

```yaml
---
description: Security audit for iOS projects
globs: ["**/*.swift", "**/Security/**/*"]
---
```

### Add Project Context

Append project-specific context to any rule:

```markdown
## Project Context

- This is a banking app handling sensitive financial data
- Uses Keychain for all credential storage
- Certificate pinning required for all API calls
```

## Combining with Other Rules

You can have multiple rule files. Cursor applies all matching rules.

Add your own `.mdc` files for project-specific guidance:

```yaml
---
description: MyApp coding standards
globs: ["**/*.swift"]
---

# MyApp Standards

- Use dependency injection
- Follow MVVM architecture
- All ViewModels must be @Observable
```

## Troubleshooting

### Rules Not Activating

1. Verify `.cursor/rules/` is in your project root
2. Check glob patterns match your file structure
3. Restart Cursor to reload rules

### Too Much Output

Edit the rules to be more concise, or narrow the glob patterns.

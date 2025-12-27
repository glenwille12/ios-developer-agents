# Getting Started: iOS Teams

Setup guide for iOS development teams wanting consistent validation workflows.

## Team Setup

### 1. Add to Your iOS Repository

Add the integration folders to your iOS project's repository:

```bash
# Clone the agents repo
git clone https://github.com/gygantskiyMatilyock/ios-developer-agents.git

# Copy integrations to your iOS project
cp -r ios-developer-agents/.claude/ /path/to/your/ios-project/
cp -r ios-developer-agents/.cursor/ /path/to/your/ios-project/

# Commit to your repo
cd /path/to/your/ios-project
git add .claude/ .cursor/
git commit -m "Add iOS Developer Agents for validation"
```

### 2. Document Team Workflow

Add to your team's development checklist:

```markdown
## Pre-Submission Checklist

- [ ] Run `/audit-security` - Fix all Critical/High issues
- [ ] Run `/audit-accessibility` - Fix all Critical issues
- [ ] Run `/validate-appstore` - Fix all Blockers
- [ ] Test on physical device
- [ ] Archive and validate in Xcode
```

### 3. Customize for Your Project

Edit the "Project Specific Context" section in each agent to match your app:

```markdown
## Project Specific Context

- **App Type**: Banking app with real-time transfers
- **Authentication**: OAuth2 with biometric fallback
- **Sensitive Data**: Account numbers, transaction history
- **Third-Party SDKs**: Plaid, Firebase Analytics, Sentry
- **Compliance**: PCI-DSS, SOC 2
```

## Consistent Usage Across Tools

| Team Member Uses | Setup |
|-----------------|-------|
| Claude Code | Copy `.claude/` folder |
| Cursor | Copy `.cursor/` folder |
| Claude.ai | Share `claude-projects/*.md` templates |
| Other AI tools | Use `ai-rules/*.txt` files |

## Recommended Team Practices

### Code Review Integration

Add agent checks to your PR template:

```markdown
## Pre-merge Checklist

- [ ] Security audit passed (`/audit-security`)
- [ ] Accessibility audit passed (`/audit-accessibility`)
- [ ] App Store validation passed (`/validate-appstore`)
```

### New Feature Development

1. **Design phase**: Run accessibility validator on mockups/designs
2. **Implementation**: Security auditor during development
3. **Pre-PR**: Full validation sweep
4. **Pre-release**: Final App Store validation

### Onboarding New Team Members

1. Ensure they have Claude Code or Cursor installed
2. Point them to this guide
3. Show them the slash commands available
4. Have them run all 3 audits on a sample PR

## Shared Claude Projects

For teams using Claude.ai:

1. Create a shared Project with `claude-projects/combined-ios-review-instructions.md`
2. Add common project files (Info.plist, key Swift files)
3. Share Project link with team
4. Each team member gets consistent reviews

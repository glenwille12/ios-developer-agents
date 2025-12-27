# Getting Started: Solo Developer

Quick setup guide for individual iOS developers.

## Fastest Way to Start

### Option 1: Claude Code (Recommended)

If you use [Claude Code](https://claude.ai/code):

1. Copy the `.claude/` folder to your iOS project root
2. Run `/validate-appstore`, `/audit-security`, or `/audit-accessibility`

```bash
# From ios-developer-agents repo
cp -r .claude/ /path/to/your/ios-project/
```

### Option 2: Cursor

If you use [Cursor](https://cursor.sh):

1. Copy the `.cursor/` folder to your iOS project root
2. The rules auto-activate when editing Swift, Info.plist, etc.

```bash
cp -r .cursor/ /path/to/your/ios-project/
```

### Option 3: Claude.ai Chat

1. Open `agents/[agent-name]/[agent-name].md`
2. Copy the entire content
3. Paste into a new Claude.ai conversation
4. Add your project files to the conversation

### Option 4: Claude Projects

1. Create a new Project in Claude.ai
2. Copy content from `claude-projects/[agent]-instructions.md`
3. Paste into the Project's "Instructions"
4. Upload your iOS project files

## Which Agent First?

| Scenario | Start With |
|----------|-----------|
| Preparing for App Store submission | App Store Validator |
| Added login/payments/sensitive data | Security Auditor |
| Building new UI screens | Accessibility Validator |
| General code review | Combined (claude-projects/combined-ios-review-instructions.md) |

## Tips for Best Results

1. **Provide context** - Fill in the "Project Specific Context" section at the bottom of each agent prompt
2. **Share relevant files** - Upload Info.plist, PrivacyInfo.xcprivacy, and key Swift files
3. **Be specific** - Tell the agent which screens or features to focus on
4. **Iterate** - Run again after fixes to verify resolution

## Example Workflow

```
1. Copy .claude/ to your project
2. Run: /audit-security
3. Fix critical issues
4. Run: /audit-accessibility
5. Fix accessibility issues
6. Run: /validate-appstore
7. Submit to App Store
```

# Contributing to iOS Developer Agents

Thank you for your interest in contributing! This guide will help you get started.

## Ways to Contribute

- **Report bugs** - Found an agent giving incorrect advice? [Open an issue](https://github.com/gygantskiyMatilyock/ios-developer-agents/issues/new?template=bug_report.md)
- **Suggest improvements** - Ideas for better checks or output? [Request a feature](https://github.com/gygantskiyMatilyock/ios-developer-agents/issues/new?template=feature_request.md)
- **Propose new agents** - Have an idea for a new agent? [Propose it](https://github.com/gygantskiyMatilyock/ios-developer-agents/issues/new?template=new_agent_proposal.md)
- **Submit PRs** - Fix bugs, improve agents, or add new ones

## Development Workflow

### 1. Fork and Clone

```bash
git clone https://github.com/YOUR-USERNAME/ios-developer-agents.git
cd ios-developer-agents
```

### 2. Create a Branch

```bash
git checkout -b feature/your-feature-name
```

### 3. Make Changes

See sections below for specific guidance.

### 4. Test Your Changes

Test with at least one integration method:
- Claude Code: Copy `.claude/` to a test project, run commands
- Cursor: Copy `.cursor/` to a test project, edit relevant files
- Direct chat: Paste prompt into Claude.ai

### 5. Submit a PR

```bash
git add .
git commit -m "Description of changes"
git push origin feature/your-feature-name
```

Then open a Pull Request on GitHub.

## Improving Existing Agents

### What to Change

1. **Source prompt**: `agents/[name]/[name].md` - The source of truth
2. **All integrations**: Update Claude commands, skills, Cursor rules, etc.

### Guidelines

- Keep the same output format structure
- Add new checks to the appropriate step/section
- Include specific guidance, not vague suggestions
- Reference official documentation or standards

### Example: Adding a Check

If adding a new security check:

1. Edit `agents/security-auditor/security-auditor.md`
2. Add to the relevant step (e.g., Step 3: Network Security)
3. Update the output format table if needed
4. Update `.claude/skills/ios-security-auditor/SKILL.md`
5. Update `.cursor/rules/ios-security-auditor.mdc`
6. Update `claude-projects/security-auditor-instructions.md`
7. Update `ai-rules/security-auditor.txt`

## Creating New Agents

### Required Files

| File | Purpose |
|------|---------|
| `agents/[name]/[name].md` | Full agent prompt |
| `agents/[name]/README.md` | Usage guide |
| `.claude/commands/[name].md` | Slash command |
| `.claude/skills/[name]/SKILL.md` | Skill definition |
| `.cursor/rules/[name].mdc` | Cursor rule |
| `claude-projects/[name]-instructions.md` | Claude Projects template |
| `ai-rules/[name].txt` | Generic AI rule |

### Agent Prompt Structure

```markdown
---
name: agent-name
description: When to use this agent
model: opus
color: blue
---

You are an expert [domain]...

## Your Expertise
[Areas of knowledge]

## Process
### Step 1: [First check]
[Detailed instructions]

## Output Format
[Structured template]

## Critical Rules
[Must-follow guidelines]

## Project Specific Context
> **USER INSTRUCTION**: Replace this section...
```

### Quality Checklist

- [ ] Covers the domain comprehensively
- [ ] Provides actionable, specific advice
- [ ] Includes structured output format
- [ ] References official standards/docs
- [ ] Has "Project Specific Context" section
- [ ] All integration files created

## Documentation

- Keep docs concise and scannable
- Use tables for comparisons
- Include code examples where helpful
- Update the main README.md for significant changes

## Code of Conduct

Be respectful and constructive. We're all here to make iOS development better.

## Questions?

Open a GitHub Discussion or Issue. We're happy to help!

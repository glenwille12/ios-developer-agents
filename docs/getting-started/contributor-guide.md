# Getting Started: Contributors

Guide for contributing new agents or improving existing ones.

## Project Structure

```
ios-developer-agents/
  agents/                    # Source prompts (source of truth)
    [agent-name]/
      [agent-name].md        # Full agent prompt
      README.md              # Usage guide

  .claude/                   # Claude Code integration
    commands/                # Slash commands
    skills/                  # Model-invoked skills

  .cursor/                   # Cursor integration
    rules/                   # .mdc rule files

  claude-projects/           # Claude.ai Project templates
  ai-rules/                  # Generic AI tool rules
  docs/                      # Documentation
```

## Creating a New Agent

### 1. Create the Agent Prompt

Create `agents/[your-agent]/[your-agent].md`:

```markdown
---
name: your-agent-name
description: One-line description of when to use this agent
model: opus
color: purple
---

You are an expert [domain] specialist...

## Your Expertise

[List areas of knowledge]

## Process

### Step 1: [First check]
[Detailed instructions]

### Step 2: [Second check]
[Detailed instructions]

## Output Format

[Structured output template]

## Critical Rules

1. [Rule 1]
2. [Rule 2]

## Project Specific Context

> **USER INSTRUCTION**: Replace this section with your project details.
```

### 2. Create Supporting Files

For each new agent, create:

| File | Purpose |
|------|---------|
| `agents/[name]/README.md` | Usage instructions |
| `.claude/commands/[name].md` | Slash command |
| `.claude/skills/[name]/SKILL.md` | Skill definition |
| `.cursor/rules/[name].mdc` | Cursor rule |
| `claude-projects/[name]-instructions.md` | Claude Projects template |
| `ai-rules/[name].txt` | Generic AI rule |

### 3. Test Your Agent

- Test with Claude Code: `/[command-name]`
- Test with Cursor: Edit files matching the glob pattern
- Test with Claude.ai: Paste prompt and run against sample code

## Improving Existing Agents

### Adding New Checks

1. Edit `agents/[name]/[name].md`
2. Add to the relevant step in the process
3. Update output format if needed
4. Update all integration files to match

### Fixing Issues

1. Open an issue describing the problem
2. Fork the repo and create a branch
3. Make changes to the agent prompt
4. Test thoroughly
5. Submit a PR with before/after examples

## Agent Design Guidelines

### Prompts Should Be

- **Comprehensive**: Cover all relevant checks
- **Structured**: Clear steps and output format
- **Actionable**: Provide specific fixes, not just problems
- **Contextual**: Include a Project Specific Context section

### Prompts Should NOT

- Be overly long (aim for focused, scannable content)
- Duplicate information from other agents
- Include outdated guidelines (fetch latest from source)
- Assume specific project structure

## Submission Checklist

- [ ] Agent prompt in `agents/[name]/[name].md`
- [ ] README in `agents/[name]/README.md`
- [ ] Claude command in `.claude/commands/[name].md`
- [ ] Claude skill in `.claude/skills/[name]/SKILL.md`
- [ ] Cursor rule in `.cursor/rules/[name].mdc`
- [ ] Claude Projects template in `claude-projects/`
- [ ] Generic AI rule in `ai-rules/`
- [ ] Updated main README.md with new agent
- [ ] Tested with at least one integration method

## Questions?

Open an issue or discussion on GitHub.

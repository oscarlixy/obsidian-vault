# Claude Code Skills

This folder contains the official [Anthropic Claude Code Skills](https://github.com/anthropics/skills) repository as a git submodule.

## What are Skills?

Skills are reusable instructions and workflows that Claude Code can load dynamically to improve performance on specialized tasks.

## Available Skills

Explore the skills in `notes/claude-skills/` or visit [github.com/anthropics/skills](https://github.com/anthropics/skills)

### Popular Skills

- **brainstorming** - Creative exploration before implementation
- **debugging** - Systematic bug investigation
- **test-driven-development** - TDD workflow implementation
- **code-reviewer** - Review code against plans and standards

## Updating Skills

To update to the latest skills:

```bash
cd obsidian
git submodule update --remote notes/claude-skills
git commit -am "Update Claude skills submodule"
git push
```

## Using Skills

In Claude Code, invoke a skill by name:

```
/Skill brainstorming
/Skill test-driven-development
```

## Resources

- [Official Skills Repo](https://github.com/anthropics/skills)
- [Claude Code Documentation](https://docs.anthropic.com/claude-code)

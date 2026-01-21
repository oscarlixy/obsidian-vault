# 🚀 Quick Start - Using Claude Skills with Obsidian

This guide shows you exactly how to use Claude Code Skills with your Obsidian vault.

## 📋 Prerequisites Check

```bash
# Verify Claude Code is installed
which claude
# Should output: /opt/homebrew/bin/claude
```

---

## 🎯 4 Ways to Use Skills

### Method 1: Built-in Skills (Easiest!)

Many skills are **already built into Claude Code** - no installation needed!

```bash
# Navigate to your vault
cd /Users/oscar/CSlearning/obsidian

# Start Claude Code
claude

# Use built-in skills directly
```

**Built-in Skills Available:**
| Skill | What It Does | Example Usage |
|-------|--------------|---------------|
| `brainstorming` | Explore ideas | "Help me brainstorm blog post ideas about AI" |
| `debugging` | Fix bugs systematically | "My code isn't working, help me debug" |
| `test-driven-development` | TDD workflow | "I want to write tests first for this feature" |
| `code-reviewer` | Review code quality | "Review my recent changes" |

---

### Method 2: Skills from Your Submodule

You already have the official skills in your vault:

```bash
cd /Users/oscar/CSlearning/obsidian
ls notes/claude-skills/skills/
```

**⚠️ IMPORTANT: How to Use Skills**

Skills are invoked using **natural language**, not slash commands:

| ❌ Wrong | ✅ Correct |
|---------|-----------|
| `/Skill brainstorming` | "Help me brainstorm..." |
| `/Skill pdf` | "Process this PDF file" |
| `/Skill doc-coauthoring` | "Help me write this document" |

**Simply describe what you want** - Claude automatically selects the right skill!

---

### Method 3: Copy Skills to Claude's Skills Directory

```bash
# Create the skills directory
mkdir -p ~/.claude/skills

# Copy specific skills you want
cp -r /Users/oscar/CSlearning/obsidian/notes/claude-skills/skills/brainstorming ~/.claude/skills/
cp -r /Users/oscar/CSlearning/obsidian/notes/claude-skills/skills/tapestry ~/.claude/skills/

# Now they're available in any Claude session!
```

---

### Method 4: Install from Plugin Marketplace (Coming Soon)

```bash
# In Claude Code
/plugin marketplace add anthropics/skills
/plugin install doc-coauthoring
```

---

## 💡 Practical Examples for Obsidian

### Example 1: Brainstorming New Note Ideas

```bash
cd /Users/oscar/CSlearning/obsidian
claude
```

```
You: I want to write about AI productivity tools. Can you help me brainstorm?

Claude: [Uses brainstorming skill automatically]

Here are some angles to explore:
1. Comparison of AI tools for different workflows
2. Case studies of AI productivity transformations
3. Technical deep-dives into specific tools
4. ROI analysis of AI adoption

Which direction interests you most?
```

**Then create a note in Obsidian:**
```markdown
# AI Productivity Tools

## Angles to Explore
- [ ] Comparison article
- [ ] Case studies
- [ ] Technical deep-dive
- [ ] ROI analysis

## Related Notes
- [[Top Skills for Obsidian]]
```

---

### Example 2: File Organization

```bash
cd /Users/oscar/CSlearning/obsidian
claude
```

```
You: My notes folder is getting messy. Can you help organize it?

Claude: [Uses file-organizer skill]

I can see your notes structure. Here are my suggestions:
1. Group by topic (AI, Development, Personal)
2. Create an Archive folder for old notes
3. Add consistent naming convention

Shall I proceed with reorganization?
```

---

### Example 3: Article Research

```bash
cd /Users/oscar/CSlearning/obsidian
claude
```

```
You: Extract the main points from this article: [paste URL]

Claude: [Uses article-extractor skill]

# Article Summary

## Key Points
- Point 1...
- Point 2...
- Point 3...

## Quotes
> "Notable quote..."

## Tags
#research #article-summary
```

**Save to Obsidian:**
```markdown
# Article: [Title]

{{Claude's output here}}

## Source
[Original URL](...)

## Date
2026-01-21
```

---

## 🎓 Common Workflows

### Workflow 1: Research Note Taking
```bash
# Terminal
cd /Users/oscar/CSlearning/obsidian
claude
```
```
You: Use article-extractor on this URL: https://example.com/article
Claude: [Extracts content]
You: Now use tapestry to connect this to my existing notes
Claude: [Finds related notes and creates links]
```

### Workflow 2: Content Creation
```bash
# Terminal
cd /Users/oscar/CSlearning/obsidian
claude
```
```
You: I want to write about [topic]. Help me brainstorm first.
Claude: [Generates ideas and questions]
You: Great, now help me outline the article.
Claude: [Creates structured outline]
You: Now help me write section 1.
Claude: [Drafts content]
```

### Workflow 3: Code Documentation
```bash
# Terminal
cd /Users/oscar/CSlearning/obsidian
claude
```
```
You: Review this code and suggest improvements
Claude: [Uses code-reviewer skill]
You: Now help me write documentation for it
Claude: [Uses doc-coauthoring skill]
```

---

## 🔧 Quick Reference

### Check Available Skills
```bash
# In Claude Code
/skills
```

### Use a Skill
```bash
# Explicit invocation
/Skill brainstorming

# Or just describe what you want
"Help me brainstorm..."
"Can you review this code?"
"I need to organize my files"
```

### Skill Parameters
Some skills accept parameters:
```bash
/Skill brainstorming --topic "AI tools" --depth "detailed"
/Skill file-organizer --directory "notes/" --dry-run
```

---

## 📱 Obsidian Integration Tips

### Tip 1: Create Skill Command Notes
```markdown
# Claude Commands

## File Organization
```bash
cd ~/obsidian && claude
# Then: Help me organize my notes
```

## Brainstorming
```bash
cd ~/obsidian && claude
# Then: Brainstorm ideas for [topic]
```

## Research
```bash
cd ~/obsidian && claude
# Then: Extract article content from [URL]
```
```

### Tip 2: Use Obsidian Templates with Claude
```markdown
---
date: {{date}}
skill: brainstorming
---

# {{title}}

## Initial Thoughts
[Claude brainstorming output goes here]

## Related Notes
- [[Link]]
- [[Link]]

## Tags
#idea #wip
```

### Tip 3: Link Claude Sessions to Notes
```markdown
# Project: [Name]

## Claude Session
```bash
cd ~/obsidian
claude
# Session date: 2026-01-21
# Skills used: brainstorming, tapestry
```

## Outcomes
- [ ] Action item 1
- [ ] Action item 2
```

---

## 🆘 Troubleshooting

**Problem:** Skill not found
```bash
# Solution: Check available skills
claude
> /skills
```

**Problem:** Skill not working as expected
```bash
# Solution: Be more specific
Claude: "I'm not sure what you need"
You: "Use the brainstorming skill to explore blog post ideas about AI tools"
```

**Problem:** Need to exit Claude
```bash
# Press Ctrl+D or type
exit
```

---

## 📚 Next Steps

1. **Try the brainstorming skill:**
   ```bash
   cd /Users/oscar/CSlearning/obsidian
   claude
   # Type: Help me brainstorm ways to organize my Obsidian vault
   ```

2. **Explore your skills submodule:**
   ```bash
   ls notes/claude-skills/skills/
   ```

3. **Read more about each skill:**
   ```bash
   cat notes/claude-skills/skills/brainstorming/SKILL.md
   ```

---

## 🔗 Related Notes

- [[Top Skills for Obsidian]] - Detailed skill descriptions
- [[Brainstorming Workflow]] - Brainstorming deep-dive
- [[Claude Code Skills]] - Skills repository info

---

*Last updated: 2026-01-21*

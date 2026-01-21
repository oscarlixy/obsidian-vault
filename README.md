# Obsidian Vault

A personal knowledge base using Obsidian.

## Structure

```
obsidian/
├── .obsidian/       # Obsidian app configuration
├── notes/           # Main notes
├── templates/       # Note templates
├── assets/          # Images and attachments
├── daily/           # Daily notes
└── README.md        # This file
```

## Getting Started

1. Open this folder in Obsidian
2. Start creating notes in the `notes/` folder
3. Use templates from `templates/` for quick note creation

## Features

- [[Internal linking]] with `[[Note Name]]`
- #tags for organization
- Markdown support
- Daily notes workflow

## GitHub Integration

This vault is connected to GitHub: https://github.com/oscarlixy/obsidian-vault

**Sync changes:**
```bash
cd obsidian
git pull          # Pull latest changes
git add .
git commit -m "your message"
git push          # Push changes
```

## Claude Code Integration

### Option 1: Use Claude Code directly

Claude Code can directly read and edit your notes:

```bash
cd obsidian
# Ask Claude to work with your notes
```

### Option 2: Obsidian Claude Plugin

Install the **Text Generator** or **Copilot** plugin in Obsidian:

1. Open Settings → Community Plugins
2. Browse and search for "Text Generator"
3. Install and enable
4. Configure with your Claude API key

Then you can use AI directly inside Obsidian!


# Plugin Template

This directory provides a template structure for creating plugins for the Scientific Research Writing Marketplace.

## Directory Structure

```
plugin-template/
├── .claude-plugin/
│   └── plugin.json       # Plugin configuration
├── skills/
│   └── example-skill/
│       └── SKILL.md      # Skill definition
├── commands/
│   └── example-command/
│       └── COMMAND.md    # Command definition
├── agents/
│   └── example-agent/
│       └── AGENT.md      # Agent definition
└── README.md             # Plugin documentation
```

## Creating a New Plugin

### 1. Copy the Template

```bash
cp -r plugin-template my-new-plugin
cd my-new-plugin
```

### 2. Update plugin.json

Edit `.claude-plugin/plugin.json` with your plugin details:

```json
{
  "name": "my-new-plugin",
  "version": "0.1.0",
  "description": "Description of your plugin",
  "skills": [...],
  "commands": [...],
  "agents": [...]
}
```

### 3. Create Your Skills

Add skills in the `skills/` directory. Each skill has its own directory with a `SKILL.md` file.

### 4. Create Your Commands (Optional)

Add commands in the `commands/` directory. Each command has its own directory with a `COMMAND.md` file.

### 5. Create Your Agents (Optional)

Add agents in the `agents/` directory. Each agent has its own directory with an `AGENT.md` file.

### 6. Update README.md

Document your plugin with installation instructions and usage examples.

### 7. Publish to GitHub

1. Create a new repository on GitHub
2. Push your plugin code
3. Update the marketplace.json in the main marketplace repository with your plugin's URL

## Skill Guidelines

### SKILL.md Format

```markdown
---
name: skill-name
description: Brief description
triggers:
  - keyword1
  - keyword2
---

# Skill Name

Detailed description...

## When to Use
- Condition 1
- Condition 2

## Instructions
Step-by-step instructions...

## Examples
Example usage...

## Checklist
- [ ] Verification items...
```

## Command Guidelines

### COMMAND.md Format

```markdown
---
name: command-name
description: Brief description
---

# Command Name

## Usage
/command-name [options] [arguments]

## Options
- `--option`: Description

## Examples
Example usage...

## Workflow
Step-by-step workflow...
```

## Agent Guidelines

### AGENT.md Format

```markdown
---
name: agent-name
description: Brief description
model: sonnet
tools:
  - Read
  - Grep
---

# Agent Name

## Purpose
Detailed purpose...

## Capabilities
- Capability 1
- Capability 2

## Instructions
Step-by-step instructions...
```

## Testing Your Plugin

Before submitting to the marketplace:

1. Test all skills trigger correctly
2. Verify commands execute as expected
3. Check agents produce expected outputs
4. Validate plugin.json syntax
5. Update version number in plugin.json

## Submitting to the Marketplace

1. Ensure your plugin is in a public GitHub repository
2. Test installation via `/plugin install your-username/your-plugin`
3. Submit a PR to update the marketplace.json with your plugin entry

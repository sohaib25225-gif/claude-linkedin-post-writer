# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Overview

This repository contains custom Claude skills - specialized agents that extend Claude's capabilities for specific tasks. The repository is structured as a collection of skills under the `.claude` directory.

## Current Skills

### LinkedIn Post Writer (`/.claude/linkedin-post-writer/`)
- **Purpose**: Generates professional LinkedIn posts based on topic input
- **Files**:
  - `skill.md` - Core skill definition and instructions
  - `README.md` - Usage documentation and examples
- **Features**: Attention-grabbing hooks, clear content, relevant hashtags, strong CTAs
- **Customization**: Tone (Professional/Casual/Inspirational), Length (Short/Medium/Long), Industry-specific posts

## Code Architecture

### Skill Definition Structure
Each skill follows this pattern:
- **Skill Directory**: `/.claude/<skill-name>/`
- **Core Definition**: `skill.md` contains the agent's purpose, responsibilities, and output rules
- **Documentation**: `README.md` provides usage examples and feature overview

### Skill Configuration
Skills are defined using markdown files that specify:
- **Purpose**: High-level agent role and responsibilities
- **Input Format**: Expected user input parameters
- **Output Rules**: Formatting and content requirements
- **Guidelines**: Tone, style, and formatting constraints
- **Examples**: Sample inputs and outputs for training

## Development Workflow

### Adding New Skills
1. Create directory under `/.claude/<skill-name>/`
2. Define `skill.md` with agent instructions
3. Add `README.md` for documentation
4. Test the skill through Claude

### Modifying Existing Skills
1. Edit the `skill.md` file to update agent behavior
2. Update `README.md` if feature changes
3. Test modifications through Claude interaction

### Git Workflow
- Main branch: `master`
- Remote: GitHub repository for sharing skills
- Commit messages should clearly describe skill additions or modifications

## Repository Structure

```
/
├── .claude/                          # Main skills directory
│   └── linkedin-post-writer/        # LinkedIn post generation skill
│       ├── README.md                # Usage documentation
│       └── skill.md                 # Core skill definition
├── .git/                            # Git repository
└── (other hidden directories)
```

## Common Commands

### Git Operations
```bash
# Check repository status
git status

# View recent commits
git log --oneline -10

# Add new skill files
git add .claude/<skill-name>/

# Commit changes
git commit -m "Add/update <skill-name> skill"

# Push to remote
git push origin master
```

### Testing Skills
- Skills are tested by interacting with Claude directly
- Use the skill invocation syntax (e.g., `/linkedin-post-writer` if configured)
- Test with various inputs to validate behavior

## Skill Configuration

### Claude Integration
- Skills are automatically detected by Claude from the `.claude` directory
- Each skill directory becomes available as a specialized agent
- Skills can be invoked through Claude's interface

### Skill Parameters
Skills accept parameters defined in their `skill.md` file:
- **Required**: Core topic/description
- **Optional**: Tone, length, industry, etc.
- **Output**: Formatted response based on skill rules

## Best Practices

### Skill Design
- Keep skill definitions focused and specific
- Use clear, actionable instructions in `skill.md`
- Provide comprehensive examples in `README.md`
- Test edge cases and various input types

### Documentation
- Include realistic examples in README files
- Document all available parameters and options
- Show expected output formats
- Include customization options

### Version Control
- Commit skills individually for clear history
- Use descriptive commit messages
- Consider creating separate repositories for complex skills
- Maintain documentation with skill updates

## Repository Context

This repository serves as a collection of reusable Claude skills. The current focus is on content creation tools (LinkedIn posts), but the structure supports any specialized agent functionality. Skills can be shared, forked, and extended by the community.

## Related Files
- `/.claude/linkedin-post-writer/skill.md` - Core LinkedIn post writer agent definition
- `/.claude/linkedin-post-writer/README.md` - Usage guide and examples
- `.git/config` - Repository configuration and remote URL
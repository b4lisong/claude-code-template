---
allowed-tools: all
description: Update the Claude Code template to the latest version with AI-powered migration
---
# Update Template Command

**Usage:** `/update-template`

**Purpose:** Update your project to the latest Claude Code template version while preserving your project-specific customizations.

## How It Works

This command executes the official template update process with intelligent migration:

1. **Downloads latest setup script** from GitHub
2. **Detects existing customizations** in your CLAUDE.md file  
3. **Offers AI-powered extraction** to preserve your project settings
4. **Creates automatic backups** of your current configuration
5. **Guides you through migration** with interactive options

## Pre-Update Safety Checks

Before running the update, I'll verify:
- Current working directory is clean (no uncommitted changes)
- Backup existing instruction files automatically
- Confirm you want to proceed with the update

## Update Process

The command runs:
```bash
curl -sL https://raw.githubusercontent.com/b4lisong/claude-code-template/main/setup.sh | bash
```

**Interactive Options You'll See:**
- **[1] AI Extraction (Recommended)** - Let AI automatically extract your customizations
- **[2] Manual Migration** - Create PROJECT-SPECIFIC-CLAUDE.md template for manual editing
- **[3] Skip Migration** - Update template only, migrate later

## AI-Powered Migration Benefits

When you choose AI extraction:
- **Context Understanding** - AI grasps the intent behind your customizations
- **Complete Extraction** - Handles complex nested content and edge cases
- **Smart Categorization** - Places content in appropriate sections automatically
- **Proper Formatting** - Maintains markdown structure and code blocks
- **Safe Process** - Shows preview and requires confirmation before applying

## What Gets Updated

**Template Files (CLAUDE.md):**
- Core methodology and workflows
- Universal quality standards
- Command definitions and patterns
- Bug fixes and new features

**Preserved Files:**
- PROJECT-SPECIFIC-CLAUDE.md (your customizations)
- All your project files and code
- Git history and branches
- Custom hooks and settings

## Post-Update Steps

After successful update:
1. **Review changes** - Check what template updates were applied
2. **Validate customizations** - Ensure your project-specific settings are preserved
3. **Test functionality** - Run `/check` to verify everything works
4. **Continue development** - Resume using updated template features

## Recovery Options

If something goes wrong:
- **Backup files preserved** - `CLAUDE.md.backup-TIMESTAMP` files created automatically
- **Use `/extract-customizations`** - Re-extract from backup if needed
- **Manual restoration** - Copy from backup files if necessary
- **Git recovery** - Use git to restore previous state if needed

## Error Handling

**Common Issues and Solutions:**
- **"curl: command not found"** - Install curl or use alternative download method
- **Network errors** - Check internet connection, retry the command
- **Permission errors** - Ensure write access to project directory
- **Migration conflicts** - Choose manual migration option for complex cases

## Best Practices

**Before Update:**
- Commit any uncommitted work
- Review current CLAUDE.md for important customizations
- Note any specific project requirements

**During Update:**
- Choose AI extraction for most reliable migration
- Review preview of extracted content carefully
- Confirm migration only if content looks correct

**After Update:**
- Test key workflows to ensure nothing broke
- Update team members about new template features
- Refine PROJECT-SPECIFIC-CLAUDE.md if needed

## Template Update Frequency

**Recommended schedule:**
- **Check weekly** for new template versions
- **Update immediately** for security fixes
- **Plan quarterly** major feature updates
- **Update before major project milestones** for latest tooling

## Integration with Development Workflow

**Update workflow example:**
```bash
# Start Claude Code session
claude

# Update template with latest features
/update-template

# Choose [1] AI Extraction when prompted
# Review extracted customizations
# Confirm migration

# Resume development with updated template
/dev "new feature with latest template"
```

This command ensures you always have the latest template improvements while maintaining your project's unique requirements and customizations.
---
allowed-tools: all
description: Update the Claude Code template to the latest version with manual migration guidance
---
# Update Template Command

**Usage:** `/update-template`

**Purpose:** Update your project to the latest Claude Code template version while preserving your project-specific customizations.

## How It Works

This command executes the official template update process with manual migration guidance:

1. **Downloads latest setup script** from GitHub
2. **Detects existing customizations** in your CLAUDE.md file  
3. **Creates automatic backups** of your current configuration
4. **Provides manual migration guidance** to preserve your project settings
5. **Guides you through the process** with clear instructions

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

**What Happens During Update:**
- **Automatic Backup** - Your existing CLAUDE.md is backed up with timestamp
- **Manual Migration Required** - You'll need to manually migrate customizations to PROJECT-SPECIFIC-CLAUDE.md
- **Template Updated** - CLAUDE.md is updated to the latest template version
- **Clear Guidance** - Setup provides step-by-step migration instructions

## Manual Migration Process

The update process will:
- **Create timestamped backup** of your current CLAUDE.md
- **Show migration warning** with backup filename for your reference
- **Create PROJECT-SPECIFIC-CLAUDE.md template** for your customizations
- **Provide clear instructions** on what to migrate and how
- **Preserve all your content** in the backup file for safe migration

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
- Note the backup filename provided during setup
- Follow the manual migration guidance provided
- Review your backup file to identify project-specific content

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

# Note the backup filename displayed
# Follow manual migration guidance
# Migrate customizations to PROJECT-SPECIFIC-CLAUDE.md

# Resume development with updated template
/dev "new feature with latest template"
```

This command ensures you always have the latest template improvements while maintaining your project's unique requirements and customizations.
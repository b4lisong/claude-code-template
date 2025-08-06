# Claude Code Commands Reference

Quick reference for all available Claude Code commands in this template.

## 🚀 Primary Development Commands

### `/dev <feature description>`
**Purpose:** Test-Driven Development workflow  
**Example:** `/dev "user authentication with JWT"`  
**What it does:**
- Writes failing tests first
- Implements minimal code to pass tests
- Refactors with test safety net
- Ensures quality throughout

### `/check`
**Purpose:** Run quality checks (linting, tests, formatting)  
**Example:** `/check`  
**What it does:**
- Runs project-appropriate linters
- Executes test suite
- Checks code formatting
- Reports issues with exit code 2

### `/ship <commit message>`
**Purpose:** Create professional commits  
**Example:** `/ship "add user authentication"`  
**What it does:**
- Stages changes
- Creates commit with message
- Updates CHANGELOG.md
- Ensures no Claude attribution

## 🔧 Code Improvement Commands

### `/debug <issue description>`
**Purpose:** Systematic debugging workflow  
**Example:** `/debug "login fails with 500 error"`  
**What it does:**
- Reproduces the issue
- Identifies root cause
- Implements fix with tests
- Verifies resolution

### `/refactor <component name>`
**Purpose:** Safe code improvement  
**Example:** `/refactor "user service"`  
**What it does:**
- Analyzes current implementation
- Ensures test coverage exists
- Refactors step-by-step
- Maintains functionality

## 📋 Planning & Documentation Commands

### `/plan <project description>`
**Purpose:** Generate development roadmap  
**Example:** `/plan "e-commerce checkout system"`  
**What it does:**
- Breaks down into milestones
- Creates task priorities
- Estimates timelines
- Identifies dependencies

### `/claude-md <action>`
**Purpose:** Manage template and project-specific instruction files  
**Available actions:**
- `backup` - Create timestamped backups of instruction files
- `update-mastery` - Update skill progression in PROJECT-SPECIFIC-CLAUDE.md
- `create-project` - Create PROJECT-SPECIFIC-CLAUDE.md if missing
- `merge-customizations` - Help migrate old CLAUDE.md customizations

**Examples:**
- `/claude-md backup` - Backup both instruction files
- `/claude-md create-project` - Set up project customizations
- `/claude-md update-mastery` - Track learning progress

**What it does:**
- Manages two-file instruction system (CLAUDE.md + PROJECT-SPECIFIC-CLAUDE.md)
- Preserves project customizations during template updates
- Tracks learning objectives and skill progression
- Provides safe backup and migration capabilities

### `/extract-customizations <backup_file>`
**Purpose:** AI-powered extraction of customizations from old CLAUDE.md files  
**Example:** `/extract-customizations CLAUDE.md.backup-20250106-143022`  

**What it does:**
- Uses Claude Code AI to intelligently analyze old CLAUDE.md files
- Distinguishes between template content and project-specific customizations
- Automatically extracts and categorizes customizations by type
- Generates properly formatted PROJECT-SPECIFIC-CLAUDE.md content
- Shows preview of extracted content before applying changes

**AI Analysis Process:**
- **Language Rules**: Detects TypeScript, Python, Rust, Go quality standards
- **Project Structure**: Identifies directory layouts and naming conventions  
- **Team Standards**: Extracts code review, deployment, and workflow practices
- **Learning Goals**: Captures skill progression and mastery tracking
- **Domain Rules**: Finds compliance requirements (HIPAA, PCI DSS, GDPR)
- **Quality Gates**: Identifies custom validation and testing requirements

**Advantages over Manual Migration:**
✅ **Context Understanding** - AI grasps intent behind customizations  
✅ **Complete Extraction** - Handles complex nested content and edge cases  
✅ **Smart Categorization** - Places content in appropriate sections automatically  
✅ **Proper Formatting** - Maintains markdown structure and code blocks  
✅ **Safe Process** - Always requires user confirmation before applying  

**Usage Scenarios:**
- **Template Updates**: Primary migration method during setup.sh upgrades
- **Manual Migration**: Extract customizations from backup files manually
- **Recovery**: Restore customizations from old backup files
- **Project Conversion**: Migrate single-file projects to two-file system

## 🛠️ Utility Commands

### `/help [command]`
**Purpose:** Get help and examples  
**Example:** `/help dev`  
**What it does:**
- Shows command documentation
- Provides usage examples
- Lists available options

### `/prompt <context>`
**Purpose:** Generate handoff prompt for other LLMs  
**Example:** `/prompt "current sprint progress"`  
**What it does:**
- Summarizes project state
- Creates context for handoff
- Includes relevant files
- Formats for LLM consumption

### `/agents`
**Purpose:** Manage specialized sub-agents for complex tasks  
**Example:** `/agents` (opens sub-agent interface)  
**What it does:**
- Create and configure specialized sub-agents
- Delegate complex tasks to focused agents
- Coordinate multi-agent workflows
- Access template-specific agents (TDD-Coach, Quality-Enforcer, Strategic-Planner, Refactoring-Specialist)

## 📁 Two-File Instruction System

The template uses a dual-file system for safe template updates:

### CLAUDE.md (Template Instructions)
- Core methodology and workflows
- Universal quality standards  
- Command definitions and patterns
- **Safe to update** when template upgrades

### PROJECT-SPECIFIC-CLAUDE.md (Your Customizations)  
- Language-specific quality rules
- Project structure definitions
- Team standards and practices
- Learning objectives and skill progression
- **Preserved across template updates**

### File Management Workflow
```
/claude-md create-project      # Set up project customizations
/claude-md backup             # Backup before major changes
/claude-md update-mastery     # Track learning progress weekly
/claude-md merge-customizations # Migrate old customizations
```

## 🎯 Quick Workflows

### Standard Development Flow
```
/dev "new feature"     # TDD implementation
/check                 # Verify quality
/ship "add feature"    # Commit changes
```

### Bug Fix Flow
```
/debug "error description"   # Find and fix
/check                      # Verify fix
/ship "fix: error"         # Commit fix
```

### Refactoring Flow
```
/check                     # Ensure tests pass
/refactor "component"      # Improve code
/check                     # Verify nothing broke
/ship "refactor: component" # Commit improvements
```

### Sub-Agent Workflow Examples
```
/agents                    # Open sub-agent interface
# Use TDD-Coach for complex test design
# Use Quality-Enforcer for parallel issue fixing  
# Use Strategic-Planner for comprehensive roadmaps
# Use Refactoring-Specialist for safe code improvements
```

### Template Update Workflows

#### AI-Powered Template Update (Recommended)
```bash
# Update existing project with AI migration
curl -sL https://raw.githubusercontent.com/b4lisong/claude-code-template/main/setup.sh | bash

# Interactive process:
# [1] AI Extraction (Recommended) ← Choose this
# ✅ Backup created automatically
# ✅ AI analyzes your customizations  
# ✅ Preview extracted content
# ✅ Confirm migration: Y
# ✅ Migration complete!

# Resume development with latest features:
claude
/dev "new feature with updated template"
```

#### Manual AI Extraction
```bash
# Extract customizations from backup manually
claude                                        # Start Claude Code
/extract-customizations backup-file.md       # AI extract from backup
# Preview shown → Confirm → Applied

# Alternative command:
/claude-md extract-ai backup-file.md         # Same AI extraction
```

#### Template Update with Manual Migration
```bash
# Update template, migrate customizations manually
curl -sL https://raw.githubusercontent.com/b4lisong/claude-code-template/main/setup.sh | bash

# Choose option [2] Manual Migration
# ✅ PROJECT-SPECIFIC-CLAUDE.md template created
# ✅ Your backup preserved: CLAUDE.md.backup-file

# Manually migrate your customizations:
/claude-md merge-customizations              # Get migration guidance
```

#### Recovery from Backup
```bash  
# Restore customizations from old backup
claude
/extract-customizations old-backup.md       # AI extract from any backup
# Or manually restore specific sections to PROJECT-SPECIFIC-CLAUDE.md
```

## 💡 Pro Tips

1. **Always start with `/dev`** for new features - TDD prevents bugs
2. **Run `/check` before `/ship`** - Ensure quality standards
3. **Use `/plan` for complex features** - Break down before building
4. **Use AI extraction for template updates** - More reliable than manual migration
5. **Customize PROJECT-SPECIFIC-CLAUDE.md** - Add your project's specific needs
6. **Run `/claude-md backup`** - Before major instruction changes
7. **Update `/claude-md update-mastery`** - Weekly learning progress tracking
8. **Preview AI extractions** - Always review before confirming migrations
9. **Use `/agents` for complex tasks** - Delegate to specialized sub-agents

## 🚫 Command Guidelines

- **NO emojis** in commits (enforced by hooks)
- **NO Claude attribution** in messages
- **Always delete old code** when replacing
- **Exit code 2** means issues found - fix before continuing

## 🔍 Troubleshooting

### Hook Failures
If `/check` keeps failing:
1. Run the specific linter manually
2. Fix all reported issues
3. Re-run `/check`

### Command Not Found
Ensure you're in a Claude Code session and the template is properly installed.

### Quality Check Issues
- **TypeScript:** Fix type errors with `tsc --noEmit`
- **ESLint:** Auto-fix with `eslint . --fix`
- **Prettier:** Format with `prettier --write .`
- **Python:** Format with `black .`
- **Rust:** Format with `cargo fmt`

---
For detailed command documentation, use `/help <command>` within Claude Code.
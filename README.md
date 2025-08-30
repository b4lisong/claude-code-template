# Claude Code Template

**Professional development setup with Claude Code for systematic, high-quality software development.**

## Summary

A production-ready Claude Code template that transforms your development workflow with TDD-first methodology, automated quality checks, and professional standards. Get from zero to shipping features in under 5 minutes with power commands, git hooks, and multi-language support.

**Value Proposition:** Replace ad-hoc development with systematic workflows that prevent bugs, ensure quality, and accelerate delivery.

**Next Step:** Run the one-line setup below, then start with `/dev "your first feature"` for immediate TDD development.

**Recommended path:** Follow the Quick Start → `/dev` workflow → `/check` → `/ship` cycle for optimal results.

## Quick Start

**Prerequisites:** Install [Claude Code](https://docs.anthropic.com/en/docs/claude-code)

### One-Line Setup

```bash
curl -H 'Cache-Control: no-cache' -sL https://raw.githubusercontent.com/b4lisong/claude-code-template/main/setup.sh | bash
```

**For existing projects, use submodule installation instead:**
```bash
git submodule add https://github.com/b4lisong/claude-code-template.git claude-code-template
cd claude-code-template && ./setup.sh --submodule
```

**Then start coding:**
```bash
claude                                # Start Claude Code
/dev "implement user authentication"  # Your first TDD feature
```

**Success indicators:** When working, you'll see `[OK]` messages and automatic test execution.

## What You Get

### 🎯 **10 Power Commands**
- **`/dev`** - TDD-first development (primary command)
- **`/debug`** - Systematic debugging workflow
- **`/refactor`** - Code improvement with safety nets
- **`/check`** - Quality verification (zero tolerance)
- **`/ship`** - Professional commits
- **`/plan`** - Strategic planning
- **`/help`** - Interactive guidance
- **`/prompt`** - Context handoff
- **`/claude-md`** - Manage template and project-specific instructions
- **`/extract-customizations`** - AI-powered customization migration (EXPERIMENTAL)

### 🛡️ **Quality Automation**
- **Git hooks** prevent Claude attribution and emojis in commits
- **Pre-commit hooks** run quality checks automatically
- **Smart linting** for multiple languages (JS, Python, Rust, Go)
- **Web search validation** ensures current information

### 📋 **Professional Standards**
- **Test-driven development** as the default workflow
- **Zero emoji policy** in code and commits
- **No Claude attribution** in commit messages
- **Systematic debugging** and refactoring processes

## Core Workflow

```bash
/dev "feature name"    # Write tests first, implement with TDD
/check                 # Verify quality (all tests pass, no lint issues)
/ship "description"    # Professional commit with clean history
```

<details>
<summary>### Advanced Workflows</summary>

#### Systematic Debugging
```bash
/debug "issue description"  # Structured debugging process
```

#### Code Quality Improvement
```bash
/refactor "component name"  # Safe refactoring with tests
```

#### Strategic Planning
```bash
/plan "project goals"      # Generate development roadmap
```

</details>

## Configuration

### Two-File Instruction System

The setup creates a dual-file instruction system for safe template updates:

- **`CLAUDE.md`** - Template instructions (updated with template versions)
  - Core methodology and workflows
  - Universal quality standards
  - Command definitions and patterns
  - Safe to update when template upgrades

- **`PROJECT-SPECIFIC-CLAUDE.md`** - Your project customizations (preserved across updates)
  - Language-specific quality rules
  - Project structure definitions
  - Team standards and practices
  - Learning objectives and skill progression

### Additional Configuration

- `.claude/hooks/smart-lint.sh` - Quality enforcement hooks
- `.claude/settings.json` - Claude Code settings
- Language-specific tooling configurations

## What is Claude Code?

**Claude Code** is an AI-powered CLI that embeds Claude directly into your terminal for agentic development:

- **Full codebase awareness** - Understands your project without manual context
- **Multi-file coordination** - Makes complex changes across files
- **End-to-end workflows** - From tests to commits, all in natural language
- **Works with any editor** - VS Code, JetBrains, Vim, etc.

### Example

Traditional workflow:
```
1. Read docs → 2. Write code → 3. Debug → 4. Repeat...
```

Agentic workflow:
```bash
/dev "user auth with JWT"  # Claude writes tests, implements, validates
/check                     # Quality gates pass automatically  
/ship "add JWT auth"       # Professional commit ready
```

## Alternative Setup

### GitHub Template
1. Click "Use this template" → Create repository
2. Clone: `git clone https://github.com/yourusername/your-repo.git`
3. Start: `claude` then `/dev "your feature"`

### Existing Project
```bash
# Preserves your existing project customizations
curl -H 'Cache-Control: no-cache' -sL https://raw.githubusercontent.com/b4lisong/claude-code-template/main/setup.sh | bash
```

### Submodule Installation
**Add Claude Code template as a submodule to your existing project:**

```bash
# Add template as submodule
git submodule add https://github.com/b4lisong/claude-code-template.git claude-code-template

# Initialize and update submodule
git submodule update --init --recursive

# Run submodule installation (creates symbolic links in parent directory)
cd claude-code-template
./setup.sh --submodule

# Start using Claude Code from your project root
cd ..
claude
```

**What the submodule setup does:**
- ✅ **Creates symbolic links** in your project root: `CLAUDE.md`, `PROJECT-SPECIFIC-CLAUDE.md`, `.claude/`
- ✅ **Installs git hooks** in your main repository for quality enforcement
- ✅ **Preserves your existing files** with automatic backup
- ✅ **Updates your .gitignore** with backup exclusion patterns
- ✅ **Works from your project root** - all Claude Code commands function normally

**Auto-detection:** The script automatically detects when you're in a `claude-code-template` submodule and prompts for submodule installation.

**Manual options:**
```bash
./setup.sh --submodule                    # Use parent directory (..)
./setup.sh --submodule --parent-dir ../.. # Custom parent directory
./setup.sh --help                         # Show all options
```

### Project Customization
After setup, customize `PROJECT-SPECIFIC-CLAUDE.md` for your project:
```bash
claude                           # Start Claude Code
/claude-md create-project        # Set up project customizations
/claude-md update-mastery        # Track your learning goals
```

## Template Updates & Migration

### 📋 **Template Updates with Manual Migration**

Updating to the latest template features provides clear migration guidance to preserve all your project customizations:

```bash
# Update existing project to latest template
curl -H 'Cache-Control: no-cache' -sL https://raw.githubusercontent.com/b4lisong/claude-code-template/main/setup.sh | bash
```

### **Manual Migration Process**

When customizations are detected in your CLAUDE.md:

**Automatic Backup & Guidance** 🎯
- Setup creates timestamped backup of your existing CLAUDE.md
- Provides clear migration warning with backup filename
- Creates PROJECT-SPECIFIC-CLAUDE.md template for your customizations  
- Shows step-by-step migration instructions

**Experimental Alternative** 🧪
- `/extract-customizations` command available for AI-powered extraction (EXPERIMENTAL)
- Use manual migration for most reliable results

### **Manual Migration Advantages**

✅ **Reliable Process** - Proven method that preserves all customizations accurately  
✅ **Complete Control** - You decide exactly what to migrate and how  
✅ **User Understanding** - You understand your project's specific needs and context  
✅ **No Risk of Misinterpretation** - Manual review ensures nothing is lost or changed incorrectly  

### **Migration Safety Features**

🛡️ **Multiple Backups** - Timestamped backups created automatically  
🛡️ **Clear Instructions** - Step-by-step guidance provided during setup  
🛡️ **Backup Preservation** - Original backups always preserved for reference  
🛡️ **Template Creation** - PROJECT-SPECIFIC-CLAUDE.md template created automatically  

### **Experimental AI Extraction**

You can also try the experimental AI extraction on any backup file:

```bash
claude                                           # Start Claude Code
/extract-customizations CLAUDE.md.backup-file   # EXPERIMENTAL AI extract from backup
/claude-md merge-customizations                  # Manual migration guidance (EXPERIMENTAL, WIP)
```

### **What Should Be Migrated**

When migrating manually, look for these customizations in your backup:
- **Language-specific quality rules** (TypeScript, Python, Rust, etc.)
- **Project structure definitions** and naming conventions  
- **Team standards and practices** (code review, deployment)
- **Learning objectives** and skill progression tracking
- **Domain-specific requirements** (compliance, performance)
- **Custom quality gates** and validation rules

### **Update Workflow Example**

```bash
# Run template update
curl -sL https://raw.githubusercontent.com/b4lisong/claude-code-template/main/setup.sh | bash

# Setup detects customizations and shows:
# ⚠️ Manual migration required for your customizations
# 📄 Backup created: CLAUDE.md.backup-20250106-143022
# 
# Step-by-step migration guidance provided:
# 1. Review your backup file for customizations
# 2. Copy relevant content to PROJECT-SPECIFIC-CLAUDE.md
# 3. Remove template examples and add your actual content
# 4. Use /claude-md commands for ongoing management

# Resume development:
claude
/dev "new feature with latest template"
```

## Key Features

- **TDD-First**: Tests drive development, not an afterthought
- **Safe Migration**: Manual template updates with clear guidance preserve project customizations
- **Systematic**: Structured workflows for debugging, refactoring, shipping
- **Quality-First**: Automated hooks prevent common issues
- **Learning-Focused**: Build skills while building products
- **Professional**: Clean commits, proper documentation, consistent standards
- **Safe Updates**: Two-file system enables template upgrades without data loss

## Requirements

- **Claude Code CLI** - See [installation guide](https://docs.anthropic.com/en/docs/claude-code)
- **Git repository** (for hooks and professional commits)
- **Python 3** (for web search validation hooks)

Ready to revolutionize your development process? **[Get started now](#quick-start)** ⚡

**New:** Check out the [Commands Reference](COMMANDS_REFERENCE.md) for quick command lookup and workflows!
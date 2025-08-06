---
allowed-tools: all
description: Manage template and project-specific instruction files
---
# Instruction File Management

**Usage:**
- `/claude-md backup` - Create timestamped backup of both instruction files
- `/claude-md update-mastery` - Update skill progression in PROJECT-SPECIFIC-CLAUDE.md
- `/claude-md create-project` - Create PROJECT-SPECIFIC-CLAUDE.md if missing
- `/claude-md merge-customizations` - Help migrate old CLAUDE.md customizations

**Examples:**
- `/claude-md backup` - Backup both CLAUDE.md and PROJECT-SPECIFIC-CLAUDE.md
- `/claude-md update-mastery` - Update your learning objectives and skill levels
- `/claude-md create-project` - Set up project-specific customization file

Manages the two-file instruction system: template instructions (CLAUDE.md) and project customizations (PROJECT-SPECIFIC-CLAUDE.md).

## Two-File System Overview

**CLAUDE.md** - Template instructions (updated with template versions)
- Core methodology and workflows
- Universal quality standards
- Command definitions and patterns
- Safe to update when template upgrades

**PROJECT-SPECIFIC-CLAUDE.md** - Your project customizations (preserved across updates)
- Language-specific quality rules
- Project structure definitions
- Team standards and practices  
- Learning objectives and skill progression

## Command Functions

### **`/claude-md backup`**
- Create timestamped backups of both instruction files
- Preserves working instruction sets before major changes
- Format: `CLAUDE.md.backup-YYYYMMDD-HHMMSS` and `PROJECT-SPECIFIC-CLAUDE.md.backup-YYYYMMDD-HHMMSS`
- Enables safe experimentation with new patterns and customizations

### **`/claude-md update-mastery`**
- Update the Technical Mastery Progression section in PROJECT-SPECIFIC-CLAUDE.md
- Track learning progress: novice → intermediate → advanced → expert
- Adjust current focus areas and learning objectives for your project
- Update skill levels across different technical domains

### **`/claude-md create-project`**
- Create PROJECT-SPECIFIC-CLAUDE.md if it doesn't exist
- Guided setup for project customizations:
  - Tech stack specific quality rules
  - Project directory structure patterns
  - Team development standards
  - Learning objectives and focus areas
- Provides template structure with examples to customize

### **`/claude-md merge-customizations`**
- Help migrate customizations from old single-file CLAUDE.md to the two-file system
- Extract project-specific sections from CLAUDE.md backup files
- Guide manual migration of:
  - Language-specific rules
  - Project structure definitions
  - Learning progression tracking
  - Team-specific standards

## Integration with Template Updates

**Safe Template Updates:**
- CLAUDE.md can be updated without losing project customizations
- PROJECT-SPECIFIC-CLAUDE.md is always preserved
- Backup system provides recovery options
- Clear separation prevents merge conflicts

**Migration Workflow:**
1. Template updates download new CLAUDE.md
2. PROJECT-SPECIFIC-CLAUDE.md remains untouched
3. Backup files available for reference
4. Manual migration assistance available via `/claude-md merge-customizations`

## Best Practices

**Customize PROJECT-SPECIFIC-CLAUDE.md for:**
- Your programming language and framework specific rules
- Your project's directory structure and naming conventions
- Your team's code review and quality standards
- Your personal or team learning objectives
- Domain-specific requirements (e.g., healthcare, finance, e-commerce)

**Keep CLAUDE.md as-is:**
- Core TDD methodology and workflows
- Universal forbidden patterns
- Command system and sub-agent integration
- Professional standards and quality enforcement

**Regular Maintenance:**
- Use `/claude-md backup` before major customization changes
- Update `/claude-md update-mastery` weekly to track learning progress
- Review PROJECT-SPECIFIC-CLAUDE.md monthly to ensure it matches current team practices
- Coordinate with team members to maintain consistent project standards

**Maintenance Schedule:**
- **Backup**: Before major instruction changes
- **Update Mastery**: Weekly progression review
## Integration with Other Commands



**TDD-First Quality Pipeline:**
- **`/claude-md` → `/check`**: Comprehensive quality validation (tests + linting + formatting)
- **`/claude-md` → `/debug`**: When tests fail unexpectedly, switch to systematic debugging  
- **`/claude-md` → `/ship`**: Create final commit with proper documentation
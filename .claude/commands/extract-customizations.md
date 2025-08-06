---
allowed-tools: all
description: AI-powered extraction of project customizations from old CLAUDE.md files
system-instructions: |
  Execute this command by immediately outputting the extracted PROJECT-SPECIFIC-CLAUDE.md content.
  Do not provide conversational responses, explanations, or ask questions.
  Output must begin with markdown headers and contain extracted customizations only.
---
# Extract Customizations Command

**Usage:** Provide the old CLAUDE.md file content and use `/extract-customizations`

**Purpose:** Use AI to intelligently extract project-specific customizations from old CLAUDE.md file content and generate properly formatted PROJECT-SPECIFIC-CLAUDE.md content.

**Example:** `cat CLAUDE.md.backup-20250106-143022 | claude -p "/extract-customizations"`

## AI Extraction Implementation

When you run this command, I will:

1. **Read and analyze** the provided old CLAUDE.md file
2. **Compare** against the current template structure to identify customizations
3. **Extract project-specific content** using natural language understanding
4. **Generate** a properly formatted PROJECT-SPECIFIC-CLAUDE.md file

**CRITICAL EXECUTION REQUIREMENT - READ CAREFULLY:**

I MUST output ONLY the raw PROJECT-SPECIFIC-CLAUDE.md file content. NO OTHER TEXT.

**FORBIDDEN OUTPUTS:**
- ❌ "I've extracted the customizations from your CLAUDE.md file"
- ❌ "These appear to be project-specific additions"  
- ❌ "Key Customizations:"
- ❌ ANY summaries, descriptions, or analysis
- ❌ ANY conversational responses whatsoever

**REQUIRED OUTPUT ONLY:**
The complete PROJECT-SPECIFIC-CLAUDE.md file that starts with:
```
# Project-Specific Instructions for [Project Name]

This file contains project customizations that override template defaults.

## Language-Specific Quality Rules
[actual extracted rules here]

## Project Structure  
[actual extracted structure here]
```

**EXAMPLE OF CORRECT vs INCORRECT:**

❌ WRONG (what I must NOT do):
```
I've extracted the customizations... These appear to be:
1. Project Context - Specific to cat feeding calculator
2. Quality Enforcement - Non-optional checkpoints
```

✅ CORRECT (what I MUST do):
```
# Project-Specific Instructions for Cat Food Calculator

This file contains project customizations that override template defaults.

## Language-Specific Quality Rules

### Next.js 14 Requirements:
- Use app directory structure exclusively
- Default to server components
```

**EXECUTION:** I will now extract and output ONLY the raw PROJECT-SPECIFIC-CLAUDE.md content:

## Critical Implementation Instructions

**CRITICAL:** When this command is executed, I MUST:

1. **READ** the provided old CLAUDE.md file completely
2. **ANALYZE** the content to identify project-specific customizations vs template content
3. **EXTRACT** the customizations and format them properly
4. **OUTPUT** the complete PROJECT-SPECIFIC-CLAUDE.md file content DIRECTLY

**I MUST NOT:**
- Ask questions or provide conversational responses
- Say "I understand you need to extract..." or similar phrases
- Describe what I will do instead of doing it
- Request clarification or offer options

**OUTPUT FORMAT REQUIREMENT:**
The output must be a complete, valid PROJECT-SPECIFIC-CLAUDE.md file that starts with the project customization content, properly formatted with markdown headers and sections.

## Command Functionality

This command performs AI-powered analysis to:

1. **Compare** old CLAUDE.md against current template
2. **Identify** project-specific customizations vs template content  
3. **Extract** customizations intelligently using natural language understanding
4. **Generate** properly formatted PROJECT-SPECIFIC-CLAUDE.md content
5. **Organize** content into appropriate sections with proper markdown structure

## AI Analysis Process

The command uses Claude Code's natural language understanding to:

### **Content Classification**
- **Template Content**: Standard workflow, universal patterns, command definitions
- **Project Customizations**: Language-specific rules, project structure, team standards, learning objectives

### **Smart Extraction Categories**
1. **Language-Specific Quality Rules**
   - Programming language preferences (TypeScript, Python, Rust, etc.)
   - Framework-specific patterns and best practices
   - Linting and formatting standards
   - Technology-specific forbidden patterns

2. **Project Structure Definitions**  
   - Directory layout and organization patterns
   - File naming conventions and standards
   - Module organization strategies
   - Test file placement and structure

3. **Development Workflow Customizations**
   - Testing strategies and coverage requirements
   - Code review standards and checklists
   - Deployment and release processes
   - Quality gates and validation steps

4. **Team Standards & Practices**
   - Communication protocols and standards
   - Documentation requirements
   - Development environment setup
   - Collaboration workflows

5. **Technical Mastery Progression**
   - Current learning objectives and focus areas
   - Skill level tracking and progression goals
   - Knowledge gaps and learning methods
   - Success criteria and evaluation metrics

6. **Domain-Specific Rules**
   - Industry compliance requirements (HIPAA, PCI DSS, etc.)
   - Security standards and practices
   - Performance requirements and benchmarks
   - Business logic constraints

### **Content Mapping Strategy**

The AI maps extracted content to PROJECT-SPECIFIC-CLAUDE.md sections:

```markdown
Old CLAUDE.md customizations → PROJECT-SPECIFIC-CLAUDE.md sections

"TypeScript strict mode required" → Language-Specific Quality Rules
"src/ directory structure" → Project Structure  
"Weekly learning goals" → Technical Mastery Progression
"Code review checklist" → Team Standards & Practices
"HIPAA compliance rules" → Domain-Specific Rules
```

### **Quality Assurance**

The extraction process includes:

- **Content Validation**: Ensures extracted content is coherent and properly formatted
- **Section Organization**: Groups related customizations logically
- **Markdown Formatting**: Maintains proper structure, code blocks, and lists
- **Context Preservation**: Retains original intent and meaning
- **Template Compliance**: Ensures output matches PROJECT-SPECIFIC-CLAUDE.md structure

## Usage Scenarios

### **Template Updates**
```bash
# When setup.sh detects customizations
/extract-customizations CLAUDE.md.backup-20250106-143022
```

### **Manual Migration**
```bash  
# For existing projects wanting to adopt two-file system
/extract-customizations CLAUDE.md
```

### **Recovery Scenarios**
```bash
# Restore customizations from backup
/extract-customizations claude-backup-20250106-143022/CLAUDE.md
```

## Output Format

The command generates PROJECT-SPECIFIC-CLAUDE.md content with:

1. **Complete Section Structure**: All standard sections with extracted content
2. **Proper Markdown Formatting**: Headers, code blocks, lists, emphasis
3. **Contextual Examples**: Relevant examples based on detected technology stack
4. **Integration Instructions**: How the customizations integrate with template
5. **Placeholder Removal**: Eliminates template examples, adds real project content

## Error Handling

**Safe Fallback Strategy:**
- If AI extraction fails, provides manual migration guidance
- Always preserves original backup files
- Offers partial extraction with user review
- Provides clear error messages and recovery options

**Content Validation:**
- Verifies markdown structure integrity  
- Ensures no critical content is lost during extraction
- Validates section mapping accuracy
- Confirms output compatibility with template system

## Integration with Setup Process

This command integrates seamlessly with the template update workflow:

1. **Automatic Detection**: setup.sh detects old customizations
2. **AI Extraction**: Offers AI-powered migration as primary option
3. **User Preview**: Shows extracted content before applying
4. **Confirmation**: User approves migration before final application
5. **Validation**: Verifies successful migration and backup preservation

## Best Practices

**Before Extraction:**
- Ensure you have a clean backup of your old CLAUDE.md
- Review your current project-specific needs
- Understand the two-file system benefits

**During Extraction:**
- Review the AI-generated content carefully
- Verify that your specific customizations are captured
- Check that content is placed in appropriate sections

**After Extraction:**  
- Test that Claude Code reads both files correctly
- Validate that your project-specific rules are working
- Update any content that needs refinement

**Manual Refinement:**
- The AI extraction provides an excellent starting point
- Feel free to refine and customize the generated content
- Add any project-specific details that weren't in the original file
- Remove or modify sections that don't apply to your project

This command transforms the complex task of customization migration into a simple, AI-assisted process that preserves your project's unique requirements while adopting the template's latest features.
---
allowed-tools: all
description: Large codebase analysis using Gemini CLI with massive context window
---

# Gemini CLI Integration for Large Codebase Analysis

**Usage:**
- `/gemini <analysis_request>` - Comprehensive analysis with user confirmation
- `/gemini quick <request>` - Skip confirmation for this session  
- `/gemini files <files>` - Analyze specific files
- `/gemini dir <directory>` - Analyze specific directory
- `/gemini all` - Analyze entire codebase

**Examples:**
- `/gemini "analyze the authentication system architecture"`
- `/gemini quick "check for security vulnerabilities"`
- `/gemini files "src/auth.js src/middleware/auth.js"`
- `/gemini dir "src/components/"`
- `/gemini all "provide comprehensive codebase overview"`

## When to Use Gemini CLI

Use `/gemini` when Claude Code's context window is insufficient:

- **Analyzing entire codebases** or large directories
- **Comparing multiple large files** that exceed context limits
- **Understanding project-wide patterns** or architecture
- **Current context window is insufficient** for the task
- **Working with files totaling more than 100KB**
- **Verifying if specific features, patterns, or security measures** are implemented
- **Checking for the presence of certain coding patterns** across the entire codebase

## Command Variants

### `/gemini <analysis_request>` - Standard Analysis (RECOMMENDED)
**Comprehensive analysis with user confirmation workflow.**

**AI Behavior:**
- Presents analysis plan with Gemini command details
- Requests user confirmation following CLAUDE-GEMINI.md protocol
- Executes Gemini CLI with appropriate @ syntax
- Processes and summarizes results for actionable insights
- Handles rate limiting and error scenarios gracefully

**Example Flow:**
```
You: /gemini "analyze the payment processing system for security issues"
AI: "I need to use Gemini CLI for comprehensive analysis of your payment system.

     Why using Gemini:
     - Payment system spans multiple directories and files
     - Need to analyze security patterns across entire codebase
     - Context requirements exceed Claude Code's limits
     
     Command I'll run:
     gemini -p \"@src/payments/ @src/middleware/auth.js @tests/payments/ Analyze the payment processing system for security vulnerabilities, proper error handling, and compliance with payment security standards\"
     
     Options:
     1. Run the Gemini command
     2. Run the Gemini command, and don't ask again in this session
     3. Don't run the Gemini command, and tell me what to do differently"
```

### `/gemini quick <request>` - No Confirmation Mode
**Skip confirmation workflow for rapid analysis cycles.**

**AI Behavior:**
- Immediately executes Gemini CLI without confirmation prompts
- Uses session context to determine optimal file/directory inclusion
- Ideal for iterative analysis and follow-up questions
- Still provides clear reasoning for command choices

### `/gemini files <files>` - Specific File Analysis
**Analyze specific files with targeted focus.**

**Usage Patterns:**
- `/gemini files "src/main.js src/utils.js" "compare implementation patterns"`
- `/gemini files "*.test.js" "analyze test coverage and quality"`
- `/gemini files "@src/auth/" "security audit of authentication"`

### `/gemini dir <directory>` - Directory-Focused Analysis
**Analyze entire directories with context awareness.**

**Usage Patterns:**
- `/gemini dir src/ "architectural overview"`
- `/gemini dir tests/ "test strategy analysis"`
- `/gemini dir docs/ "documentation completeness review"`

### `/gemini all` - Complete Codebase Analysis
**Comprehensive analysis of the entire project.**

**AI Behavior:**
- Uses `--all_files` flag for maximum context inclusion
- Provides structured analysis covering architecture, patterns, quality, and recommendations
- Handles large output and potential rate limiting gracefully
- Summarizes findings into actionable categories

## Integration with Development Workflow

### **Pre-Development Analysis:**
- **`/gemini` → `/plan`**: Use Gemini insights to create detailed implementation roadmaps
- **`/gemini` → `/dev`**: Start TDD with comprehensive understanding of existing patterns

### **Quality Assurance Integration:**
- **`/gemini` → `/check`**: Identify quality issues before running local checks
- **`/gemini` → `/refactor`**: Use codebase insights to guide systematic improvements

### **Debugging and Investigation:**
- **`/gemini` → `/debug`**: Understand system-wide implications of bugs
- **`/debug` → `/gemini`**: Get broader context when local debugging hits limits

## Professional Output Standards

**Analysis Structure:**
1. **Executive Summary**: Key findings and recommendations
2. **Architecture Overview**: System design and component relationships  
3. **Quality Assessment**: Code quality, patterns, and potential issues
4. **Security Review**: Security practices and vulnerabilities
5. **Performance Insights**: Performance patterns and optimization opportunities
6. **Actionable Recommendations**: Specific next steps prioritized by impact

**Error Handling:**
- **Rate Limiting**: Graceful handling with retry suggestions and timing guidance
- **API Failures**: Clear error reporting with fallback analysis strategies
- **Context Overflows**: Automatic chunking strategies for massive codebases
- **Network Issues**: Timeout handling and offline continuation options

## Advanced Usage Patterns

### **Multi-Phase Analysis:**
```bash
# Phase 1: Architecture Understanding
/gemini dir src/ "analyze system architecture and component dependencies"

# Phase 2: Security Assessment  
/gemini files "@src/ @middleware/ @auth/" "comprehensive security audit"

# Phase 3: Performance Review
/gemini files "@src/ @lib/" "identify performance bottlenecks and optimization opportunities"
```

### **Comparison Analysis:**
```bash
# Compare implementations
/gemini files "old-auth.js new-auth.js" "compare authentication implementations"

# Feature implementation verification
/gemini all "is dark mode fully implemented across the application?"
```

### **Pattern Detection:**
```bash
# Anti-pattern identification
/gemini all "identify code smells, anti-patterns, and architectural issues"

# Best practice verification
/gemini dir src/ "verify adherence to React/Node.js best practices"
```

## Session Context Management

**Confirmation State Tracking:**
- Option 2 ("don't ask again") persists for the current Claude Code session
- Automatic confirmation expires when starting new sessions
- Manual override available with `/gemini quick` for single-use skipping

**Analysis History:**
- Recent Gemini analyses inform follow-up questions
- Context-aware suggestions for related analysis areas
- Integration with todo lists for systematic codebase exploration

## Best Practices

**Effective Prompts:**
- Be specific about what you're looking for
- Include context about your goals and constraints
- Specify output format preferences (architecture diagrams, code examples, checklists)

**Resource Management:**
- Use targeted analysis (files/dir) when possible to conserve API quota
- Batch related questions to minimize separate API calls
- Monitor rate limiting and plan analysis sessions accordingly

**Quality Integration:**
- Follow Gemini analysis with `/check` to validate findings
- Use insights to improve local development patterns
- Document architectural decisions revealed through analysis

## Command Evolution

**Future Enhancements:**
- Integration with project-specific analysis templates
- Automated report generation for common analysis patterns
- Integration with documentation generation workflows
- Custom analysis profiles for different project types

---

**Remember**: Gemini CLI is your tool for understanding codebases that exceed normal analysis limits. Use it strategically to gain comprehensive insights that inform better development decisions and maintain high-quality code standards.

The `/gemini` command makes large-scale codebase analysis systematic and professional.
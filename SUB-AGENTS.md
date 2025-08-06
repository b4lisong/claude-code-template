# Sub-Agents Guide: Specialized AI for Complex Development Tasks

This Claude Code template includes four specialized sub-agents designed to handle complex, multi-step development tasks while maintaining the template's core values: TDD-first development, zero-tolerance quality standards, and systematic learning approaches.

## What Are Sub-Agents?

Sub-agents are specialized AI assistants that:
- Operate in separate context windows
- Have customized system prompts for specific domains
- Can be configured with specific tool access
- Proactively delegate tasks based on expertise
- Coordinate with the main conversation and other agents

**Access via:** `/agents` command to open sub-agent management interface

## Template Sub-Agents Overview

### 🧪 **TDD-Coach Agent**
**Purpose:** Specialized test-driven development coach  
**Expertise:** RED→GREEN→REFACTOR cycle, systematic TDD thinking  
**Use When:** Complex test design, TDD workflow guidance, building testing skills  

### 🔍 **Quality-Enforcer Agent** 
**Purpose:** Zero-tolerance quality verification and issue resolution  
**Expertise:** Parallel issue fixing, comprehensive quality checks  
**Use When:** Quality issues need immediate resolution, pre-commit verification  

### 📋 **Strategic-Planner Agent**
**Purpose:** Comprehensive project planning and roadmap generation  
**Expertise:** 5-phase planning methodology, systematic analysis  
**Use When:** Complex project planning, architectural decisions, roadmap creation  

### ♻️ **Refactoring-Specialist Agent**
**Purpose:** Safe, systematic code improvement  
**Expertise:** Test-covered refactoring, incremental improvements  
**Use When:** Code quality improvements, architectural refactoring, technical debt reduction  

---

## Detailed Agent Capabilities

## 🧪 TDD-Coach Agent

### **Core Mission**
Ensures ALL development follows the TDD cycle while building systematic, senior-level TDD thinking skills.

### **Key Responsibilities**
- **RED Phase:** Write comprehensive failing tests that define exact behavior
- **GREEN Phase:** Guide minimal implementation to pass tests  
- **REFACTOR Phase:** Improve code quality with test safety net
- **Learning:** Explain the "why" behind every TDD decision

### **When to Use**
```bash
# Complex feature with multiple test scenarios
"Use the TDD-Coach agent to design comprehensive tests for this authentication system"

# When TDD workflow is unclear
"TDD-Coach agent: guide me through testing this payment processing module"

# Building TDD skills
"TDD-Coach agent: explain why we write tests first for this user management feature"
```

### **Quality Standards Enforced**
- Implementation never before tests
- Tests define behavior, not implementation details
- Comprehensive coverage of happy path, edge cases, errors
- Clear, readable tests that serve as documentation

### **Integration Points**
- **With `/dev`:** Handles complex test design and TDD workflow
- **With main conversation:** Reports TDD insights and decisions
- **With other agents:** Ensures refactoring maintains test coverage

---

## 🔍 Quality-Enforcer Agent

### **Core Mission**
Zero tolerance for quality issues - fixes every problem immediately, never just reports them.

### **Key Responsibilities**
- **Comprehensive Detection:** Run all appropriate linters, tests, builds
- **Immediate Resolution:** Fix every issue found, spawn parallel agents as needed
- **Continuous Verification:** Re-run checks until everything shows GREEN
- **Parallel Processing:** Handle multiple issue types simultaneously

### **When to Use**
```bash
# When /check finds multiple issues
"Quality-Enforcer agent: fix all these linting and test issues immediately"

# Pre-commit quality gates
"Quality-Enforcer agent: ensure everything passes before commit"

# Parallel issue resolution
"Spawn Quality-Enforcer to handle these 15 ESLint errors while I work on features"
```

### **Quality Standards Enforced**
- ALL forbidden patterns eliminated (no emojis, no Claude attribution)
- Zero linting warnings across all languages
- All tests passing consistently
- Proper error handling for target languages
- Professional code standards maintained

### **Integration Points**
- **With `/check`:** Immediately resolves all detected issues
- **With `/ship`:** Final quality gate before commits
- **With other agents:** Ensures all agent output meets quality standards

---

## 📋 Strategic-Planner Agent

### **Core Mission**
Transform complex initiatives into systematic, actionable implementation roadmaps using a comprehensive 5-phase methodology.

### **Key Responsibilities**
- **Discovery & Analysis:** Understand current state and requirements
- **Solution Design:** Create comprehensive technical approach
- **Phase Planning:** Break into actionable phases with clear deliverables
- **Implementation Roadmap:** Detailed execution guidance with quality gates
- **Resource Planning:** Realistic timelines and resource allocation

### **When to Use**
```bash
# Complex project planning
"Strategic-Planner agent: create comprehensive roadmap for microservices migration"

# Architecture decisions
"Strategic-Planner agent: plan approach for adding real-time features to this system"

# Large feature planning
"Strategic-Planner agent: break down this e-commerce checkout system implementation"
```

### **Planning Methodology**
1. **Phase 1:** Discovery & Analysis → Current state assessment
2. **Phase 2:** Solution Design → Technical architecture and specifications  
3. **Phase 3:** Phase Planning → Actionable phases with dependencies
4. **Phase 4:** Implementation Roadmap → Detailed execution guidance
5. **Phase 5:** Resource & Timeline Planning → Realistic scheduling

### **Integration Points**
- **With `/plan`:** Provides comprehensive analysis and roadmaps
- **With TDD-Coach:** Includes test strategy in all planning
- **With Quality-Enforcer:** Builds quality gates into every phase

---

## ♻️ Refactoring-Specialist Agent

### **Core Mission**
Systematically improve code quality while maintaining absolute safety through comprehensive test coverage and incremental changes.

### **Key Responsibilities**
- **Safety Assessment:** Verify test coverage before ANY refactoring
- **Incremental Improvement:** Apply changes step-by-step with continuous validation
- **Quality Enhancement:** Improve readability, maintainability, performance
- **Behavior Preservation:** Ensure identical functionality throughout process

### **When to Use**
```bash
# Code improvement with safety
"Refactoring-Specialist agent: safely improve this payment processing module"

# Architecture refactoring
"Refactoring-Specialist agent: extract services from this monolithic controller"

# Technical debt reduction
"Refactoring-Specialist agent: systematically improve code quality in user module"
```

### **Safety Protocols**
1. **Phase 1:** Safety Assessment - verify comprehensive test coverage
2. **Phase 2:** Incremental Changes - one improvement at a time with test verification  
3. **Phase 3:** Quality Validation - ensure improvements achieved

### **Integration Points**
- **With `/refactor`:** Provides safe, systematic code improvement
- **With TDD-Coach:** Ensures refactoring maintains TDD principles
- **With Quality-Enforcer:** All refactored code meets quality standards

---

## Multi-Agent Coordination Patterns

### **Development Workflow Enhancement**
```bash
# Start complex feature development
/agents
# Delegate to TDD-Coach for comprehensive test design
# Use Quality-Enforcer for continuous quality maintenance
# Strategic-Planner for architectural decisions
/dev "enterprise authentication system"
/check  # Quality-Enforcer ensures everything passes
/ship "add enterprise auth with SSO support"
```

### **Quality-First Development**
```bash
# Parallel quality and development
/agents
# TDD-Coach designs tests
# Quality-Enforcer maintains standards
# Development proceeds with dual safety nets
```

### **Strategic Refactoring**
```bash
# Complex refactoring project  
/agents
# Strategic-Planner creates refactoring roadmap
# Refactoring-Specialist executes safely
# Quality-Enforcer ensures standards maintained
# TDD-Coach maintains test coverage
```

## Best Practices for Sub-Agent Usage

### **When to Delegate to Sub-Agents**
- **Complex Tasks:** Multi-step processes requiring specialized expertise
- **Parallel Processing:** Multiple independent tasks that can run simultaneously
- **Specialized Knowledge:** Domain-specific requirements (TDD, quality, planning, refactoring)
- **Quality Assurance:** Tasks requiring zero-tolerance standards
- **Learning Opportunities:** Situations where specialized coaching adds value

### **Coordination Strategies**
- **Clear Task Boundaries:** Define specific responsibilities for each agent
- **Communication Protocols:** Ensure agents report back key insights
- **Quality Consistency:** All agents must maintain template quality standards
- **Learning Integration:** Use agent interactions as learning opportunities

### **Agent Selection Guide**
- **Need tests designed?** → TDD-Coach Agent
- **Have quality issues?** → Quality-Enforcer Agent  
- **Complex planning required?** → Strategic-Planner Agent
- **Code needs improvement?** → Refactoring-Specialist Agent
- **Multiple needs?** → Coordinate multiple agents

## Sub-Agent Quality Standards

All sub-agents enforce the template's core quality requirements:

### **Universal Standards**
- NO emojis in any output or generated content
- NO Claude attribution in commits or documentation
- Follow all forbidden patterns from CLAUDE.md
- Maintain professional output suitable for production
- Support the template's learning-focused approach

### **Agent-Specific Excellence**
- **TDD-Coach:** Builds systematic TDD thinking skills
- **Quality-Enforcer:** Achieves zero-tolerance quality standards
- **Strategic-Planner:** Creates actionable, realistic roadmaps
- **Refactoring-Specialist:** Ensures behavior preservation during improvement

## Getting Started with Sub-Agents

### **Step 1: Access Sub-Agents**
```bash
/agents  # Opens sub-agent management interface
```

### **Step 2: Understand Available Agents**
Review the four template agents and their specializations:
- TDD-Coach for test-driven development
- Quality-Enforcer for issue resolution  
- Strategic-Planner for comprehensive planning
- Refactoring-Specialist for safe code improvement

### **Step 3: Strategic Delegation**
Choose agents based on task complexity and domain requirements:
- Simple tasks → Main conversation
- Complex specialized tasks → Appropriate sub-agent
- Multi-faceted problems → Coordinate multiple agents

### **Step 4: Monitor and Learn**
- Pay attention to agent reasoning and decisions
- Use agent interactions as learning opportunities
- Build understanding of when to delegate vs. handle directly

## Advanced Usage Patterns

### **Multi-Agent Project Workflow**
```bash
# Phase 1: Strategic Planning
Strategic-Planner agent: "Create comprehensive roadmap for user management system"

# Phase 2: TDD Implementation  
TDD-Coach agent: "Design tests for user registration, authentication, and profile management"

# Phase 3: Quality Assurance
Quality-Enforcer agent: "Ensure all code meets production standards"

# Phase 4: Code Improvement
Refactoring-Specialist agent: "Optimize user service architecture"
```

### **Continuous Quality Development**
```bash
# Ongoing quality partnership
Quality-Enforcer agent: "Monitor and fix issues as they arise"
TDD-Coach agent: "Maintain test-first approach throughout development"
# Main conversation handles feature logic with specialist support
```

### **Learning-Accelerated Development**
```bash
# Use agents as teachers
TDD-Coach agent: "Explain TDD decisions while implementing authentication"
Refactoring-Specialist agent: "Show me refactoring patterns while improving code quality"
Strategic-Planner agent: "Teach planning methodology while creating roadmaps"
```

---

## Conclusion

The template's sub-agents transform individual development into coordinated team development, with each agent bringing specialized expertise while maintaining the template's core values:

- **TDD-first philosophy** preserved and enhanced
- **Quality standards** enforced across all agents
- **Professional output** maintained in all interactions
- **Learning opportunities** multiplied through specialized coaching
- **Systematic approaches** applied to complex problems

Use sub-agents strategically to handle complexity while building your own systematic thinking skills. The goal is not dependency on AI agents, but leveraging them to become a better, more systematic developer yourself.

**Remember:** Sub-agents are tools to enhance your capabilities and accelerate your learning, not replace your thinking. Use them wisely to build senior-level development skills while maintaining the template's commitment to quality and systematic approaches.
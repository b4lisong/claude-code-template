# Sub-Agents Guide: Specialized Research AI for Complex Development Analysis

This Claude Code template includes five specialized research sub-agents designed to analyze complex development challenges and create comprehensive plans while maintaining the template's core values: research-first approach, evidence-based recommendations, and systematic analysis methodologies.

## What Are Research Sub-Agents?

Research sub-agents are specialized AI assistants that:
- **Analyze and research** rather than implement directly
- **Create comprehensive plans** saved to `/plans` directory for human execution
- **Operate in separate context windows** with specialized research prompts
- **Focus on evidence-based recommendations** backed by thorough analysis
- **Coordinate research efforts** across multiple domains and expertise areas

**IMPORTANT: All sub-agents are RESEARCHERS, not implementers.** They create detailed research plans that you review and execute.

**Access via:** `/agents` command to open sub-agent management interface

## Template Research Sub-Agents Overview

### 🧪 **TDD Research Specialist Agent**
**Purpose:** Comprehensive testing strategy research and TDD planning  
**Research Focus:** Testing patterns, TDD methodologies, quality assurance strategies  
**Creates Plans For:** Testing strategies, TDD implementation approaches, quality gate design  

### 🔍 **Quality Research Analyst Agent** 
**Purpose:** Thorough quality assessment and improvement planning  
**Research Focus:** Code quality analysis, technical debt assessment, improvement strategies  
**Creates Plans For:** Quality improvement roadmaps, issue remediation strategies, quality metrics  

### 📋 **Strategic Research Architect Agent**
**Purpose:** Comprehensive strategic analysis and roadmap development  
**Research Focus:** System architecture, strategic planning, organizational change  
**Creates Plans For:** Strategic initiatives, architectural decisions, organizational roadmaps  

### ♻️ **Code Analysis Researcher Agent**
**Purpose:** Systematic code analysis and refactoring planning  
**Research Focus:** Code quality assessment, refactoring opportunities, technical debt analysis  
**Creates Plans For:** Code improvement strategies, refactoring roadmaps, technical debt reduction  

### 📚 **Documentation Research Specialist Agent**
**Purpose:** External documentation research and context consolidation specialist  
**Research Focus:** Third-party libraries, APIs, integration patterns, external service documentation  
**Creates Plans For:** Integration strategies, API reference guides, documentation summaries, implementation patterns  

---

## Research Workflow Integration

### Research-First Development Process

1. **Problem Identification** - Identify complex challenges requiring specialized research
2. **Agent Assignment** - Delegate research to appropriate specialized agent
3. **Comprehensive Analysis** - Agent conducts thorough research and analysis
4. **Plan Creation** - Agent creates detailed implementation plan with evidence-based recommendations
5. **Plan Review** - Human reviews research findings and proposed approach
6. **Implementation Execution** - Human or main Claude implements based on research plan

### Plan Storage and Organization

All research plans are stored in organized `/plans` directory structure:

```
/plans/
├── tdd-research/           # TDD Research Specialist plans
├── quality-analysis/       # Quality Research Analyst plans  
├── strategic-research/     # Strategic Research Architect plans
├── refactoring-analysis/   # Code Analysis Researcher plans
├── documentation-research/ # Documentation Research Specialist plans
└── templates/             # Plan templates for consistency
```

**Naming Convention:** `{agent-type}-{description}-{YYYY-MM-DD}.md`

---

## Detailed Agent Research Capabilities

## 🧪 TDD Research Specialist Agent

### **Research Mission**
Analyzes codebases and creates comprehensive TDD strategies and testing plans through systematic research.

### **Research Specializations**
- **Testing Strategy Analysis:** Research optimal testing approaches for specific domains and technologies
- **TDD Pattern Investigation:** Study TDD methodologies and their application to complex features  
- **Test Architecture Research:** Design comprehensive testing strategies and organization approaches
- **Quality Gate Planning:** Research validation approaches and success criteria for TDD initiatives

### **Research Outputs**
- Comprehensive testing strategy plans with evidence-based recommendations
- TDD implementation roadmaps with phase-by-phase guidance
- Test coverage analysis and improvement strategies
- Testing tool evaluation and selection criteria

### **When to Use**
- Complex feature development requiring comprehensive testing strategy
- Legacy system testing improvement initiatives
- TDD adoption planning and organizational change
- Testing architecture design for new systems

### **Example Research Tasks**
- "Research optimal TDD approach for authentication system development"
- "Analyze current test coverage and create improvement strategy"
- "Investigate testing patterns for microservices architecture"

---

## 🔍 Quality Research Analyst Agent

### **Research Mission**
Conducts thorough quality assessments and creates detailed remediation plans for systematic code improvement.

### **Research Specializations**
- **Code Quality Analysis:** Systematic assessment using static analysis tools and manual inspection
- **Technical Debt Research:** Quantification and prioritization of improvement opportunities
- **Quality Metrics Investigation:** Research appropriate quality measurements and benchmarks
- **Improvement Strategy Planning:** Evidence-based approaches to quality enhancement

### **Research Outputs**
- Comprehensive quality assessment reports with detailed findings
- Prioritized improvement roadmaps with effort and impact analysis
- Quality metrics and measurement strategies
- Tool configuration and automation recommendations

### **When to Use**
- Pre-commit quality assessment and improvement planning
- Technical debt analysis and reduction strategy development
- Quality process improvement and automation planning
- Code review and quality gate enhancement initiatives

### **Example Research Tasks**
- "Analyze code quality issues and create comprehensive improvement plan"
- "Research quality metrics and measurement approaches for this codebase"
- "Investigate automated quality checking strategies and tool configuration"

---

## 📋 Strategic Research Architect Agent

### **Research Mission**
Conducts comprehensive strategic analysis and creates detailed roadmaps for complex initiatives and architectural decisions.

### **Research Specializations**
- **Architectural Analysis:** Research current system architecture and improvement opportunities
- **Strategic Planning:** Comprehensive analysis using systematic 5-phase research methodology
- **Technology Research:** Investigation of solution approaches and technology options
- **Organizational Strategy:** Research change management and adoption strategies

### **Research Outputs**
- Comprehensive strategic analysis reports with multiple solution options
- Detailed implementation roadmaps with phase-by-phase execution plans
- Risk assessment and mitigation strategies based on research findings
- Resource planning and organizational readiness assessments

### **When to Use**
- Complex architectural decisions requiring comprehensive analysis
- Large-scale system migration or modernization planning
- Strategic technology adoption and organizational change initiatives
- Multi-team coordination and project planning requirements

### **Example Research Tasks**
- "Research microservices migration strategy and create comprehensive roadmap"
- "Analyze system architecture and investigate performance improvement approaches"
- "Research API modernization strategies and organizational impact assessment"

---

## ♻️ Code Analysis Researcher Agent

### **Research Mission**
Systematically analyzes code quality and creates comprehensive refactoring plans with detailed safety assessments.

### **Research Specializations**
- **Code Quality Analysis:** Systematic identification of improvement opportunities and anti-patterns
- **Refactoring Strategy Research:** Investigation of safe, incremental improvement approaches
- **Technical Debt Assessment:** Quantification and prioritization of code improvement opportunities
- **Safety Assessment Planning:** Research test coverage requirements and validation strategies

### **Research Outputs**
- Comprehensive code analysis reports with detailed improvement opportunities
- Systematic refactoring plans with phase-by-phase safety considerations
- Technical debt quantification and prioritization matrices
- Safety assessment and validation strategies for code improvements

### **When to Use**
- Code quality improvement initiatives requiring systematic analysis
- Legacy code modernization and refactoring planning
- Technical debt reduction strategy development
- Architecture improvement and code organization initiatives

### **Example Research Tasks**
- "Analyze authentication module code quality and create refactoring plan"
- "Research technical debt in payment processing system and prioritize improvements"
- "Investigate code organization opportunities and create systematic improvement strategy"

---

## 📚 Documentation Research Specialist Agent

### **Research Mission**
Conducts comprehensive research on external documentation sources and creates consolidated reference materials for third-party integrations.

### **Research Specializations**
- **External Documentation Analysis:** Research GitHub repositories, API specs, and official documentation
- **Integration Pattern Investigation:** Study third-party library usage patterns and community best practices
- **Security and Compliance Research:** Investigate security considerations and compliance requirements for external dependencies
- **Context Consolidation Planning:** Create comprehensive reference documents from multiple authoritative sources

### **Research Outputs**
- Comprehensive integration strategy plans with evidence-based recommendations
- API reference consolidations with key endpoints and implementation patterns
- Security and compliance analysis for external dependencies
- Version compatibility matrices and upgrade planning guides

### **When to Use**
- Third-party library integration planning and research
- API integration strategy development and documentation consolidation
- External service integration analysis and security assessment
- Documentation research for complex integrations requiring multiple sources

### **Example Research Tasks**
- "Research Stripe API integration patterns and create comprehensive implementation guide"
- "Analyze React Router v6 documentation and create migration strategy from v5"
- "Research AWS SDK security best practices and create integration compliance plan"

---

## Advanced Research Coordination Patterns

### **Multi-Agent Research Collaboration**

For complex initiatives requiring multiple research perspectives:

1. **Strategic Research Architect** - Provides high-level strategic analysis and roadmap
2. **Documentation Research Specialist** - Researches external dependencies and integration requirements
3. **TDD Research Specialist** - Develops testing strategy aligned with strategic goals and external integrations
4. **Quality Research Analyst** - Assesses quality requirements and improvement needs
5. **Code Analysis Researcher** - Analyzes implementation challenges and technical constraints

### **Research Workflow Examples**

#### **Example: Microservices Migration Research**
1. **Strategic Research Architect**: Analyze migration strategy, technology options, organizational impact
2. **Documentation Research Specialist**: Research microservices frameworks, container orchestration, and API gateway documentation
3. **Code Analysis Researcher**: Assess current codebase and identify refactoring requirements  
4. **TDD Research Specialist**: Design testing strategy for microservices architecture
5. **Quality Research Analyst**: Research quality gates and validation approaches

#### **Example: Third-Party API Integration Research**
1. **Documentation Research Specialist**: Comprehensive API documentation analysis and integration pattern research
2. **Strategic Research Architect**: Integration architecture strategy and organizational impact assessment
3. **Quality Research Analyst**: API integration quality standards and monitoring strategy
4. **TDD Research Specialist**: API testing strategy and mock service planning

#### **Example: Legacy System Modernization Research**
1. **Code Analysis Researcher**: Comprehensive legacy code analysis and improvement opportunities
2. **Strategic Research Architect**: Modernization roadmap with risk assessment and phasing
3. **Documentation Research Specialist**: Research modern technology stack documentation and migration patterns
4. **Quality Research Analyst**: Quality improvement strategy aligned with modernization goals
5. **TDD Research Specialist**: Testing strategy for legacy system improvement and validation

---

## Research Quality Standards

### **All Research Plans Must Include:**
- **Executive Summary** - High-level findings and key recommendations
- **Research Methodology** - How analysis was conducted and information sources
- **Current State Analysis** - Comprehensive assessment of existing situation
- **Evidence-Based Recommendations** - Specific suggestions backed by research findings
- **Implementation Guidance** - Clear, actionable steps for human execution
- **Success Criteria** - Measurable outcomes and validation approaches
- **Risk Assessment** - Potential challenges and mitigation strategies

### **Professional Standards:**
- **NO emojis** in any research output or plans
- **NO Claude attribution** in research documentation  
- **Professional tone** suitable for technical and executive stakeholder consumption
- **Evidence-based approach** with clear rationale for all recommendations
- **Comprehensive coverage** ensuring no critical aspects are overlooked

---

## Integration with Development Workflow

### **Research-Driven Development Process**

1. **Challenge Identification** - Recognize complex problems requiring specialized research
2. **Research Agent Assignment** - Delegate to appropriate specialized research agent
3. **Comprehensive Analysis** - Agent conducts thorough investigation and analysis
4. **Plan Creation and Documentation** - Evidence-based implementation plan with detailed guidance
5. **Plan Review and Validation** - Human review of research findings and recommendations
6. **Implementation Execution** - Human or main Claude implements based on research plan
7. **Results Validation** - Verify outcomes match research predictions and success criteria

### **Benefits of Research-First Approach**

- **Better Decision Making** - Comprehensive analysis before implementation
- **Risk Mitigation** - Issues identified and addressed during research phase
- **Knowledge Preservation** - All analysis and reasoning documented for future reference
- **Team Collaboration** - Plans can be reviewed, shared, and improved by multiple team members
- **Quality Assurance** - Evidence-based approach ensures well-founded implementation decisions

---

Remember: These research sub-agents are your specialized analytical partners. They don't implement solutions - they conduct thorough research, analyze complex challenges, and create comprehensive plans that enable you to make informed decisions and execute with confidence.
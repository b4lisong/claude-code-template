# Project-Specific Instructions

This file contains project-specific customizations for your Claude Code development workflow. These instructions are preserved when the template updates, allowing safe upgrades while maintaining your team's specific requirements.

**How this works:** Claude Code reads both `CLAUDE.md` (template instructions) and this file together. Your project-specific rules override template defaults where applicable.

## Language-Specific Quality Rules

### Your Tech Stack Rules
Add specific quality rules for your programming languages and frameworks:

```markdown
**Example for Node.js/TypeScript projects:**
- No `any` types - use specific types or `unknown`
- Prefer `const` over `let`, never use `var`
- Use strict TypeScript configuration
- No `@ts-ignore` without detailed explanation
- Async functions must handle all error cases

**Example for Python projects:**
- Use type hints for all function signatures
- No bare `except:` clauses - specify exception types
- Follow PEP 8 formatting standards
- Use `pathlib` instead of `os.path`
- Prefer f-strings over `.format()` or `%` formatting

**Example for Rust projects:**
- Never use `unwrap()` or `expect()` in production code
- Use `Result<T, E>` for error handling
- Prefer `?` operator over explicit match
- Use `clippy::pedantic` lints
- Document all public APIs with examples
```

Replace the examples above with rules specific to your project's tech stack.

## Project Structure

Define your project's directory layout and organization patterns:

```markdown
**Example structure:**
src/
├── api/           # REST API endpoints and handlers
├── services/      # Business logic services
├── models/        # Data models and types
├── utils/         # Utility functions and helpers
├── config/        # Configuration management
└── tests/         # Test files organized by module

**File naming conventions:**
- Use kebab-case for directories: `user-service/`
- Use camelCase for TypeScript files: `userService.ts`
- Test files: `userService.test.ts`
- Types: `userTypes.ts`
```

Customize this section to match your project's structure.

## Development Workflow Customizations

### Research-First Development Process
**IMPORTANT: All sub-agents are researchers who create plans, not implementers:**

```markdown
**Sub-Agent Research Workflow:**
- **TDD Research Specialist**: Creates comprehensive testing strategies and plans
- **Quality Research Analyst**: Analyzes code quality and creates improvement plans  
- **Strategic Research Architect**: Develops strategic roadmaps and architectural plans
- **Code Analysis Researcher**: Analyzes code issues and creates refactoring plans
- **Documentation Research Specialist**: Researches external APIs, libraries, and creates integration guides

**Plan Storage & Review Process:**
- All research plans saved to `/plans/` directory with organized subdirectories
- Plan naming convention: `{agent-type}-{description}-{YYYY-MM-DD}.md`
- Review plans before implementation - agents research, humans implement
- Plans include comprehensive analysis, methodology, and actionable steps
```

### Testing Strategy
Define your project's testing approach:

```markdown
**Test Requirements:**
- Unit tests: Minimum 80% coverage for business logic
- Integration tests: All API endpoints
- E2E tests: Critical user journeys
- Performance tests: API response times < 200ms

**Test Organization:**
- Co-locate tests with source files
- Use `describe` blocks for feature grouping
- Test file naming: `*.test.ts` or `*.spec.ts`
- Mock external dependencies consistently

**TDD Research Integration:**
- Use TDD Research Specialist for complex testing strategy planning
- Research plans inform implementation approach and testing architecture
- Plans include test organization, coverage strategy, and validation approaches
```

### Code Review Standards
Your team's code review requirements:

```markdown
**Required before merge:**
- [ ] All tests passing
- [ ] Code coverage maintained or improved
- [ ] Documentation updated for public APIs
- [ ] Performance impact assessed
- [ ] Security implications considered
- [ ] Accessibility requirements met (for UI changes)

**Review checklist:**
- Business logic correctness
- Error handling completeness
- Code readability and maintainability
- Consistency with existing patterns
```

## Technical Mastery Progression

Track your learning objectives and skill development:

### Current Focus Areas (Update Weekly)
```markdown
**This Week's Learning Goals:**
- Target concept: [e.g., "Advanced TypeScript generics"]
- Learning method: [e.g., "Implement generic utility types from scratch"]
- Knowledge gap: [e.g., "Understanding conditional types and mapped types"]
- Success criteria: [e.g., "Can explain and implement utility types without AI assistance"]

**This Month's Major Goal:**
- [e.g., "Master React performance optimization patterns"]

**This Quarter's Objective:**
- [e.g., "Become proficient in system design for microservices"]
```

### Skill Progression Tracking
```markdown
**Current Skill Levels:**
- **Your Primary Language (e.g., TypeScript)**: Advanced → Expert
- **Your Framework (e.g., React)**: Intermediate → Advanced  
- **System Design**: Novice → Intermediate
- **Database Design**: Intermediate → Advanced
- **DevOps/Infrastructure**: Novice → Intermediate
- **Testing & Quality**: Advanced → Expert

**Skill Level Definitions:**
- **Novice**: Can use with AI guidance and documentation
- **Intermediate**: Can explain concepts and debug issues independently  
- **Advanced**: Can implement complex features from first principles
- **Expert**: Can teach others and contribute to architectural decisions
```

## Team Standards & Practices

### Communication Protocols
```markdown
**Development Communication:**
- Daily standups: Focus on blockers and dependencies
- Code reviews: Constructive feedback with specific suggestions
- Technical discussions: Document decisions and rationale
- Knowledge sharing: Weekly tech talks or pair programming sessions

**Documentation Requirements:**
- Architecture decisions: Record in ADR format
- API changes: Update OpenAPI/Swagger specs
- Database changes: Migration scripts with rollback plans
- Configuration changes: Update deployment documentation
```

### Deployment & Release Process
```markdown
**Release Workflow:**
1. Feature development in feature branches
2. Code review and CI/CD validation
3. Merge to staging for integration testing
4. Release candidate testing
5. Production deployment with monitoring
6. Post-release verification and monitoring

**Rollback Procedures:**
- Database migrations: Always reversible
- Feature flags: Immediate disable capability
- Infrastructure: Blue-green deployment strategy
- Monitoring: Automated alerts for key metrics
```

## Domain-Specific Rules

Add any domain-specific requirements for your project:

```markdown
**Example for E-commerce projects:**
- PCI DSS compliance for payment processing
- GDPR compliance for user data handling
- Performance requirements for high-traffic scenarios
- Security requirements for financial transactions

**Example for Healthcare projects:**
- HIPAA compliance for patient data
- Audit logging for all data access
- Data encryption at rest and in transit
- Role-based access control implementation

**Example for Financial services:**
- Regulatory compliance (SOX, Basel III, etc.)
- Risk management frameworks
- Audit trails for all transactions
- Real-time fraud detection requirements
```

## Custom Quality Gates

Define additional quality checks specific to your project:

```markdown
**Pre-commit Requirements:**
- [ ] All linting rules pass
- [ ] Unit tests pass with minimum coverage
- [ ] Type checking passes (if applicable)
- [ ] Security scanning passes
- [ ] Documentation updated

**Pre-deployment Requirements:**
- [ ] Integration tests pass
- [ ] Performance benchmarks met
- [ ] Security audit completed
- [ ] Monitoring and alerting configured
- [ ] Rollback plan documented
```

## Learning Resources & References

Track your team's preferred learning resources:

```markdown
**Primary Documentation:**
- [Your framework docs]
- [Your language official docs]
- [Your company's engineering handbook]

**Recommended Reading:**
- [Books relevant to your stack]
- [Architecture patterns for your domain]
- [Team-recommended articles and blogs]

**Training & Development:**
- [Internal training programs]
- [External courses or certifications]
- [Conference talks and workshops]
```

---

## How to Use This File

1. **Customize the sections above** to match your project's specific needs
2. **Remove examples** and replace with your actual requirements
3. **Update regularly** as your project and team standards evolve
4. **Use `/claude-md update-mastery`** to update the Technical Mastery section
5. **Keep synchronized** with your team's current practices and standards

**Remember:** This file is preserved when you update the template, so feel free to customize it extensively for your project's unique requirements.
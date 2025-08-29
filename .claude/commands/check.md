---
allowed-tools: all
description: Verify code quality, run tests, and ensure production readiness
---
# Quality Verification & Standards Enforcement

**Usage:**
- `/check` - Comprehensive quality verification and fixing
- `/check --fix` - Automatically fix issues where possible

**Examples:**
- `/check` - Comprehensive quality verification and fixing
- `/check --fix` - Automatically fix issues where possible


# CRITICAL REQUIREMENT: FIX ALL ERRORS!

**THIS IS NOT A REPORTING TASK - THIS IS A FIXING TASK!**

When you run `/check`, you are REQUIRED to:

1. **IDENTIFY** all errors, warnings, and issues
2. **FIX EVERY SINGLE ONE** - not just report them!
3. **USE MULTIPLE AGENTS** to fix issues in parallel:
   - Spawn one agent to fix linting issues
   - Spawn another to fix test failures
   - Spawn more agents for different files/modules
   - Say: "I'll spawn multiple agents to fix all these issues in parallel"
4. **DO NOT STOP** until:
   - ALL linters pass with ZERO warnings
   - ALL tests pass
   - Build succeeds
   - EVERYTHING is GREEN

**FORBIDDEN BEHAVIORS:**
- "Here are the issues I found" → NO! FIX THEM!
- "The linter reports these problems" → NO! RESOLVE THEM!
- "Tests are failing because..." → NO! MAKE THEM PASS!
- Stopping after listing issues → NO! KEEP WORKING!

**MANDATORY WORKFLOW:**
1. Run checks → Find issues
2. For complex quality problems, delegate to Quality Research Analyst agent
3. Review research plan for systematic issue resolution
4. IMMEDIATELY fix ALL issues based on research recommendations
5. Re-run checks → Find remaining issues
6. Fix those too
7. REPEAT until EVERYTHING passes

**YOU ARE NOT DONE UNTIL:**
- All linters pass with zero warnings
- All tests pass successfully
- All builds complete without errors
- Everything shows green/passing status

## Universal Quality Verification Protocol

**Step 1: Language-Agnostic Linting**
Run appropriate linters for ALL languages in the project:
- `make lint` if Makefile exists
- `~/.claude/hooks/smart-lint.sh` for automatic detection
- Manual linter runs if needed

**Universal Requirements:**
- ZERO warnings across ALL linters
- ZERO disabled linter rules without documented justification
- ZERO "nolint" or suppression comments without explanation
- ZERO formatting issues (all code must be auto-formatted)

**Step 2: Test Verification**
Run `make test` and ensure:
- ALL tests pass without flakiness
- Test coverage is meaningful (not just high numbers)
- Table-driven tests for complex logic
- No skipped tests without justification
- Tests actually test behavior, not implementation details

**Step 3: Quality Checklist**
- [ ] No commented-out code blocks
- [ ] No debugging print statements
- [ ] No placeholder implementations
- [ ] Consistent formatting
- [ ] Dependencies are actually used
- [ ] No circular dependencies

## Integration with Quality Research Analyst

### **Research-Driven Quality Resolution:**
For complex or systematic quality issues, `/check` integrates with the **Quality Research Analyst** agent:

- **Comprehensive Quality Assessment**: Agent analyzes all quality dimensions and creates detailed reports
- **Issue Categorization**: Systematically prioritizes problems by impact, effort, and risk
- **Systematic Remediation Plans**: Creates detailed step-by-step resolution strategies
- **Root Cause Analysis**: Investigates underlying causes behind quality problems

**Research Workflow Integration:**
```bash
/check                                 # Discovers multiple complex quality issues
# May delegate to Quality Research Analyst for systematic analysis
# Agent creates detailed plan in /plans/quality-analysis/
# Review research plan and remediation strategy
# Implement fixes based on systematic recommendations
```

All quality analysis plans are saved to `/plans/quality-analysis/` directory.

**Failure Response Protocol:**
When issues are found:
1. **ASSESS COMPLEXITY** - Simple issues: fix immediately; Complex issues: delegate research
2. **RESEARCH IF NEEDED** - Let Quality Research Analyst create systematic remediation plan
3. **FIX EVERYTHING** - Address EVERY issue based on research recommendations
4. **VERIFY** - Re-run all checks after fixes
5. **REPEAT** - If new issues found, continue systematic resolution
6. **NO STOPPING** - Keep working until ALL checks show GREEN
7. **NO EXCUSES** - Fix it NOW!

**Final Verification:**
The code is ready when:
- make lint: PASSES with zero warnings
- make test: PASSES all tests
- All checklist items verified
- Feature works end-to-end in realistic scenarios

**REMEMBER: This is a FIXING task, not a reporting task!**

The code is ready ONLY when every single check shows GREEN.
## Integration with Other Commands

- **`/check` → `/dev`**: Integration workflow
- **`/check` → `/debug`**: Integration workflow
- **`/check` → `/refactor`**: Integration workflow

**TDD-First Quality Pipeline:**
- **`/check` → `/check`**: Comprehensive quality validation (tests + linting + formatting)
- **`/check` → `/debug`**: When tests fail unexpectedly, switch to systematic debugging  
- **`/check` → `/ship`**: Create final commit with proper documentation
**Quality Requirements**:
- Follow all forbidden patterns from CLAUDE.md
- Use proper error handling for your language (Result types, exceptions)
- No unwrap(), expect(), panic!() in production code
- Delete old code when replacing functionality

**Universal Quality Standards:**
- **Delete** old code when replacing it
- **Meaningful names**: `user_id` not `id`, `process_payment` not `do_stuff`
- **Early returns** to reduce nesting depth
- **Proper error handling** for your language (exceptions, Result types, etc.)
- **Comprehensive tests** for complex logic
- **Consistent code style** following project/language conventions

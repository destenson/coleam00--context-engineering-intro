# Review Codebase and Recommend Next Steps

Comprehensively review the current codebase, assess its current state, and recommend the most impactful next action.

Make sure to check README.md, TODO.md, and any other relevant documentation files in the codebase.

## Phase 1: Current State Analysis

0. **Initial Setup**
   - Read through README.md and TODO.md for context
   - Familiarize yourself with the project structure
   - Check the git log for recent changes and PRs

1. **Check Implementation Status**
   - List core modules (*.rs files) and their current status
   - Identify any broken or incomplete components (e.g., TODOs, unimplemented features)
   - Check for any recently changed files

2. **Test Coverage Assessment**
   - Run tests and capture results
   - Count test functions

3. **Examples and Integration**
   - List and test examples
   - Identify any missing examples or integration tests

## Phase 2: PRP (Proposed Refinement Plan, or Project Requirements and Planning) Status Review

1. **List PRPs and Check Status**
   - List all PRPs (*.md files) in the PRPs directory
   - Check if each PRP has been executed or is still pending, or if it has been partially completed
   - Identify any PRPs that are fully implemented and working
   - Identify any PRPs that are incomplete or not yet implemented

2. For each PRP, determine if its target functionality exists in the codebase
   - If it exists, check if it is working as intended
   - If it does not exist, assess the impact of implementing it

## Phase 3: Strategic Assessment

1. **Identify Gaps and Technical Debt**
   - Count TODOs and issues (e.g., "FIXME", "HACK") in the codebase
   - Check for error handling quality (e.g., count the use of `unwrap()`, `expect()`, `panic!()` in non-test code)

2. **Validate Build Configuration**
   - Test feature combinations

## Phase 4: Record Implementation Decisions

Document the key architectural decisions made by the user during the implementation:
  1. Architectural decisions
  2. Code quality improvements
  3. Design patterns
  4. Technical solutions
  5. What wasn't implemented
  6. Lessons learned

## Output Format

Provide an update to a structured report at `codebase-review-report.md` with:

### Executive Summary
- Current implementation status (2-3 sentences)
- Primary recommendation with justification

### Implementation Status
- **Working**: [Component] - Evidence
- **Broken/Incomplete**: [Component] - Issue
- **Missing**: [Component] - Impact

### Code Quality
- Test Results: X/Y passing (Z%)
- TODO Count: X occurrences
- Examples: X/Y working

### Recommendation

**Next Action**: [Execute PRP(s) X] OR [Create new PRP(s) for Y]

**Justification**:
- Current capability: [What works now]
- Gap: [What's blocking progress]
- Impact: [What this enables]

**90-Day Roadmap**:
1. Week 1-2: [Action] → [Outcome]
2. Week 3-4: [Action] → [Outcome]
3. Week 5-8: [Action] → [Outcome]
4. Week 9-12: [Action] → [Outcome]

### Technical Debt Priorities
1. [Issue]: [Impact] - [Effort]
2. [Issue]: [Impact] - [Effort]

## Success Criteria
- Accurate current state assessment based on code inspection
- Executable validation of all findings
- Clear, actionable next step recommendation
- Roadmap with specific, measurable outcomes

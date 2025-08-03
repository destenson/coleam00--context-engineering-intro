# Review Codebase and Recommend Next Steps

Comprehensively review the current codebase, assess its current state, and recommend the most impactful next action.

## Phase 1: Current State Analysis

1. **Check Implementation Status**
   ```bash
   # List core modules
   find src/ -name "*.rs" -type f | head -20
   
   # Check for incomplete implementations
   rg -c "todo!\(|unimplemented!\(" src/
   
   # Find main algorithm implementations
   rg -l "impl.*(SpatialPooler|TemporalMemory|Classifier|AnomalyDetector)" src/
   ```

2. **Test Coverage Assessment**
   ```bash
   # Run tests and capture results
   cargo test --features "std,itertools,rayon,ndarray" 2>&1 | grep -E "test result:|[0-9]+ passed"
   
   # Count test functions
   rg -c "#\[test\]|#\[cfg\(test\)\]" src/
   ```

3. **Examples and Integration**
   ```bash
   # List and test examples
   ls -la examples/
   for example in examples/*.rs; do
     name=$(basename "$example" .rs)
     echo "Testing example: $name"
     cargo run --example "$name" 2>&1 | head -5
   done
   ```

## Phase 2: PRP Status Review

1. **List PRPs and Check Status**
   ```bash
   # List all PRPs
   ls -la PRPs/*.md
   
   # Extract status indicators
   for prp in PRPs/*.md; do
     echo "\n=== $(basename "$prp") ==="
     grep -i "confidence.*score\|status.*complete\|implemented" "$prp" | head -3
   done
   ```

2. For each PRP, determine if its target functionality exists in the codebase

## Phase 3: Strategic Assessment

1. **Identify Gaps and Technical Debt**
   ```bash
   # Count TODOs and issues
   rg -c "TODO|FIXME|HACK" src/
   
   # Check error handling quality
   rg "unwrap\(\)|expect\(|panic!" src/ | wc -l
   ```

2. **Validate Build Configuration**
   ```bash
   # Test feature combinations
   cargo build --features "std,itertools,rayon,ndarray"
   cargo clippy --all-targets --features "std,itertools,rayon,ndarray"
   cargo doc --no-deps --features "std,itertools,rayon,ndarray"
   ```

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

**Next Action**: [Execute PRP X] OR [Create new PRP for Y]

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

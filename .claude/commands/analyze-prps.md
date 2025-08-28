# Analyze and Update PRPs

**Purpose**: Compare Project Requirement Plans (PRPs) against the actual source code implementation and UPDATE the PRP markdown files to reflect reality. PRPs are planning documents that rarely get updated after implementation, so they become outdated. This command fixes that by making the documentation match the code (the source of truth).

## Target: $ARGUMENTS

If $ARGUMENTS is provided, it should be a path to a specific PRP file or a directory containing PRPs. If not provided, the default directory is `PRPs/` at the workspace root.

## Key Principle: Code is Truth, Documents Lie

**IMPORTANT**: 
- The SOURCE CODE is the source of truth - it shows what actually exists
- PRP files are planning documents that get outdated quickly  
- README/TODO files also get outdated and may show aspirational status
- This command's job is to make the PRP documentation accurate again

## Process

### 1. Discovery Phase - Find All PRPs
- Identify the target directory from `$ARGUMENTS` or use default `PRPs/`
- Use `Glob` or `LS` to find all `.md` files in the directory
- Create a list of ALL PRP files to process (don't get stuck on one!)

### 2. Analysis Phase - Check Implementation Status
**PROCESS EFFICIENTLY - IT'S OK TO WORK IN BATCHES**

For each PRP file:
- Read the PRP to identify key deliverables:
  - Files to be created (check with `Glob` or `LS`)
  - Features to implement (check with `Grep` for code presence)
  - Tests to write (check if test files exist)
  - Success criteria checkboxes `[ ]`

- Quickly verify against codebase:
  - Does the file/directory exist? YES/NO
  - Is the feature implemented? YES/NO/PARTIAL
  - Are tests present? YES/NO
  - Does implementation match plan? YES/NO/DIFFERENT
  - If DIFFERENT: Note the deviation pattern (renamed, restructured, enhanced, simplified)

### 3. Update Phase - Fix the PRP Documentation
**ALWAYS UPDATE BOTH INDIVIDUAL PRPs AND THE DASHBOARD**

For each PRP that needs updating:
- Update checkboxes from `[ ]` to `[x]` for completed items
- Add a status line at the top (preserving original PRP intent):
  ```
  **Status**: COMPLETED (YYYY-MM-DD) - All deliverables implemented
  **Status**: PARTIAL (YYYY-MM-DD) - X of Y tasks completed  
  **Status**: NOT STARTED (YYYY-MM-DD) - No implementation found
  ```
- Update the PRP metadata section if present
- Add an "Implementation Notes" section to capture deviations:
  ```markdown
  ## Implementation Notes
  - **Design Decision**: [What changed] and [Why it was better]
  - **Deviation**: [What differs from plan] ([Reason for change])
  - **Enhancement**: [What was added beyond plan]
  - **Simplification**: [What was removed or simplified]
  ```
- **Preserve the original PRP content** - only add status, don't remove planning text
- **Document WHY** things deviated when patterns don't match the plan

Also create/update `PRPs/README.md` dashboard:
- Generate a status table for all PRPs discovered
- Include completion percentages and last verification dates
- This serves as a quick overview without opening individual files

### 4. Summary Report Phase
Generate a concise report showing:
- PRPs analyzed this session (e.g., "X of Y total PRPs analyzed")
- Completion breakdown for this batch:
  - A PRPs fully completed
  - B PRPs partially completed  
  - C PRPs not started
- List of PRPs that were updated
- Progress indicator: "Z PRPs remaining to analyze"
- Confirmation: "PRPs/README.md dashboard updated with latest status"
- Key findings from this batch

## Example Workflow

```
1. Discover all PRP files in target directory
2. Process a reasonable batch (e.g., 10-20 PRPs per execution)
3. Update those PRPs that need it
4. Report progress: "Updated X of Y PRPs analyzed (Z remaining)"
5. User can re-run command to continue with next batch
```

**Batching Strategy**:
- If there are many PRPs, process them in manageable batches
- Prioritize PRPs that seem most likely to be implemented
- It's better to thoroughly analyze a subset than rush through all
- Each execution should provide value by updating some PRPs

## Common Patterns to Recognize

- **File Creation Tasks**: `CREATE src/module/file.rs` → Check if file exists
- **Feature Implementation**: `IMPLEMENT error handling` → Grep for error types
- **Test Coverage**: `ADD unit tests` → Check for test files
- **Documentation**: `UPDATE README.md` → Often outdated, skip or note

## Common Deviation Patterns to Look For

- **Structural Changes**: Files/modules organized differently than planned
- **Technical Decisions**: Different implementation approach taken
- **Scope Changes**: Features added, removed, or modified from original plan
- **Naming Changes**: Components renamed for clarity or consistency

## Output Format

```markdown
## PRP Analysis Complete

### Summary
- Analyzed: X PRPs (of Y total)
- Updated: Z PRPs
- Status: A Complete, B Partial, C Not Started
- Dashboard: PRPs/README.md updated

### Updated PRPs
- PRP-XX: [Title] - Updated to [STATUS] ([reason])
- PRP-YY: [Title] - Updated to [STATUS] ([reason])
- PRP-ZZ: [Title] - Updated to [STATUS] ([reason])
[... list all updated PRPs ...]

### Key Findings
- [Finding 1 about PRP status vs implementation]
- [Finding 2 about major deviations discovered]
- [Finding 3 about completion patterns]
```

## PRPs/README.md Dashboard Format

The command will generate/update a dashboard file at `PRPs/README.md`:

```markdown
# PRP Status Dashboard
Last Updated: YYYY-MM-DD by analyze-prps command

## Overview
| Metric | Count | Percentage |
|--------|-------|------------|
| Total PRPs | X | 100% |
| Completed | Y | Y% |
| Partial | Z | Z% |
| Not Started | W | W% |

## Status Details
| PRP | Title | Status | Completion | Last Verified | Notes |  
|-----|-------|--------|------------|---------------|-------|
| PRP-01 | [Title] | ✅ COMPLETE | X/X tasks | YYYY-MM-DD | - |
| PRP-02 | [Title] | 🔄 PARTIAL | Y/Z tasks | YYYY-MM-DD | [Note] |
| PRP-03 | [Title] | ❌ NOT STARTED | 0/W tasks | YYYY-MM-DD | - |
[... continue for all PRPs ...]

## Recent Changes
- YYYY-MM-DD: X PRPs updated to reflect implementation
- YYYY-MM-DD: Initial analysis of all PRPs
```

**Dashboard Benefits**:
- Quick overview without opening individual files
- Git-friendly format shows changes clearly
- Regenerated each run so it stays current
- Tracks verification history
- Highlights deviations for architecture documentation

## Tips for Efficiency

1. **Work in batches**: Process 10-20 PRPs per run if there are many
2. **Track progress**: Note which PRPs have been analyzed vs remaining
3. **Use grep counts**: `Grep` with count mode to quickly verify presence
4. **Skip validation commands**: Don't run test suites, just check they exist
5. **Focus on checkboxes**: Primary goal is updating `[ ]` to `[x]`
6. **Prioritize likely completions**: Start with PRPs mentioned as "completed" in README
7. **Dashboard is regenerated**: Don't worry about corrupting it, rebuilt each run

## Common Pitfalls to Avoid

❌ **DON'T** try to process all PRPs in one go if there are too many
❌ **DON'T** spend 10+ minutes analyzing a single PRP in detail
❌ **DON'T** try to understand the full implementation 
❌ **DON'T** run validation commands that might hang or take time
❌ **DON'T** trust README/TODO status over actual code presence
❌ **DON'T** assume documents are accurate - verify everything

✅ **DO** work in manageable batches (10-20 PRPs per execution)
✅ **DO** provide progress updates (X analyzed, Y remaining)
✅ **DO** update PRP files to match reality
✅ **DO** focus on file existence and basic implementation checks
✅ **DO** provide a clear summary of what was updated
✅ **DO** treat source code as the only truth
✅ **DO** preserve original PRP content while adding status
✅ **DO** regenerate the dashboard file completely each run
✅ **DO** document design decisions that caused deviations
✅ **DO** capture the VALUE of deviations (why the change was better)

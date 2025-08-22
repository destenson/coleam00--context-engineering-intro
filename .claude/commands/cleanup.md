# Cleanup Code

Remove dead code, unused imports, format inconsistencies.

## Target: $ARGUMENTS

If $ARGUMENTS is provided, focus cleanup on specific files, directories, or code areas mentioned.

## Cleanup Process

1. **Analyze current state**:
   - Scan for unused imports/dependencies
   - Identify dead/unreachable code
   - Check for formatting inconsistencies
   - Find duplicate code blocks
   - Locate empty or placeholder functions

2. **Language-specific cleanup**:
   - **Rust**: Remove unused imports, fix clippy warnings, format with rustfmt
   - **Python**: Remove unused imports, fix flake8/black issues, sort imports
   - **JavaScript/TypeScript**: Remove unused imports, fix eslint issues, format with prettier
   - **General**: Remove commented-out code, fix whitespace issues

3. **Code quality improvements**:
   - Consolidate duplicate logic
   - Remove debugging print statements
   - Clean up variable names and comments
   - Remove empty catch blocks or placeholder TODOs
   - Update deprecated function calls

4. **Validation**:
   - Ensure all tests still pass
   - Verify builds complete successfully
   - Check that functionality remains unchanged

## Output

Provide summary of cleanup actions taken and any issues found that require manual review.

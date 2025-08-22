# Cleanup Code

Remove dead code, unused imports, format inconsistencies, and improve overall code hygiene.

## Target: $ARGUMENTS

If $ARGUMENTS is provided, focus cleanup on specific files, directories, or code areas mentioned.

## Process

1. **Explore multiple cleanup opportunities and code quality issues**:
   - **Dead code detection**: Unreachable code, unused functions, abandoned features
   - **Import/dependency cleanup**: Unused imports, circular dependencies, outdated packages
   - **Formatting inconsistencies**: Mixed indentation, line endings, spacing issues
   - **Code duplication**: Identical blocks, similar logic, copy-paste patterns
   - **Placeholder code**: TODO stubs, empty implementations, debugging artifacts
   - **Naming improvements**: Unclear variables, inconsistent conventions, misleading names
   - **Documentation hygiene**: Outdated comments, redundant documentation, missing explanations

2. **Systematic analysis of current state**:
   - Scan entire codebase for automated cleanup opportunities
   - Identify manual review areas requiring human judgment
   - Check for language-specific linting and formatting violations
   - Analyze code complexity and refactoring opportunities
   - Review recent changes for cleanup debt accumulation
   - Assess impact of cleanup on functionality and testing

3. **Language-specific cleanup strategies**:
   - **Rust**: Remove unused imports, fix clippy warnings, format with rustfmt, check for unsafe code cleanup
   - **Python**: Remove unused imports, fix flake8/black/ruff issues, sort imports, update type hints
   - **JavaScript/TypeScript**: Remove unused imports, fix eslint/prettier issues, update deprecated APIs
   - **C/C++**: Remove unused headers, fix compiler warnings, format with clang-format
   - **General**: Remove commented-out code, fix whitespace issues, standardize file endings

4. **Code quality and maintainability improvements**:
   - Use the TodoWrite tool to organize cleanup tasks by priority
   - **Consolidation opportunities**: Merge duplicate logic, extract common patterns
   - **Debugging artifact removal**: Print statements, temporary variables, test data
   - **Variable and function naming**: Clear, descriptive, consistent naming
   - **Error handling cleanup**: Remove empty catch blocks, improve error messages
   - **Deprecated API updates**: Replace obsolete function calls, update to current APIs
   - **Resource cleanup**: Proper disposal, connection closing, memory management

5. **Automated tooling and validation**:
   - Run automated formatters and linters
   - Execute static analysis tools for cleanup suggestions
   - Use IDE refactoring tools for safe code transformations
   - Validate that automated changes don't break functionality
   - Set up pre-commit hooks for ongoing code hygiene

6. **Manual review and validation**:
   - Ensure all tests still pass after cleanup
   - Verify builds complete successfully across all environments
   - Check that functionality remains unchanged through testing
   - Review cleanup changes for unintended side effects
   - Validate performance impact of cleanup changes

## Cleanup Categories

### Automated Cleanup (Low Risk)
- Code formatting and style fixes
- Unused import removal
- Basic linting violations
- Whitespace and line ending normalization

### Semi-Automated Cleanup (Medium Risk)
- Variable renaming for clarity
- Simple code consolidation
- Comment and documentation updates
- Deprecated API replacements

### Manual Cleanup (High Risk)
- Dead code removal requiring domain knowledge
- Complex refactoring for duplicated logic
- Architecture cleanup and simplification
- Performance optimization during cleanup

## Output

Provide comprehensive cleanup report with:
- **Cleanup Summary**: Overview of changes made and code quality improvements
- **Automated Changes**: List of safe, tool-assisted modifications
- **Manual Review Items**: Code requiring human judgment before cleanup
- **Risk Assessment**: Potential impacts and areas requiring extra testing
- **Tool Configuration**: Recommended linting and formatting tool setup
- **Ongoing Hygiene**: Practices to maintain code cleanliness
- **Metrics**: Before/after code quality measurements where applicable

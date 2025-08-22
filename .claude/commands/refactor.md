# Refactor Code

Improve code structure while maintaining functionality.

## Code Smell: $ARGUMENTS

If $ARGUMENTS is provided, it may be file paths, code snippets, or descriptions of code smells. Use this to locate and understand the refactoring target.

## Execution Process

1. **Identify code smells**:
   - **Long methods/functions**: Break into smaller, focused functions
   - **Duplicate code**: Extract common logic into reusable functions
   - **Large classes**: Split responsibilities using single responsibility principle
   - **Deep nesting**: Use early returns, guard clauses, or strategy patterns
   - **Magic numbers**: Replace with named constants
   - **God objects**: Decompose into focused, cohesive components

2. **Brainstorm multiple refactoring approaches**:
   - Evaluate at least 3-4 different refactoring strategies and their trade-offs
   - Consider the long-term maintainability implications of each approach
   - Think through how each change affects testability, performance, and readability
   - Analyze potential ripple effects throughout the codebase
   - Consider whether incremental vs. comprehensive refactoring is more appropriate
   - Evaluate if the current design patterns are still the best fit
   - Think about future extensibility and how changes align with project direction

3. **Analyze current design**:
   - Understand the existing functionality completely
   - Identify dependencies and coupling points
   - Map out data flow and control flow
   - Note any existing tests that cover the code

4. **Plan refactoring strategy**:
   - Use the TodoWrite tool to create and track your plan
   - Choose appropriate refactoring patterns:
     - **Extract method**: Split large functions
     - **Extract class**: Separate concerns
     - **Move method**: Improve cohesion
     - **Rename**: Improve clarity
     - **Introduce parameter object**: Reduce parameter lists
     - **Replace conditional with polymorphism**: Eliminate complex if/else chains

5. **Execute refactoring**:
   - Make small, incremental changes
   - Run tests after each change to ensure functionality preserved
   - Update related documentation and comments
   - Maintain consistent coding style and conventions

6. **Validate improvements**:
   - Verify all tests pass
   - Check that performance is not negatively impacted
   - Ensure code is more readable and maintainable
   - Confirm adherence to project patterns and standards

7. **Document changes**:
   - Update comments and documentation
   - Note any API changes or breaking changes
   - Document design decisions for future maintainers

## Output

Provide refactored code with explanation of improvements made, design decisions, and confirmation that functionality is preserved.

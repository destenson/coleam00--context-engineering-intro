# Review Code

Analyze code for potential issues, best practices, and improvement opportunities.

## Target: $ARGUMENTS

If $ARGUMENTS is provided, focus on specific files, modules, commits, or pull requests mentioned.

## Process

1. **Explore multiple review perspectives**:
   - **Functionality**: Does the code do what it's supposed to do?
   - **Readability**: Is the code clear and self-documenting?
   - **Maintainability**: Will this be easy to modify and extend?
   - **Performance**: Are there obvious bottlenecks or inefficiencies?
   - **Security**: Are there potential vulnerabilities or data leaks?
   - **Testing**: Is the code well-tested and testable?
   - **Architecture**: Does it fit well with the overall system design?

2. **Systematic code analysis**:
   - **Code structure**: Function/class size, complexity, single responsibility
   - **Naming conventions**: Clear, consistent, descriptive names
   - **Error handling**: Proper exception handling, graceful failures
   - **Dependencies**: Appropriate use of external libraries, coupling
   - **Documentation**: Comments, docstrings, inline explanations
   - **Patterns**: Consistent use of established patterns and idioms

3. **Language-specific considerations**:
   - **Rust**: Ownership patterns, error handling with Result/Option, unsafe usage
   - **Python**: PEP compliance, type hints, resource management
   - **JavaScript/TypeScript**: Type safety, async/await usage, bundle size impact
   - **General**: Memory management, resource cleanup, thread safety

4. **Security and robustness review**:
   - Input validation and sanitization
   - Authentication and authorization checks
   - Data exposure and logging sensitivity
   - Potential injection vulnerabilities
   - Resource exhaustion protection

5. **Performance considerations**:
   - Algorithm efficiency and Big O complexity
   - Memory usage patterns
   - Database query optimization
   - Caching opportunities
   - Network request efficiency

6. **Provide actionable feedback**:
   - Use the TodoWrite tool to organize findings by priority
   - Categorize issues: Critical, Important, Minor, Suggestion
   - Provide specific examples and suggested improvements
   - Explain the reasoning behind recommendations
   - Highlight positive patterns worth replicating

## Output

Provide structured review feedback with:
- **Critical Issues**: Security vulnerabilities, bugs, breaking changes
- **Important Improvements**: Performance, maintainability, best practices
- **Minor Suggestions**: Style, naming, documentation improvements
- **Positive Highlights**: Good patterns, clever solutions, clear code

For each item, include file/line references, clear explanations, and specific improvement suggestions.

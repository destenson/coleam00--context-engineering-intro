# Add Test Cases

Generate comprehensive test cases for existing functions/modules.

## Target: $ARGUMENTS

If $ARGUMENTS is provided, focus on specific functions, modules, or components mentioned.

## Process

1. **Analyze the code to understand testing needs**:
   - Identify all public functions, methods, and API endpoints
   - Understand the expected inputs, outputs, and side effects
   - Review existing tests to identify gaps in coverage
   - Consider different types of testing needed (unit, integration, property-based)
   - Evaluate complex logic paths, edge cases, and error conditions

2. **Explore comprehensive test scenarios**:
   - **Happy path**: Normal inputs and expected outputs
   - **Edge cases**: Boundary values, empty inputs, maximum values
   - **Error conditions**: Invalid inputs, network failures, timeouts
   - **State-dependent behavior**: Different system states affecting outcomes
   - **Integration points**: Interactions with databases, APIs, file systems
   - **Performance characteristics**: Load testing, memory usage, timing
   - **Security considerations**: Input validation, authentication, authorization

3. **Design test strategy**:
   - Use the TodoWrite tool to create and track your test plan
   - Choose appropriate testing frameworks and tools for the language
   - Plan test data setup and teardown procedures
   - Consider mocking strategies for external dependencies
   - Design tests for maintainability and readability

4. **Language-specific testing approaches**:
   - **Rust**: Use `#[test]`, property testing with `proptest`, integration tests
   - **Python**: pytest, unittest, hypothesis for property testing
   - **JavaScript/TypeScript**: Jest, Mocha, Cypress for e2e
   - **API testing**: Postman, REST Assured, or language-specific HTTP clients

5. **Implement test cases**:
   - Write clear, descriptive test names that explain what is being tested
   - Follow AAA pattern (Arrange, Act, Assert) or Given-When-Then
   - Include both positive and negative test cases
   - Add performance and load tests where appropriate
   - Ensure tests are isolated and repeatable

6. **Validate test quality**:
   - Run tests to ensure they pass with current implementation
   - Verify tests fail when expected (by temporarily breaking code)
   - Check test coverage reports to identify missed areas
   - Review test readability and maintainability

## Output

Provide complete test files with clear organization, descriptive test names, and coverage for all identified scenarios. Include setup instructions and documentation for running the tests.

# Fix Bugs

Debug specific issues with context from error logs/descriptions.

## Bug Description: $ARGUMENTS

If $ARGUMENTS is provided, it may be error logs, stack traces, file paths, or bug descriptions. Use this to locate and understand the issue context.

## Execution Process

1. **Reproduce the bug**
   - Understand the steps to trigger the bug
   - Identify the expected vs actual behavior
   - Note environmental factors (OS, browser, data, etc.)
   - Capture detailed error information

2. **Analyze the problem**:
   - **Runtime errors**: Stack traces, memory issues, null pointers
   - **Logic errors**: Incorrect calculations, wrong conditions
   - **Integration errors**: API failures, database issues
   - **Performance bugs**: Timeouts, memory leaks, infinite loops
   - **UI/UX bugs**: Display issues, interaction problems

3. **Debugging techniques**:
   - Add strategic logging/debugging statements
   - Use debugger to step through problematic code
   - Isolate the issue with minimal test cases
   - Check recent changes that might have introduced the bug
   - Review assumptions about data, state, or external systems

4. **Root cause analysis**:
   - Trace the bug to its source (not just where it manifests)
   - Consider edge cases and boundary conditions
   - Check for race conditions or timing issues
   - Examine error handling and fallback logic

5. **Create fix plan**:
   - Use the TodoWrite tool to create and track your plan
   - Design solution that addresses root cause
   - Consider impact on existing functionality
   - Plan comprehensive test cases
   - Document the fix for future reference

6. **Execute and validate**:
   - Implement the fix with minimal changes
   - Test the specific bug scenario
   - Run full test suite to prevent regressions
   - Verify the fix handles edge cases

## Output

Provide explanation of the root cause, the fix implemented, and confirmation that the bug is resolved with proper testing.

# Fix Bugs

Debug specific issues with context from error logs/descriptions.

## Bug Description: $ARGUMENTS

If $ARGUMENTS is provided, it may be information like compiler output, a specific file path, error code, or description of the bug. Use this information to locate and understand the error context.

## Execution Process

1. **Identify the bug**
   - Read the error message carefully to identify the nature of the bug.
   - Locate the specific file and line number mentioned in the error message.
   - Understand the context of the bug by reviewing the surrounding code.

2. **Think out loud**
   - Identify potential causes of the bug.
   - Consider different possibilities, such as logic errors, incorrect assumptions, or edge cases.
   - Discuss the implications of the bug and how it may reveal issues in other parts of the codebase.

3. **Create a plan**
   - Use the TodoWrite tool to create and track your plan.
   - Eliminate the bad ideas and outline a plan to fix the bug, including any necessary changes to the code or configuration.
   - Create a comprehensive test plan to validate the fix and ensure no other parts of the codebase are affected.

4. **Execute the plan**
   - Execute the plan
   - Implement all the code

5. **Validate**
   - Run each validation command
   - Fix any failures
   - Re-run until all pass

6. **Complete**
   - Ensure all checklist items done
   - Run final validation suite
   - Report completion status

Note: If validation fails, fix and retry.

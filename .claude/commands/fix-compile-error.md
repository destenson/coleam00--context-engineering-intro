# Fix Compile Errors

Analyze the current project and fix any compile errors present in the codebase.

## Compile Error: $ARGUMENTS

If $ARGUMENTS is provided, it may be information like compiler output, a specific file path, error code, or description of the compile error. Use this information to locate and understand the error context.

## Execution Process

1. **Identify the error**
   - Read the compiler output carefully to identify the nature of the error.
   - Locate the specific file and line number mentioned in the error message.
   - Understand the context of the error by reviewing the surrounding code.

2. **Think out loud**
   - Identify potential causes of the compile error.
   - Consider different possibilities, such as syntax errors, type mismatches, missing imports, or incorrect configurations.
   - Discuss the implications of the error and how it may reveal issues in other parts of the codebase.
3. **Create a plan**
   - Use the TodoWrite tool to create and track your plan.
   - Eliminate the bad ideas and outline a plan to fix the error, including any necessary changes to the code or configuration.
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

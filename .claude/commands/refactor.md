# Refactor code

Improve code structure while maintaining functionality

## Code Smell: $ARGUMENTS

If $ARGUMENTS is provided, it may be information like a specific file path, code snippet, or description of the code smell. Use this information to locate and understand the code context.

## Execution Process

1. **Identify the code smell**
   - Read the code carefully to identify the nature of the code smell.
   - Locate the specific file and line number mentioned in the code smell description.
   - Understand the context of the code smell by reviewing the surrounding code.

2. **Think out loud**
   - Identify potential causes of the code smell.
   - Consider different possibilities, such as duplicated code, long methods, or large classes.
   - Discuss the implications of the code smell and how it may reveal issues in other parts of the codebase.

3. **Create a plan**
   - Use the TodoWrite tool to create and track your plan.
   - Eliminate the bad ideas and outline a plan to refactor the code, including any necessary changes to the code or configuration.
   - Create a comprehensive test plan to validate the refactor and ensure no other parts of the codebase are affected.

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

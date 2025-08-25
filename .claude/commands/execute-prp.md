# Execute BASE PRP

Implement a feature using using the PRP file. Start by reading `codebase-review-report.md`, if it exists, for important context and requirements. Then read the specified PRP file and follow all instructions in it. Update the README.md, and/or TODO.md, as needed.

## PRP File: $ARGUMENTS

If $ARGUMENTS is provided, use it to customize the execution of the PRP. If not, follow the recommendation in `codebase-review-report.md` and/or `TODO.md`. PRP files are located in PRPs/*.md.

## Execution Process

1. **Load PRP**
   - Read the specified PRP file
   - Understand all context and requirements
   - Follow all instructions in the PRP and extend the research if needed
   - Ensure you have all needed context to implement the PRP fully
   - Do more web searches and codebase exploration as needed

2. **ULTRATHINK**
   - Think hard before you execute the plan. Create a comprehensive plan addressing all requirements.
   - Break down complex tasks into smaller, manageable steps using your todos tools.
   - Use the TodoWrite tool to create and track your implementation plan.
   - Identify implementation patterns from existing code to follow.
   - Write code in small, focused, modules with unit tests to verify proper functionality.

3. **Execute the plan**
   - Execute the PRP
   - Implement all the code
     - Follow existing code patterns (read the APIs you're using, RTFM, use Grep & websearch to find examples)
     - Write unit tests for all new code
   - Document all new functionality and design decisions

4. **Validate**
   - Run each validation command
   - Fix any failures
   - Re-run until all pass

5. **Complete**
   - Ensure all checklist items done
   - Run final validation suite
   - Report completion status
   - Read the PRP again to ensure you have implemented everything

6. **Reference the PRP**
   - You can always reference the PRP again if needed

Note: If validation fails, use error patterns in PRP to fix and retry.

NO EMOJIS IN CODE!

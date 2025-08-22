# Fix Compile Errors

Analyze and fix compilation errors in the codebase.

## Compile Error: $ARGUMENTS

If $ARGUMENTS is provided, it may be compiler output, file path, error code, or error description. Use this to locate and understand the error context.

## Execution Process

1. **Identify the error**
   - Parse compiler output to extract error type, location, and message
   - Identify the programming language and build system
   - Locate the specific file and line number
   - Understand the context by reviewing related code

2. **Analyze multiple potential causes**:
   - Generate several hypotheses about what could be causing this error
   - Consider both obvious causes (syntax, typos) and subtle ones (environment, dependencies)
   - Think through the compilation process step-by-step to identify failure points
   - Evaluate whether this error might be masking other underlying issues
   - Consider if recent changes or updates could have introduced this problem

3. **Categorize error type**:
   - **Syntax errors**: Missing semicolons, brackets, quotes
   - **Type errors**: Type mismatches, undefined variables
   - **Import/dependency errors**: Missing modules, circular imports
   - **Configuration errors**: Build settings, compiler flags
   - **Environment errors**: Missing tools, wrong versions

4. **Language-specific analysis**:
   - **Rust**: Check Cargo.toml, use `cargo check`, analyze borrow checker errors
   - **Python**: Check imports, indentation, virtual environment
   - **JavaScript/TypeScript**: Check package.json, tsconfig, module resolution
   - **C/C++**: Check headers, linking, compiler flags

5. **Create fix plan**:
   - Use the TodoWrite tool to create and track your plan
   - Identify root cause (not just symptoms)
   - Plan minimal changes to resolve error
   - Consider impact on other parts of codebase
   - Plan validation steps

6. **Execute the fix**:
   - Make targeted changes to resolve the error
   - Test incrementally if multiple changes needed
   - Update related documentation if necessary

7. **Validate**:
   - Run compiler again to confirm fix
   - Run relevant tests to ensure no regression
   - Check for new errors introduced by changes

## Output

Provide the specific changes made, explanation of why they fix the error, and confirmation that compilation succeeds.

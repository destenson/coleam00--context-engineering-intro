# Audit Technical Debt

Identify and prioritize technical debt items across the codebase.

## Focus Area: $ARGUMENTS

If $ARGUMENTS is provided, it may include specific files, directories, or types of technical debt to focus on.

## Process

1. **Explore multiple dimensions of technical debt**:
   - **Code quality debt**: Complex functions, duplicate code, poor naming
   - **Architecture debt**: Tight coupling, missing abstractions, poor layering
   - **Testing debt**: Low coverage, brittle tests, missing integration tests
   - **Documentation debt**: Outdated docs, missing comments, unclear APIs
   - **Infrastructure debt**: Outdated dependencies, manual processes, config drift
   - **Performance debt**: Known bottlenecks, inefficient algorithms, resource leaks
   - **Security debt**: Unpatched vulnerabilities, weak authentication, data exposure

2. **Systematic debt discovery**:
   - **Code analysis**: Static analysis tools, complexity metrics, duplication detection
   - **Dependency audit**: Outdated packages, security vulnerabilities, license issues
   - **Test analysis**: Coverage reports, flaky tests, slow test suites
   - **Performance analysis**: Profiling results, monitoring alerts, user complaints
   - **Security scanning**: Vulnerability scanners, code review findings
   - **Documentation review**: Accuracy checks, completeness assessment

3. **Code-level technical debt identification**:
   - **Complexity indicators**: Cyclomatic complexity, nesting depth, function length
   - **Code smells**: Long parameter lists, god objects, feature envy
   - **Anti-patterns**: Spaghetti code, copy-paste programming, magic numbers
   - **Maintenance issues**: TODO comments, FIXME notes, HACK markers
   - **Language-specific issues**: Unsafe code (Rust), global state (Python), callback hell (JS)

4. **Infrastructure and process debt**:
   - **Deployment complexity**: Manual steps, environment inconsistencies
   - **Build system issues**: Slow builds, flaky CI, complex dependencies
   - **Monitoring gaps**: Missing alerts, inadequate logging, poor observability
   - **Development workflow**: Inefficient processes, tooling problems

5. **Prioritization and impact assessment**:
   - Use the TodoWrite tool to organize and prioritize findings
   - **Business impact**: Customer-facing issues, development velocity impact
   - **Risk assessment**: Security implications, stability concerns, compliance issues
   - **Effort estimation**: Time to fix, complexity of changes, coordination required
   - **Dependencies**: Blocking relationships, prerequisite work, team coordination

6. **Debt categorization and planning**:
   - **Critical**: Security vulnerabilities, production-breaking issues
   - **High**: Major performance issues, development blockers
   - **Medium**: Code quality improvements, minor performance issues
   - **Low**: Style improvements, nice-to-have refactoring
   - **Strategic**: Architecture improvements, technology upgrades

## Technical Debt Categories

### Code Quality Debt
- Complex functions requiring refactoring
- Duplicate code blocks needing consolidation  
- Poor naming and unclear interfaces
- Missing error handling and validation
- Inconsistent coding standards

### Testing Debt
- Low test coverage areas
- Flaky or unreliable tests
- Missing integration and end-to-end tests
- Slow test execution times
- Outdated test data and scenarios

### Documentation Debt
- Outdated or incorrect documentation
- Missing API documentation
- Unclear setup instructions
- Absent architecture documentation
- Poor code comments and explanations

### Infrastructure Debt
- Outdated dependencies and libraries
- Manual deployment processes
- Configuration management issues
- Missing monitoring and alerting
- Inconsistent environments

### Performance Debt
- Known performance bottlenecks
- Inefficient database queries
- Memory leaks and resource issues
- Slow startup times
- Unoptimized critical paths

## Output

Provide technical debt audit report with:
- **Executive Summary**: Overall debt status and business impact
- **Critical Debt Items**: Immediate attention required with specific remediation plans
- **Categorized Debt Inventory**: Organized by type and priority
- **Risk Assessment**: Security, stability, and performance implications  
- **Remediation Roadmap**: Prioritized plan with effort estimates and dependencies
- **Prevention Strategy**: Practices to avoid accumulating new debt
- **Metrics and Tracking**: How to measure debt reduction progress

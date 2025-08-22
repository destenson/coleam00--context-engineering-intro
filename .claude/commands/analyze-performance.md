# Analyze Performance

Identify performance bottlenecks and optimization opportunities.

## Target: $ARGUMENTS

If $ARGUMENTS is provided, focus on specific components, functions, or performance issues mentioned.

## Process

1. **Establish performance baseline and explore problem areas**:
   - Profile the application to identify current performance characteristics
   - Consider multiple performance dimensions: CPU, memory, I/O, network
   - Analyze user-reported performance issues or complaints
   - Review system monitoring data and logs for patterns
   - Examine load testing results and stress test outcomes
   - Consider performance requirements and SLA targets

2. **Systematic bottleneck identification**:
   - **CPU-bound issues**: Hot code paths, inefficient algorithms, excessive computation
   - **Memory issues**: Leaks, excessive allocation, poor garbage collection
   - **I/O bottlenecks**: Database queries, file operations, network requests
   - **Concurrency problems**: Lock contention, race conditions, blocking operations
   - **Architecture issues**: Poor caching, excessive round trips, inefficient data structures

3. **Language and platform-specific analysis**:
   - **Rust**: Allocation patterns, async performance, unsafe optimizations
   - **Python**: GIL contention, import overhead, C extension opportunities
   - **JavaScript**: Event loop blocking, bundle size, DOM manipulation
   - **Database**: Query optimization, indexing, connection pooling
   - **Web**: Rendering performance, asset loading, caching strategies

4. **Measurement and profiling**:
   - Use appropriate profiling tools for the technology stack
   - Measure before and after any optimization attempts
   - Set up performance monitoring and alerting
   - Create reproducible performance test scenarios
   - Document baseline metrics and improvement targets

5. **Optimization strategy planning**:
   - Use the TodoWrite tool to prioritize optimization opportunities
   - Focus on high-impact, low-effort improvements first
   - Consider trade-offs between performance and other qualities (maintainability, security)
   - Plan incremental improvements with measurable goals
   - Evaluate whether optimization is worth the complexity cost

6. **Implementation and validation**:
   - Apply optimizations incrementally with careful measurement
   - Verify that optimizations don't introduce bugs or regressions
   - Test performance improvements under realistic load conditions
   - Document optimization techniques for future reference

## Common Optimization Techniques

- **Algorithm improvements**: Better complexity, more efficient data structures
- **Caching strategies**: In-memory, distributed, CDN, browser caching
- **Database optimization**: Query tuning, indexing, connection pooling
- **Async programming**: Non-blocking I/O, parallel processing
- **Resource pooling**: Connection pools, object pools, thread pools
- **Lazy loading**: Defer expensive operations until needed
- **Compression**: Data compression, asset minification
- **Profiling-guided optimization**: Focus on actual bottlenecks, not assumptions

## Output

Provide performance analysis report with:
- **Current Performance Profile**: Baseline metrics and bottleneck identification
- **Root Cause Analysis**: Why performance issues exist
- **Optimization Recommendations**: Prioritized list with expected impact
- **Implementation Plan**: Step-by-step optimization approach
- **Success Metrics**: How to measure improvement
- **Monitoring Strategy**: Ongoing performance tracking approach

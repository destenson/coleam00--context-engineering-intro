# Security Audit

Scan for common security issues and vulnerabilities.

## Target: $ARGUMENTS

If $ARGUMENTS is provided, focus on specific components, endpoints, or security concerns mentioned.

## Process

1. **Explore multiple attack vectors and security dimensions**:
   - **Input validation**: Injection attacks, malformed data, boundary testing
   - **Authentication**: Weak passwords, session management, multi-factor authentication
   - **Authorization**: Privilege escalation, access control bypass, role verification
   - **Data protection**: Encryption at rest/transit, sensitive data exposure
   - **Network security**: TLS configuration, certificate validation, secure protocols
   - **Infrastructure**: Container security, dependency vulnerabilities, environment configuration

2. **Systematic vulnerability assessment**:
   - **OWASP Top 10**: Injection, broken authentication, sensitive data exposure, XXE, broken access control, security misconfiguration, XSS, insecure deserialization, known vulnerabilities, insufficient logging
   - **Code-level issues**: Buffer overflows, race conditions, resource leaks
   - **Configuration problems**: Default credentials, exposed debug endpoints, verbose error messages
   - **Dependency risks**: Outdated libraries, known CVEs, license compliance

3. **Technology-specific security concerns**:
   - **Web applications**: CSRF, XSS, SQL injection, session hijacking
   - **APIs**: Rate limiting, input validation, authentication bypass
   - **Rust**: Unsafe code blocks, integer overflow, memory safety
   - **Python**: Pickle deserialization, code injection, path traversal
   - **JavaScript**: Prototype pollution, eval injection, DOM-based XSS
   - **Database**: SQL injection, privilege escalation, data encryption

4. **Infrastructure and deployment security**:
   - Container and orchestration security
   - Cloud configuration and IAM policies
   - Network segmentation and firewall rules
   - Logging and monitoring security events
   - Backup and disaster recovery security

5. **Security testing and validation**:
   - Use the TodoWrite tool to organize security testing plan
   - Automated security scanning tools and static analysis
   - Manual penetration testing techniques
   - Security code review practices
   - Threat modeling for critical components

6. **Risk assessment and prioritization**:
   - Evaluate severity and likelihood of identified vulnerabilities
   - Consider business impact and regulatory compliance requirements
   - Prioritize fixes based on exploitability and potential damage
   - Document security findings with clear remediation steps

## Common Security Issues to Check

- **Input Validation**: SQL injection, XSS, command injection, path traversal
- **Authentication**: Weak passwords, session fixation, brute force protection
- **Authorization**: Horizontal/vertical privilege escalation, insecure direct object references
- **Cryptography**: Weak algorithms, improper key management, insufficient randomness
- **Error Handling**: Information disclosure, stack trace exposure
- **Logging**: Insufficient logging, log injection, sensitive data in logs
- **Configuration**: Default credentials, debug mode in production, unnecessary services

## Output

Provide security audit report with:
- **Executive Summary**: Overall security posture and critical findings
- **Critical Vulnerabilities**: Immediate security risks requiring urgent attention
- **High Priority Issues**: Significant security concerns with remediation plans
- **Medium/Low Priority Items**: Best practice improvements and hardening opportunities
- **Compliance Notes**: Regulatory requirements and industry standard adherence
- **Remediation Roadmap**: Prioritized action plan with timelines
- **Security Recommendations**: Ongoing security practices and monitoring

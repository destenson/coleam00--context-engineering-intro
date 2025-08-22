# Generate Documentation

Create or update comprehensive documentation including API docs, code comments, and architecture documentation.

## Documentation Type: $ARGUMENTS

If $ARGUMENTS is provided, it may specify the type of documentation needed (API, code, architecture, user guide, etc.).

## Process

1. **Analyze documentation needs from multiple perspectives**:
   - **Audience analysis**: Developers, end users, operators, stakeholders
   - **Current state assessment**: Existing docs, gaps, outdated information
   - **Content types needed**: API reference, tutorials, guides, troubleshooting
   - **Maintenance requirements**: Automation opportunities, update frequency
   - **Integration points**: Code generation, CI/CD, version control
   - **Accessibility needs**: Language, technical level, format preferences

2. **Documentation strategy planning**:
   - **Information architecture**: Organization, navigation, cross-references
   - **Content standards**: Style guide, templates, formatting conventions  
   - **Tooling decisions**: Documentation generators, hosting platforms
   - **Workflow integration**: Docs-as-code, review processes, automation
   - **Version management**: Sync with code versions, deprecation handling

3. **Content creation and organization**:
   - Use the TodoWrite tool to plan documentation structure
   - **API Documentation**: Endpoint descriptions, parameters, examples, error codes
   - **Code Documentation**: Inline comments, docstrings, architectural decisions
   - **User Guides**: Getting started, tutorials, common workflows
   - **Developer Guides**: Setup instructions, development workflows, contribution guidelines
   - **Architecture Documentation**: System design, data flow, decision records

4. **Language and platform-specific documentation**:
   - **Rust**: Rustdoc comments, cargo doc generation, example code
   - **Python**: Docstrings, Sphinx, type annotations documentation
   - **JavaScript/TypeScript**: JSDoc, TypeDoc, README examples
   - **API**: OpenAPI/Swagger, Postman collections, interactive examples
   - **Architecture**: ADRs, C4 diagrams, sequence diagrams

5. **Documentation quality and maintenance**:
   - **Accuracy validation**: Code examples that compile/run, link checking
   - **Clarity testing**: User testing, feedback collection, iterative improvement  
   - **Automation setup**: Doc generation, deployment, broken link detection
   - **Update processes**: Triggered by code changes, regular review cycles
   - **Metrics tracking**: Usage analytics, feedback scores, maintenance burden

6. **Integration and deployment**:
   - **Hosting strategy**: Static site generators, documentation platforms
   - **Search and discovery**: Full-text search, tagging, categorization
   - **Cross-references**: Inter-doc linking, code-to-docs traceability
   - **Multiple formats**: Web, PDF, mobile, offline access

## Documentation Types and Standards

### API Documentation
- Complete endpoint listings with HTTP methods and URLs
- Request/response examples with realistic data
- Error code explanations and troubleshooting
- Authentication and authorization details
- Rate limiting and usage guidelines

### Code Documentation  
- Function/method documentation with parameters and return values
- Class and module overview documentation
- Usage examples and common patterns
- Architecture decision records (ADRs)
- Inline comments for complex logic

### User Documentation
- Getting started guides and tutorials
- Feature documentation with screenshots
- Troubleshooting and FAQ sections  
- Configuration and customization guides
- Migration and upgrade instructions

### Developer Documentation
- Development environment setup
- Build and deployment processes
- Testing strategies and guidelines
- Contributing guidelines and code standards
- Release processes and versioning

## Output

Provide comprehensive documentation package including:
- **Documentation Plan**: Structure, audience, and maintenance strategy
- **Generated Content**: Complete documentation files in appropriate formats
- **Style Guide**: Writing standards and formatting conventions  
- **Automation Setup**: Tools and processes for maintaining docs
- **Integration Instructions**: How to incorporate into development workflow
- **Maintenance Guidelines**: Update procedures and quality assurance

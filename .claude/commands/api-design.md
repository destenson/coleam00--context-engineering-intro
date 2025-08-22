# API Design

Design REST/GraphQL APIs with proper patterns and best practices.

## API Type: $ARGUMENTS

If $ARGUMENTS is provided, it may specify REST, GraphQL, or other API requirements and constraints.

## Process

1. **Explore multiple design approaches and considerations**:
   - **API style trade-offs**: REST vs GraphQL vs RPC vs event-driven
   - **Resource modeling**: Entity relationships, hierarchies, aggregations
   - **Consumer perspectives**: Web frontend, mobile apps, third-party integrations
   - **Scalability requirements**: Read/write patterns, caching, pagination
   - **Evolution strategy**: Versioning, backward compatibility, deprecation
   - **Security model**: Authentication, authorization, rate limiting

2. **Resource and endpoint design**:
   - **RESTful principles**: Proper HTTP verbs, status codes, resource URIs
   - **Resource relationships**: Nested resources, linking, embedding strategies  
   - **Collection patterns**: Filtering, sorting, pagination, search
   - **Idempotency**: Safe operations, retry handling, duplicate prevention
   - **Bulk operations**: Batch processing, transaction handling

3. **Request and response design**:
   - **Content negotiation**: JSON, XML, protobuf, content-type handling
   - **Request validation**: Schema validation, input sanitization, error responses
   - **Response structure**: Consistent formatting, metadata inclusion, error details
   - **Hypermedia**: HATEOAS principles, discoverable APIs, link relations
   - **Compression**: Response compression, request size limits

4. **Authentication and authorization patterns**:
   - **Authentication mechanisms**: JWT, OAuth 2.0, API keys, mutual TLS
   - **Authorization models**: RBAC, ABAC, resource-based permissions
   - **Token management**: Refresh tokens, expiration, revocation
   - **Security headers**: CORS, CSP, rate limiting, DDoS protection

5. **API evolution and versioning**:
   - Use the TodoWrite tool to plan versioning strategy
   - **Versioning approaches**: URL versioning, header versioning, content negotiation
   - **Backward compatibility**: Additive changes, deprecation policies
   - **Migration strategies**: Gradual rollout, dual-version support
   - **Documentation evolution**: Change logs, migration guides

6. **Performance and scalability design**:
   - **Caching strategies**: ETags, cache headers, CDN integration
   - **Rate limiting**: Per-user, per-endpoint, burst handling
   - **Database optimization**: N+1 query prevention, efficient joins
   - **Async patterns**: Webhooks, polling, server-sent events

## Technology-Specific Considerations

### REST API Design
- Resource-oriented URLs and proper HTTP verb usage
- Stateless operations with clear semantics
- Standard HTTP status codes and error handling
- OpenAPI/Swagger documentation

### GraphQL API Design  
- Schema design with types, queries, mutations, subscriptions
- Resolver optimization and N+1 query prevention
- Error handling and partial results
- Introspection and schema evolution

### Real-time APIs
- WebSocket connection management
- Event streaming and message queuing
- Connection scaling and load balancing
- Message ordering and delivery guarantees

## Output

Provide comprehensive API design including:
- **API Architecture**: Overall design approach and technology choices
- **Resource Model**: Entity definitions and relationships
- **Endpoint Specification**: Complete API endpoints with examples
- **Schema Definitions**: Request/response schemas and validation rules
- **Authentication Design**: Security implementation details
- **Documentation**: API documentation with examples and usage patterns
- **Implementation Guidelines**: Development and deployment recommendations

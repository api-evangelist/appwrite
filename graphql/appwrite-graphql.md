# Appwrite GraphQL API

Appwrite exposes its full backend API surface through a GraphQL endpoint that mirrors every REST operation. All services — Account, Databases, Storage, Functions, Teams, Locale, Messaging, and Users — are accessible as GraphQL queries (for GET operations) and mutations (for POST, PUT, PATCH, and DELETE operations). The schema is generated dynamically from Appwrite's route definitions, so field names follow the pattern of `{namespace}{MethodName}` (e.g., `accountGet`, `databasesListDocuments`, `storageCreateFile`). Appwrite uses `_` instead of `$` for internal model fields in GraphQL (e.g., `_id`, `_createdAt`, `_permissions`), because `$` is reserved in GraphQL syntax.

Authentication is handled through the same mechanisms as the REST API: client session cookies, JWT tokens passed via the `x-appwrite-jwt` header, API keys via the `x-appwrite-key` header, or Admin mode. The GraphQL endpoint supports all four Appwrite auth types — Session, JWT, API Key, and Admin. Requests may be sent as GET with query parameters, POST with `application/json` (single object or array for batching), POST with `application/graphql`, or multipart form-data for file uploads.

The GraphQL endpoint supports query batching, allowing multiple queries or mutations to be sent in a single HTTP request as a JSON array. Introspection is available on Appwrite Cloud and self-hosted instances (unless disabled by the project administrator). Field selection sets let clients request only the data they need, reducing bandwidth. Complex query controls (depth and complexity limits) are enforced server-side.

**Endpoint:** https://{hostname}/v1/graphql

**Mutation Endpoint:** https://{hostname}/v1/graphql/mutation

**Documentation:** https://appwrite.io/docs/apis/graphql

**References:**
- Documentation: https://appwrite.io/docs/apis/graphql
- GettingStarted: https://appwrite.io/docs/quick-starts

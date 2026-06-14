# Testmail.app GraphQL API

The Testmail.app GraphQL API provides a full-featured interface for querying test emails from programmable inboxes. Emails are routed to addresses in the format `{namespace}.{tag}@inbox.testmail.app`, where a namespace is a unique identifier tied to an API key and a tag is a freely chosen sub-inbox label. The API exposes a single `inbox` query that retrieves emails matching a namespace and optional tag or tag prefix, returning a rich `Email` object with parsed headers, body content (HTML and plaintext), attachments, SPF/DKIM authentication results, and spam scoring via SpamAssassin.

The API supports advanced filtering (include/exclude by field and wildcard or exact match) and custom multi-field sorting, as well as offset-based pagination via `limit` and `offset` parameters. A `livequery` mode allows clients to hold a connection open and wait for the next matching email to arrive rather than repeatedly polling — particularly useful in CI/CD pipelines that trigger an email flow and need to confirm delivery without polling loops. Authentication is performed via a Bearer token in the `Authorization` header using the API key generated at testmail.app.

The endpoint accepts standard GraphQL POST requests with JSON bodies. There are no mutations — Testmail is a receive-only email testing service. The schema includes object types for `Inbox`, `Email`, `ParsedAddress`, `HeaderLine`, and `Attachment`, plus input types and enums for advanced filtering and sorting. Attachments and raw MIME messages are available for download at hosted URLs returned in the `downloadUrl` fields.

**Endpoint:** https://api.testmail.app/api/graphql

**Documentation:** https://testmail.app/docs/

**References:**

- Documentation: https://testmail.app/docs/
- GettingStarted: https://testmail.app/docs/
- Reference: graphql/testmail-app-schema.graphql

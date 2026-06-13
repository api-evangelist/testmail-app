# Testmail

Testmail is an email testing API platform for developers and QA teams that provides programmable inboxes with unlimited email addresses via a namespace.tag routing scheme. It offers both a JSON REST API and a GraphQL API for instant, programmatic retrieval of test emails, supporting automated end-to-end email testing in development workflows and CI/CD pipelines.

Key capabilities include wildcard tag searches, live queries, pagination, spam score testing via SpamAssassin, and attachment handling. Teams at Salesforce, Adobe, Atlassian, and SAP rely on Testmail for automated email testing.

- **Website:** https://testmail.app
- **Documentation:** https://testmail.app/docs/
- **Pricing:** https://testmail.app/pricing/
- **Status:** https://status.testmail.app
- **Blog:** https://testmail.app/blog/
- **GitHub:** https://github.com/testmail-app
- **X:** https://x.com/testmailapp

## APIs

- **JSON API** — `https://api.testmail.app/api/json` — REST endpoint with API key auth via query parameter
- **GraphQL API** — `https://api.testmail.app/api/graphql` — Full GraphQL endpoint with Bearer token auth

## Plans

| Plan | Price | Emails/Month | Retention | Namespaces |
|------|-------|-------------|-----------|------------|
| Free | $0/mo | 100 | 1 day | 1 (random) |
| Essential | $9/mo | Unlimited | 3 days | 1 (random) |
| Pro | $39/mo | Unlimited | 30 days | Unlimited (custom) |
| Enterprise | $129/mo | Unlimited | 30 days | Unlimited (custom) |

## Artifacts

- [`apis.yml`](apis.yml) — APIs.json 0.19 index
- [`plans/testmail-app-plans-pricing.yml`](plans/testmail-app-plans-pricing.yml) — API Commons Plans 0.1
- [`rate-limits/testmail-app-rate-limits.yml`](rate-limits/testmail-app-rate-limits.yml) — API Commons Rate Limits 0.1
- [`finops/testmail-app-finops.yml`](finops/testmail-app-finops.yml) — FinOps Framework 1.0 analysis

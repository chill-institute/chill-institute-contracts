# API Reference

Entry point for the public `chill.institute` API docs.

## Canonical URLs

| Surface | URL |
|---------|-----|
| API host | `https://api.chill.institute` |
| v4 docs UI | `https://api.chill.institute/v4` |
| v4 OpenAPI doc | `https://api.chill.institute/v4/docs` |
| v4 RPC base | `https://api.chill.institute/v4` |
| Core service prefix | `https://api.chill.institute/v4/chill.v4.CoreService/*` |
| User service prefix | `https://api.chill.institute/v4/chill.v4.UserService/*` |
| v3 compatibility | `https://api.chill.institute/v3` |

## Auth

| Surface | Header | Format |
|---------|--------|--------|
| `CoreService` | `X-API-Key` | raw API key |
| `UserService` | `Authorization` | `Bearer <token>` |
| v3 compatibility | `X-API-Key` or user bearer token | deprecated |

Do not send API keys as `Authorization: Bearer ...`.

## Source Of Truth

The schema lives in:

- `proto/chill/v4/api.proto`
- `gen/openapi/chill/v4/api.swagger.yaml`
- `gen/go/chill/v4/`
- `gen/ts/chill/v4/`

Use the generated OpenAPI and generated client artifacts for field-level request and response details. Keep this page short and update it only when service URLs, auth, or doc entry points change.

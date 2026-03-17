# API Reference

Entry point for the public `chill.institute` API docs.

## Canonical URLs

| Surface | URL |
|---------|-----|
| API host | https://api.chill.institute |
| v4 OpenAPI doc | https://api.chill.institute/v4 |

## Auth

| Surface | Header | Format |
|---------|--------|--------|
| `v4.CoreService` | `X-API-Key` | Service key |
| `v4.UserService` | `Authorization` | User Token: `Bearer <token>` |

## Source Of Truth

The schema lives in:

- `proto/chill/v4/api.proto`
- `gen/openapi/chill/v4/api.swagger.yaml`
- `gen/go/chill/v4/`
- `gen/ts/chill/v4/`

Use the generated OpenAPI and generated client artifacts for field-level request and response details.

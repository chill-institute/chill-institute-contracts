# Development

Development and release notes for `chill-institute/contracts`.

## Tooling

This repo uses [`mise`](https://mise.jdx.dev/) for local tooling and generation.

```bash
mise install
mise run generate
mise run verify
```

## Repository Role

This repo owns:

- protobuf source files in `proto/`
- generated Go artifacts in `gen/go/`
- generated TypeScript artifacts in `gen/ts/`
- generated OpenAPI output in `gen/openapi/`

This repo does not own:

- backend implementation
- web, mobile, or CLI application logic
- deploy/runtime configuration

## Consumer Usage

Go consumers import generated artifacts directly:

```go
import chillv4 "github.com/chill-institute/contracts/gen/go/chill/v4"
import chillv4connect "github.com/chill-institute/contracts/gen/go/chill/v4/chillv4connect"
```

TypeScript consumers install `@chill-institute/contracts`:

```bash
npm install @chill-institute/contracts
```

Example import:

```ts
import { UserService } from "@chill-institute/contracts/chill/v4/api_pb";
```

## Release Flow

Normal contract change flow:

1. Update `proto/`.
2. Run `mise run generate`.
3. Review generated output in `gen/go`, `gen/ts`, and `gen/openapi`.
4. Run `mise run verify`.
5. Commit schema and generated output together.
6. Tag and publish a release.

Consumers should depend on tagged releases, not `main`.

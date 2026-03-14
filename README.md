# `chill-institute/contracts`

![Protobuf](https://img.shields.io/badge/schema-Protobuf-black)
![Connect](https://img.shields.io/badge/RPC-Connect-black)
![OpenAPI](https://img.shields.io/badge/output-OpenAPI-black)

Canonical protobuf API contracts and generated client artifacts for `chill.institute`.

This repository is the source of truth for the public RPC surface used by official `chill.institute` clients. It contains protobuf schema plus generated Go, TypeScript, and OpenAPI artifacts.

Start here:

```bash
mise install
mise run generate
mise run verify
```

Key docs:

- [docs/DEVELOPMENT.md](./docs/DEVELOPMENT.md)

Main paths:

- `proto/`
- `gen/go/`
- `gen/ts/`
- `gen/openapi/`

Consumers should depend on tagged releases, not `main`.

## License

MIT. See [LICENSE](./LICENSE).

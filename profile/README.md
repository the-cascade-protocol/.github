# Cascade Protocol

**A developer-first framework for structured, patient-owned health data.**

Cascade Protocol provides semantic vocabularies, serialization formats, and developer tools for building health applications where patients own and control their data. All processing is local-first -- no data leaves the user's machine.

## Repositories

| Repository | Description | Status |
|---|---|---|
| [spec](https://github.com/the-cascade-protocol/spec) | Ontology files, SHACL shapes, serialization specification, JSON-LD context | Stable |
| [conformance](https://github.com/the-cascade-protocol/conformance) | Conformance test fixtures, reference Patient Pod | Stable |
| [cli](https://github.com/the-cascade-protocol/cli) | `cascade-cli` -- validate, convert, query, and manage health data | v0.2.0 |
| [sdk-typescript](https://github.com/the-cascade-protocol/sdk-typescript) | TypeScript SDK (`@cascade-protocol/sdk`) | v1.0.0 |

## Quick Start

```bash
# Install the CLI
npm install -g @cascade-protocol/cli

# Initialize a Pod with reference data
cascade pod init --template reference ./my-pod

# Query medications
cascade pod query ./my-pod --medications

# Validate data
cascade validate ./my-pod
```

## Key Principles

- **Local-first**: Zero network calls during operation. All data stays on your machine.
- **Patient-owned**: Data stored in portable Pods that users control.
- **Provenance-tracked**: Every record carries its origin -- clinical, device, self-reported, or AI-generated.
- **Semantic**: Built on RDF/OWL with W3C PROV-O provenance. SPARQL-ready knowledge graphs.
- **Open**: Apache 2.0 (code) / CC-BY 4.0 (specifications). No proprietary dependencies.

## Links

- [cascadeprotocol.org](https://cascadeprotocol.org) -- Documentation & playground
- [Security & Compliance Guide](https://cascadeprotocol.org/docs/security/)
- [Getting Started (TypeScript)](https://cascadeprotocol.org/docs/getting-started/typescript/)

## License

Code repositories: [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
Specification & documentation: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

# Cascade Protocol

**A developer-first framework for structured, patient-owned health data.**

Cascade Protocol provides semantic vocabularies, serialization formats, and developer tools for building health applications where patients own and control their data. All processing is local-first — no data leaves the user's machine.

## Repositories

| Repository | Description | Status |
|---|---|---|
| [spec](https://github.com/the-cascade-protocol/spec) | Ontology files, SHACL shapes, serialization specification, JSON-LD context | Stable |
| [conformance](https://github.com/the-cascade-protocol/conformance) | Conformance test fixtures, reference Patient Pod | Stable |
| [cascade-cli](https://github.com/the-cascade-protocol/cascade-cli) | CLI for validating, converting, querying, and managing health data Pods | v0.3.1 |
| [sdk-typescript](https://github.com/the-cascade-protocol/sdk-typescript) | TypeScript SDK (`@the-cascade-protocol/sdk`) | v1.1.0 |
| [sdk-python](https://github.com/the-cascade-protocol/sdk-python) | Python SDK (`cascade-protocol`) | v1.0.1 |
| [cascade-agent](https://github.com/the-cascade-protocol/cascade-agent) | Natural language interface for the Cascade Protocol CLI | Early access |

## Quick Start

```bash
# Install the CLI
npm install -g @the-cascade-protocol/cli

# Import FHIR data into a Pod
cascade pod init ./my-pod
cascade pod import ./my-pod patient.json

# Query by data type
cascade pod query ./my-pod --medications --conditions --lab-results

# Validate against the Cascade spec
cascade validate ./my-pod
```

## Key Principles

- **Local-first**: Zero network calls during operation. All data stays on your machine.
- **Patient-owned**: Data stored in portable Pods that users control.
- **Provenance-tracked**: Every record carries its origin — clinical, device, self-reported, or AI-generated.
- **Semantic**: Built on RDF/OWL with W3C PROV-O provenance. SPARQL-ready knowledge graphs.
- **Open**: Apache 2.0 (code) / CC-BY 4.0 (specifications). No proprietary dependencies.

## Links

- [cascadeprotocol.org](https://cascadeprotocol.org) — Documentation & getting started guides
- [CLI Guide](https://cascadeprotocol.org/docs/getting-started/cli/)
- [Security & Compliance](https://cascadeprotocol.org/docs/security/)

## License

Code repositories: [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
Specification & documentation: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

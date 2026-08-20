# Cascade Protocol

**A developer-first framework for structured, patient-owned health data.**

Cascade Protocol provides semantic vocabularies, serialization formats, and developer tools for building health applications where patients own and control their data. All processing is local-first — no data leaves the user's machine.

## Repositories

| Repository | Description | Released as |
|---|---|---|
| [spec](https://github.com/the-cascade-protocol/spec) | Ontology files, SHACL shapes, serialization specification, JSON-LD context | Versioned per vocabulary — see [`VOCAB_VERSIONS`](https://github.com/the-cascade-protocol/spec/blob/main/VOCAB_VERSIONS) |
| [conformance](https://github.com/the-cascade-protocol/conformance) | Conformance test fixtures, reference Patient Pod | Tagged releases |
| [cascade-cli](https://github.com/the-cascade-protocol/cascade-cli) | CLI for validating, converting, querying, and managing health data Pods | [`@the-cascade-protocol/cli`](https://www.npmjs.com/package/@the-cascade-protocol/cli) on npm |
| [sdk-typescript](https://github.com/the-cascade-protocol/sdk-typescript) | TypeScript SDK | [`@the-cascade-protocol/sdk`](https://www.npmjs.com/package/@the-cascade-protocol/sdk) on npm |
| [sdk-python](https://github.com/the-cascade-protocol/sdk-python) | Python SDK | [`cascade-protocol`](https://pypi.org/project/cascade-protocol/) on PyPI |
| [cascade-agent](https://github.com/the-cascade-protocol/cascade-agent) | Natural language interface for the Cascade Protocol CLI | [`@the-cascade-protocol/agent`](https://www.npmjs.com/package/@the-cascade-protocol/agent) on npm |
| [cascade-knowledge](https://github.com/the-cascade-protocol/cascade-knowledge) | Open clinical knowledge crosswalk: provenance-per-row mappings that turn isolated codes into meaning | In development |

Versions live in the package registries rather than in this table. This page is not
where anyone should learn a version, and a number written here goes stale the next
time anything ships. Four of the six had, one of them by sixteen minor releases.

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

## Contributing

Contributions are welcome, and the work is tracked in the open.

- **[All open issues across the organization](https://github.com/search?q=org%3Athe-cascade-protocol+is%3Aissue+is%3Aopen&type=issues)** — everything currently on the list, in every repository.
- **[Good first issues](https://github.com/search?q=org%3Athe-cascade-protocol+is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22&type=issues)** — scoped, self-contained, and a reasonable place to start.

Vocabulary changes are the one thing that is not a single-repository change: an
ontology is authored in [`spec`](https://github.com/the-cascade-protocol/spec) and
propagates from there to the SDKs, the CLI, the conformance suite and the
documentation site, in that order. If your change touches a vocabulary, read
[`spec/CONTRIBUTING.md`](https://github.com/the-cascade-protocol/spec/blob/main/CONTRIBUTING.md)
first — it carries the authoritative sequence.

Issues and pull requests are the right place for questions about the protocol
itself. Please do not include real patient data in either.

## Links

- [cascadeprotocol.org](https://cascadeprotocol.org) — Documentation & getting started guides
- [CLI Guide](https://cascadeprotocol.org/docs/getting-started/cli/)
- [Cascade Agent Guide](https://cascadeprotocol.org/docs/getting-started/agent/)
- [Security & Compliance](https://cascadeprotocol.org/docs/security/)

## License

Code repositories: [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0)
Specification & documentation: [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)

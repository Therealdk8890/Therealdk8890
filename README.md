# Danny

Building local-first systems for **verifiable AI, runtime authorization, and containment**.

## Security & AI infrastructure

**[WarrantKit](https://github.com/Therealdk8890/WarrantKit)** — runtime authorization, containment coordination, evidence, and lifecycle control for autonomous AI agents. WarrantKit keeps authority, enforcement, observation, and verification in separate trust boundaries and provides portable warrants, epoch fencing, evidence envelopes, and cryptographic attestation.

**[AgentContainment](https://github.com/Therealdk8890/AgentContainment)** — the security-critical runtime enforcement engine used by WarrantKit for external workload containment, kill/fencing, and runtime verification.

## Verifiable AI

**[dpk-gate-demo](https://github.com/Therealdk8890/dpk-gate-demo)** — fail the PR when the agent skips `verify`, even if the answer still looks right.

**[DProvenanceKitPython](https://github.com/Therealdk8890/DProvenanceKitPython)** — Python SDK + CLI for provenance and verification-oriented evidence.

**[dprovenancekit-action](https://github.com/Therealdk8890/dprovenancekit-action)** — GitHub Action for verification/provenance workflows.

**[DProvenanceKit](https://github.com/Therealdk8890/DProvenanceKit)** — Swift / on-device provenance and attestation.

Site: [dprovenance.dev](https://dprovenance.dev)

## Architecture

The work is organized around a simple principle:

**Authority should not depend on the agent. Evidence should not become authority. Verification should say exactly what was checked.**

The broader stack separates runtime enforcement, observation, provenance, claim/evidence verification, and external evidence correlation so each boundary can be independently inspected.

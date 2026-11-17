# Danny — Verifiable AI & Agent Security

Building **local-first security infrastructure for autonomous AI agents**: evidence you can inspect, authority you can revoke, and enforcement outside the agent's control.

## NobodySystems

**Independent control and verification infrastructure for autonomous AI agents.**

**NobodySystems** is the separately licensed **operational/control-plane layer** that brings three independently usable open-source engines together. The goal is to let teams govern what an AI agent is authorized to do, constrain the runtime that executes it, and verify the evidence afterward—without asking the agent to police itself.

| Layer | Project | Responsibility |
| --- | --- | --- |
| **Evidence** | **[DProvenanceKit](https://github.com/Therealdk8890/DProvenanceKit)** · [Python SDK](https://github.com/Therealdk8890/DProvenanceKitPython) | Local AI decision-path recording, regression testing, attestation, and offline verification of instrumented evidence. |
| **Authority** | **[WarrantKit](https://github.com/Therealdk8890/WarrantKit)** | Scoped, expiring, epoch-bound execution Warrants and guarded action authorization. |
| **Enforcement** | **[AgentContainment](https://github.com/Therealdk8890/AgentContainment)** | External workload controls, controller-issued execution leases, and Linux containment/verification primitives. |
| **Operations** | **NobodySystems** · private alpha | Coordinates local policies, guarded tool operations, operator workflows, and separately executed evidence verification. |

**The stack, at a glance**

```text
                    NobodySystems
            Operations / control plane
                   (private alpha)
                         |
         +---------------+---------------+
         |               |               |
     EVIDENCE        AUTHORITY       ENFORCEMENT
   DProvenanceKit    WarrantKit     AgentContainment
    record/verify   scope/fence     constrain/verify
```

Each engine has its **own trust boundary and independent Apache-2.0 release**. Evidence does not grant authority. A valid Warrant does not prove an action was enforced. A verified receipt does not establish that every underlying claim is true.

**Current scope:** NobodySystems is a **private alpha**, not a production SaaS or a general-purpose hostile-agent sandbox. The local controller, immutable policies, bounded guarded tools, operator interfaces, and evidence-bundle verification are implemented for constrained evaluations. Fleet orchestration, hosted editions, organization-wide policy workflows, and enterprise guarantees are **planned, not shipped**.

**Explore the stack:** [Public architecture, evaluation scope & OSS/commercial boundary](https://github.com/Therealdk8890/DProvenanceKit/blob/main/docs/NOBODYSYSTEMS.md) · [WarrantKit authority proof](https://github.com/Therealdk8890/WarrantKit/blob/main/docs/GETTING_STARTED.md) · [AgentContainment host-boundary proof](https://github.com/Therealdk8890/AgentContainment#reproduce-the-host-boundary-proof) · [Request a controlled private-alpha evaluation](mailto:danielpaulkissel@gmail.com?subject=NobodySystems%20private-alpha%20evaluation)

## More verifiable AI tooling

- **[dpk-gate-demo](https://github.com/Therealdk8890/dpk-gate-demo)** — a reproducible CI demonstration that catches a skipped verification step even when an agent's answer looks right.
- **[dprovenancekit-action](https://github.com/Therealdk8890/dprovenancekit-action)** — GitHub Action for provenance and decision-path regression gates.
- **[DProvenanceKitPython](https://github.com/Therealdk8890/DProvenanceKitPython)** — Python SDK and CLI for local provenance workflows.

**DProvenanceKit website:** [dprovenance.dev](https://dprovenance.dev)

---

*Design principle: authority must remain independent of the agent; enforcement must be independently checked; verification must state exactly what was proven.*

# DST

**Deterministic Signal Trading**

Built on the **Deterministic Simulation Thesis**.

DST finds possible trades. **DJZS audits** whether they are admissible. **Hermes runs the system**.

## Product role

DST is a deterministic decision layer for trading.

It is not:
- a generic charting platform
- an exchange
- a fully autonomous trading bot

It is:
- a signal engine
- an admissibility audit surface
- a runtime-orchestrated evidence pipeline

## Core architecture

- **DST** — Deterministic Signal Trading
- **DJZS** — deterministic audit authority
- **Hermes** — runtime, evidence ingress, workflow orchestration
- **DefiLlama** — core market-state input
- **Pyth** — price confidence and freshness verifier

## Recommended repo structure

```text
DST/
  README.md
  .gitignore
  apps/
    web/                # deterministic-signal.trading frontend
    api-server/         # DST API, signal engine, DJZS audit routes
  packages/
    trust/              # deterministic audit logic, taxonomy, scoring
    ui/                 # shared terminal-brutalist UI components
    types/              # canonical packet and schema types
  lib/
    api-spec/           # OpenAPI contracts
  docs/
    architecture.md
    hermes-runtime.md
    taxonomy.md
```

## Current priorities

1. Stabilize signal/audit snapshot integrity
2. Repair SHORT signal pipeline
3. Harden verification and provenance
4. Add clean Pyth Hermes v2 price-context support
5. Keep Hermes evidence-only and non-sovereign

## Core doctrine

**The market is uncertain. The decision process should not be.**

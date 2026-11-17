# 0001 - A separate SDK, API and authentication method per service

## Convention

Each service is reached through its own SDK, API and authentication method. Ocalt's documentation states the cost of this as "twenty SDKs" against one grammar. Source: https://ocalt.com/docs/oql.

## Counter-design

**OcaltQL**, a verb-first, pipeline-oriented, server-side execution language implemented in Rust, serving as the single control layer for a digital infrastructure. Source: https://ocalt.com/docs/oql.

- One grammar covers web, filesystem, media, CAD, mail, maps, machines, WebAssembly, HTTP and databases.
- Every statement starts with a verb. Every query compiles to an execution graph before an instruction runs.
- The language is deterministic, auditable and parallelisable by construction.
- `AND` runs branches in parallel, `AFTER` chains sequentially, `OR` falls back on failure.
- Databases are native to the namespace, not a wrapper around SQL.
- A query is one HTTP request to the runtime, however much the script chains inside it.

Projects written in it: [`ocaltql`](https://github.com/Ocalt/ocaltql). Specification: the OcaltQL tutorial at https://ql.ocalt.com.

## Evidence

Research note "OcaltQL Real Tough Benchmark", 21 Aug 2026, https://ocalt.com/updates/ocaltql-real-tough-benchmark.

- A production stress test on the public Starter endpoint: three tables and eighteen rows, joins, a bulk update, string pipelines, factorial arithmetic, a six-node parallel fabric and five nested conditional gates, invoked four times concurrently.
- Every phase passed.
- Runs of this class complete in roughly 460 ms end to end, including the network round trip and TLS. The note states that the dominant cost is the network, not the engine or storage.
- The note claims no per-phase breakdown.

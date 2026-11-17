# 0003 - The OcaltQL tutorial is the specification

Status: Accepted

## Context

The language was defined before it was implemented.

## Decision

The OcaltQL tutorial at https://ql.ocalt.com is the specification. Unless the tutorial has a syntax flaw, it is the source of truth and the runtime is built up to match it.

## Consequences

- The specification is the tutorial published at https://ql.ocalt.com. This repository links to it and does not copy it, so there is exactly one source of truth.
- A mismatch between the tutorial and the runtime is a runtime defect, unless the tutorial has a syntax flaw.

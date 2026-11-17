# 0002 - OcaltQL is the single control layer

Status: Accepted

## Context

Source: https://ocalt.com/docs/oql. Reaching each service through its own SDK, API and authentication method multiplies grammars.

## Decision

OcaltQL is the single control layer for the digital infrastructure of an Ocalt account. One grammar replaces many SDKs.

## Consequences

- Anything expressible in OcaltQL can be inspected, configured or orchestrated from a single surface.
- QueryAdmin operates on the same namespace and credentials model as the rest of Ocalt.
- A model that can write OcaltQL has to be taught one schema, not many.

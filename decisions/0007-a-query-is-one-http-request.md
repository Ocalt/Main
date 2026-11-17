# 0007 - A query is one HTTP request to the runtime

Status: Accepted

## Context

Source: https://ocalt.com/docs/oql. Pricing needs a unit that does not depend on how much a script chains inside it.

## Decision

A query is one HTTP request to the runtime, regardless of how much the script chains inside it. That is the unit pricing counts.

## Consequences

- Daily query allowances are counted in requests, per plan.
- Credits are drawn after the daily allowance is spent.

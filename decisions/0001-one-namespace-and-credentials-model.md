# 0001 - One namespace and credentials model for every Ocalt product

Status: Accepted

## Context

Source: https://ocalt.com and https://ocalt.com/about. The products are views onto one namespace, not separate silos.

## Decision

Every Ocalt product runs on the same namespace and credentials model. Data of every product lives in the one namespace of the account.

## Consequences

- Mail data sits alongside files, databases and system objects.
- There is one copy of every file and database.
- Access to data and access to machines are granted separately, per person.
- Every query is attributed and logged on one consolidated bill.

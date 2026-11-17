# 0005 - One credential, one job

Status: Accepted

## Context

Source: https://ocalt.com/security. A single credential that does everything cannot be replaced without breaking everything.

## Decision

Signing in, running scripts and connecting devices each use their own credential: the account password, the OcaltQL API key and the Ocalt Client key.

## Consequences

- Rotating one credential never affects the others.
- The API key carries no sign-in rights.
- A business member acts through a key that belongs to that membership alone, and it stops working when the membership is revoked.
- Failures of API and Client keys are limited separately from sign-in and can never lock an account.

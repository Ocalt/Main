# 0004 - Connected machines connect outbound only

Status: Accepted

## Context

Source: https://ocalt.com/security. Machines reachable through inbound ports or a VPN widen what an attacker can reach.

## Decision

A connected machine dials out to Ocalt and holds the connection itself. Nothing on it listens on a public interface.

## Consequences

- A machine is bound to one account and acts only for that account.
- The OcaltQL Client's own settings page is reachable only from the machine it runs on.
- A lost machine is cut off by rotating one key.

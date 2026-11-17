# 0006 - Namespaces are isolated by separation, not filtering

Status: Accepted

## Context

Source: https://ocalt.com/security. A blocklist has to anticipate every route to another account.

## Decision

Every namespace has its own network, with its own loopback, address range and name resolution containing only that account's things. Another namespace is not blocked; it is not attached at all.

## Consequences

- There is no route to block.
- 127.0.0.1 inside a namespace is that namespace's own loopback, and nothing of Ocalt's listens on it.
- Nothing in a namespace is public unless it is shared, and a shared link is created explicitly for one file.

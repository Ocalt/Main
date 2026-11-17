# 0003 - Per-product silos of data and identity

## Convention

Each product keeps its own silo of data and identity. Ocalt's About page states its alternative as applications that are "views onto the same namespace rather than a separate silo". Source: https://ocalt.com/about.

## Counter-design

**One namespace and one credentials model for every Ocalt product.** Sources: https://ocalt.com and https://ocalt.com/security.

- Every Ocalt product runs on the same namespace and credentials model.
- Mail data sits natively alongside files, databases and system objects.
- One shared namespace gives everyone the same files, databases and registered machines, with only ever one copy.
- Access to data and access to machines are granted separately, per person.
- Every query is attributed and logged on one consolidated bill.
- Isolation is by separation, not by filtering. Every namespace has its own network, with its own loopback, address range and name resolution containing only that account's things. Another namespace is not blocked; it is not attached at all.
- Signing in, running scripts and connecting devices each use their own credential, so replacing one never breaks the others.

## Evidence

The behaviour is documented on the Security Model page, https://ocalt.com/security, which states that it describes how the platform behaves today. The same page lists what has not yet been published: an independent penetration test, a compliance certification, a service-level agreement, a disaster-recovery and incident-response procedure, and a statement on encryption at rest.

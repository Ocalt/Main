# Review standard

## What a reviewer checks

1. The change against the specification, line by line.
2. Every assumption. An unflagged assumption is a defect.
3. Scope. Anything not asked for is a defect unless named as an addition.
4. Convention smuggled in. A design chosen because it is standard elsewhere is a defect.
5. Leaked material: hostnames, IP addresses, paths, configuration, credentials, backup or scratch files.

## How a reviewer writes

- State the defect, the evidence and the required correction.
- Correctness comes before encouragement. Praise is not required and is not a substitute for a finding.
- A concern about an instruction is raised separately from the implementation and does not block it.

## Outcomes

- **Accepted**: every check passes.
- **Changes required**: at least one defect. Each is listed.
- **Blocked**: the specification is silent or contradictory. The question goes to the author.

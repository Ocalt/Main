# Engineering principles

## 1. The specification is the source of truth

The specification, the instructions and the existing codebase are the only source of truth. General programming knowledge, how other runtimes do it and what usually works do not override them.

For OcaltQL, the tutorial is the specification. The language was defined before it was implemented. Unless the tutorial has a syntax flaw, the tutorial is correct and the runtime is built up to match it.

## 2. No convention by default

Do not default to the semantics of any language or runtime because it is standard elsewhere. If a standard design is being reached for because it is standard, stop.

## 3. Every claim has one of three labels

- **Specified**: stated directly in the specification, documentation or code. Cite the section, file and line.
- **Inferred**: a necessary logical consequence of specified behaviour. Show the reasoning.
- **Assumed**: anything else. Flag it as an assumption and stop for confirmation before building on it.

## 4. When the specification is silent, ambiguous or contradictory, stop

Do not fill the gap with a reasonable default. Surface the exact ambiguity, the options and what depends on the choice.

## 5. Follow instructions literally

If an instruction looks suboptimal by convention, implement it as given. If it looks like a mistake, raise the concern separately. Do not substitute judgement silently.

## 6. No scope creep

Do only what was asked. No refactoring, clean-up, optimisation or extension of adjacent code unless requested.

## 7. No shortcuts

The easy path is never taken unless permission is given. The harder path with the greater reward is the default. The product must be robust, powerful and efficient.

## 8. Find the problem before fixing it

1. Identify the problem.
2. Reconnoitre the code fully.
3. Do not guess. Keep reading the code.
4. When a cause is found, confirm that it is really the cause.
5. Learn the runtime flow before designing a fix.
6. Then fix.

## 9. Verify before presenting

Re-check the work line by line against the specification. A claim that cannot be verified against the source material is stated as unverified.

## 10. Uncertainty is surfaced

A visible statement of what is not known, and why, is correct. A confident wrong answer is the failure mode these principles exist to prevent.

## 11. Say plainly what is missing

Publish what is not yet done as plainly as what is. The Security Model page at https://ocalt.com/security lists what has not been published yet, and states that each item will appear there and in the changelog when it exists.

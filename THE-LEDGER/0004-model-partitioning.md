# 0004 - Sharing a model between machines by cutting it into layers

## Convention

The usual way to share a model between machines is to cut it into layers and pass the work down a chain. Source: https://ocalt.com/updates/olde-one-model-many-machines.

## Evidence

Research note "Olde: one model, held by every machine you own", 12 Nov 2026, https://ocalt.com/updates/olde-one-model-many-machines.

- Machines on Ocalt talk through DIRECTIVE, and one exchange costs about half a second. A chain of one hundred machines holding one layer each would spend more than a minute on a single pass.
- In a chain, the number of machines in a row sets the speed, so adding machines makes it slower. Rounds per pass are set by how much model one stage holds, not by how many machines exist.

## Counter-design

**Olde.** Every machine holds the whole model, at whatever resolution it has room for, written in its own basis. Each copy is a **view**.

- A view is made by turning the model's residual stream with an orthogonal matrix drawn from the view's own seed, then quantising. At full precision the turned model computes the same as the original.
- Views with different seeds make rounding mistakes in different directions, so their errors partly cancel when the answers are fused.
- Each machine answers about the same run of tokens with its likeliest next tokens and their log probabilities. The answers are fused token by token as a product of experts, weighted by precision. Machines never talk to each other. There is one round per token however many machines take part.
- A view is encoded straight from the model's published files over HTTP range requests, so the machine making a view needs room only for the view itself.

## Measurements published so far

These are first measurements, not a benchmark suite.

- A 0.5B instruct model: a full-precision view in a rotated basis reproduced the reference predictions to within rounding.
- Holographic mode, a 7B code model across the internet, two machines each holding one 4-bit view: 120 tokens in 80 seconds, 1.5 tokens per second, with the views choosing the same token 93 percent of the time.
- Holographic Local, a 7B model on two machines with no graphics cards: 92 tokens per second, views agreeing on 96 percent of tokens.
- Local Split, a 1.5B model on two machines with no graphics cards: 65 to 70 tokens per second.

## Open

- Whether fusion keeps paying as the number of low-resolution views grows.
- Behaviour below roughly one and a half bits per view.
- Speculation, where a small drafter proposes several tokens and one fused pass confirms them. Designed, not built.
- Breadth. The encoder has been run on one model family.

Product: Olde, https://olde.ocalt.com. Released 12 Nov 2026 per https://ocalt.com/changelog.

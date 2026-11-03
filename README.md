# AOP Landscape

`aop-landscape` is the single authority for how the Agentic Operating Procedure differs from what already exists, and for the standards landscape the programme builds against.

| Field | Value |
|---|---|
| Authority | External positioning, prior art, standards grounding |
| Tier | Concept |
| Landing wave | 1 |
| Version | 0.1.0 |
| Status | Stable |
| Licence | MIT |

## Why this repository exists

The hardest obstacle to the concept becoming authoritative is not building it. It is establishing, in public and with citations, that it is not a relabelling of something that already exists.

A discipline that cannot state its difference credibly cannot hold authority. Every claim in this repository is stated so that a reader can check it, and every comparison names what the other thing does well. A comparison that only lists weaknesses is marketing, and it is refuted by the first practitioner who knows the neighbouring tool.

## What this repository owns

- The claim-by-claim differentiation table: what AOP states that each adjacent discipline does not, and what each of them states that AOP does not.
- The prior-art survey: the systems, patterns and published work that a reader will assume AOP duplicates.
- The standards landscape: the open standards the programme cites and aligns with, with the exact part of each that is used.

## What this repository does not own

- The concept itself. That is `aop-foundations`.
- The normative model. That is `aop-spec`.
- The implementation of anything compared here. That is `aop-toolkit` and `aop-reference-harness`.

## How a claim is made here

Every differentiation row follows one shape:

1. The adjacent discipline, named specifically.
2. What it does well, stated without qualification.
3. What it does not state.
4. What AOP states instead.
5. The citation, where the claim is externally checkable.

Rows without a checkable citation are marked as programme reasoning rather than evidence, and are labelled as such. That label is not a weakness; it is the difference between an opinion and a claim.

## Documents

| Document | What it settles |
|---|---|
| [`docs/aop-differentiation-landscape-scope.md`](docs/aop-differentiation-landscape-scope.md) | The claim-by-claim differentiation table against every adjacent discipline |
| [`docs/aop-prior-art-survey-landscape-scope.md`](docs/aop-prior-art-survey-landscape-scope.md) | The prior-art survey: what a reader will assume AOP duplicates, and where each one stops |
| [`docs/aop-standards-landscape-landscape-scope.md`](docs/aop-standards-landscape-landscape-scope.md) | The standards landscape: which open standards are cited, and for exactly what |

## Repository layout

```
aop-landscape/
  README.md            # this file
  CHANGELOG.md         # release notes
  CODEOWNERS           # ownership
  LICENSE              # MIT
  docs/                # the differentiation table, the prior-art survey, the standards landscape
```

## Contributing

The contribution guide, the code of conduct, and the issue and pull-request templates live in the organisation profile repository, `.github`. A correction to a differentiation claim is a change request against `aop-governance` when it alters the programme's external positioning, and a direct pull request here when it corrects a citation.

## Licence

MIT. See `LICENSE`.

# AOP Standards Landscape: Agentic Operating Engineering, Agentic Operating Procedure, Agent Skill, Domain Agent Harness, Agent, Agentic Operations Levels (Landscape Scope)

_The open standards the programme cites, and the exact part of each that is used. Sourcing is restricted to ITU-T, ETSI, ISO and IEC, and NIST._

| Field | Value |
|---|---|
| Version | 0.1.0 |
| Status | Stable |
| Scope | Landscape Scope |
| Owner | Emmanuel A. Otchere |

## 1. The sourcing rule

Standards are cited only from open, published sources: ITU-T recommendations, ETSI technical specifications, ISO and IEC standards, and NIST publications and frameworks. Where a domain specification exists only behind a paywall or under a restricted disclosure programme, the programme does not cite it, and does not reproduce its terminology.

This is a hard rule (ADR-0007), not a preference. A discipline that builds on closed specifications cannot be independently adopted, and it cannot be verified by the readers it claims to serve.

## 2. Standards in use

| Source | What the programme takes from it | Where it is used |
|---|---|---|
| ITU-T M.3050.x series | The structure of a shared operational information model: how entities of an operational domain are described so that separate systems can exchange them | The naming and structure of the Context Graph of Work entities in `aop-context-graph` |
| ETSI technical specifications on management and orchestration interfaces | The separation of management intent, configuration state and execution notification, and the resource model those interfaces share | The observation and control surfaces in `aop-context-graph` and `aop-reference-harness` |
| ISO/IEC 42001 | The shape of an AI management system: organisational context, scope, risk and impact assessment, treatment, and monitoring | The programme-level governance framing; the assurance surfaces in `aop-conformance` |
| ISO/IEC 23894 | Risk taxonomy and risk management methodology for AI systems | The risk axes underlying the decision-rights ladder in `aop-spec` |
| NIST AI Risk Management Framework | The four-function structure of govern, map, measure, manage, and the separation of measurement from treatment | The evaluation design in `aop-evaluation`; the assurance surfaces in `aop-conformance` |
| ISO/IEC 11179 metadata registry | Identifier and registration conventions for metadata elements, so that a published term carries a stable identifier | The glossary and identifier scheme in `aop-foundations` and `aop-spec` |
| W3C PROV data model | Provenance as a first-class entity with generation, attribution, and derivation relations | The provenance chain from a published AOP back to its observed cases, in `aop-registry` |
| OpenTelemetry | Consistent trace and metric semantics for observability data | The context snapshot and case record fields in `aop-reference-harness` |

## 3. What is deliberately not claimed

- **No conformance claim against any standard.** The programme does not claim conformance to ISO/IEC 42001, NIST AI RMF, or any other management-system standard. Those frameworks describe organisational management; AOP describes an operational specification. The relationship is alignment, and the alignment is stated in this table so that a reader can check the direction of the mapping.
- **No certification of third-party systems.** A statement in a landscape document is a statement about the programme's own work.
- **No proprietary terminology.** Terms are defined in `aop-foundations` with stable identifiers, and the definitions are the programme's own.

## 4. The direction of mapping

The mapping runs from AOP to these standards, never from them into AOP. That is, the programme consumes open standards and does not fork them. Where AOP needs an entity that a standard already defines, the standard's definition is referenced. Where AOP needs an entity that no standard defines, it defines its own, and says so.

## 5. What the standards do not cover

No cited standard specifies:

- A procedure compiled from observed work with a provenance chain back to its source cases.
- A per-decision authority boundary for a delegated actor, with an enforcement point outside the actor's own context.
- An evidence obligation stated as part of the operating specification.
- The maturity path from human-operated through assisted to agentic operations.

These four gaps are where the programme's own contribution sits, and they are the gaps `aop-spec` exists to close.

## 6. Related documents

- [`aop-differentiation-landscape-scope.md`](aop-differentiation-landscape-scope.md): the claim-by-claim differentiation table.
- [`aop-prior-art-survey-landscape-scope.md`](aop-prior-art-survey-landscape-scope.md): the prior-art survey.

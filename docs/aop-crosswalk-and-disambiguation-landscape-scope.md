# AOP Crosswalks and Disambiguation: Positioning Against Standards, Frameworks, Regulations and Name Collisions (Landscape Scope)

Informative. This document carries two obligations: the crosswalks to neighbouring standards, frameworks and regulations, each with a verdict and its reasoning; and the disambiguation of the name collisions the acronym AOP carries in neighbouring fields. It also evidences the positioning claim the programme makes. Per ADR-0007 the sourcing cites ITU-T M.3050.x, ETSI TS, ISO/IEC and NIST only; regulations and practitioner guidance named here are obligations being mapped, not sources of normative text, and their rows are anchored on the ISO/IEC and NIST material already in scope.

## 1. Name disambiguation

Three uses of AOP, or near-acronym, collide with this programme's Agentic Operating Procedure. None is a conflict of substance; all three are worth stating so a reader arriving from either field is oriented in one paragraph.

| Claim to the name | What it is | Artefact class | Relationship to this programme |
|---|---|---|---|
| Agent-oriented programming (Shoham, 1993; the AGENT0 language) | A programming paradigm: agents as computational systems characterised by mental state, with a specialised agent language | A language and paradigm for building agents | Acronym collision only. An agent-oriented program is an implementation artefact; an Agentic Operating Procedure is an operational specification that governs implementations of any kind. The programme's agent layer is deliberately the least authoritative and most replaceable part of the estate, which inverts the AOP paradigm's centre of gravity |
| Agent Operating Procedure (Decagon; AI customer-experience agents) | A versioned playbook a commercial AI agent product executes; publicly described as the agent equivalent of an SOP, increasingly edited by the product's own automation | A product-internal procedure artefact | The nearest neighbour in spirit, and the clearest contrast in mechanism. Decagon's AOPs are authored natural-language instructions compiled into a product's structured logic; this programme's AOPs are compiled from observed work, carry per-rule provenance, and are governed by a guardrail outside the model context with published conformance and evaluation surfaces. This assessment is the programme's own reading of publicly available material |
| Agentic Operating Playbook (Skan; as named in the external review of 2026-11-04) | Reported process-intelligence playbook usage; not independently verified at filing | Unverified | To be assessed when public material is available. Listed here so the collision is at least named |

The estate's own short form, AOP, is retained. The glossary carries the stable identifier, and this document is the disambiguation surface: any external text that says AOP is resolved by artefact class, not by initials.

## 2. Crosswalks

Each row gives the verdict for the neighbouring framework against the AOP surface: equivalent, partial, or absent, with the reasoning. Where the reasoning is the programme's own argument rather than a demonstrated measurement, the row says so. Where a row cites regulation or practitioner guidance, the anchor is the ISO/IEC or NIST material already in the standards landscape, per the sourcing rule above.

| Framework or obligation | Verdict | What they cover that AOP also covers | What AOP states that they do not | Reasoning status |
|---|---|---|---|---|
| Policy engines and PDP/PEP models | Partial | The enforcement-point separation: the check sits outside the evaluated entity's control. The guardrail is recognisably a PDP/PEP pair | The full operational specification: intent, per-decision rights, provenance-bounded rules, assurance obligations. A policy engine evaluates a decision; it does not state what the work is, where the rules came from, or what evidence closes the case | Programme's own argument, supported by the differentiation document's boundary analysis |
| NIST AI Risk Management Framework | Partial | The four functions map onto the estate: govern (aop-governance), map (aop-foundations, aop-landscape), measure (aop-evaluation), manage (aop-adoption) | Machine-executable, per-case enforcement. The RMF is organisational and periodic; AOP obligations bind at run time, per case, with evidence | Programme's own argument; the mapping direction is already stated in the standards landscape |
| ISO/IEC 42001 (AI management systems) | Partial | Management-system shape: scope, risk assessment, treatment, monitoring map to the programme's governance and assurance tiers | The operational specification an AMS would govern. ISO/IEC 42001 says an organisation manages AI; AOP says how one procedure's delegated execution is specified and bounded | Programme's own argument |
| EU AI Act human-oversight obligations (mapped via the ISO/IEC 42001 and NIST RMF rows above) | Partial | The oversee mechanism: defined thresholds, evidence bundles for approvers, oversight metrics (block 2 of CR-009), the maturity model's human-accountability rule | Legal-effect claims. The estate cites no law and claims no conformance to any regulation; the mapping states where an adopter's own regulatory answer would draw on AOP artefacts | Programme's own argument, informative only, anchored on the ISO/IEC and NIST rows |
| OWASP agentic-security guidance (mapped via the NIST RMF measure and manage rows above) | Partial | The threat surface: injection into the procedure, authority escalation, credential misuse are the estate's T1 to T7, each with a testable mitigation in the conformance profiles | Guidance status. OWASP guidance is advisory checklists; AOP carries the mitigations as enforced clauses with must-fail fixtures, which is a stronger and narrower claim | Programme's own argument |
| Agent-authorization protocols (AAP, ATP, AIP; named in the external review, not independently verified at filing) | To be assessed | Not assessed: no public material was examined at filing | Not assessed | Listed so the gap is visible; assessment is a CR-009-9 follow-up |

## 3. The evidence behind the positioning claim

The programme's positioning statement says AOP is the specification layer that sits above the neighbouring artefact classes and below none of them. The programme owner has directed that this claim be carried by evidence, not softened. The evidence is of two kinds, and the distinction matters:

Demonstrated by artefacts:

- The complete specification surface exists and is gated: the normative model with stable clause identifiers, the machine-readable schema, the reference validator, the conformance profiles, the evaluation method, and the worked exemplar whose reproduction gate passes end to end.
- The enforcement claim (authority outside the executor's context) is tested behaviourally: poisoned-context checks, credential scoping checks, tamper-detection checks, all passing and certified against the reference harness.

Argued, not measured:

- That no neighbouring artefact class covers the same surface. That claim rests on the crosswalk verdicts above, and every row that supports it is marked as the programme's own argument. A reader can check the argument; the programme does not claim to have measured every neighbouring product.
- That the difference matters in practice. That claim awaits the Demonstrated tier: the independent reproduction and the non-steward pilot that CR-009-8 organises.

The claim is therefore retained, with its evidence stated and its argumentative parts marked. This is the middle path the review asked for: neither an unevidenced slogan nor a softened retreat.

## 4. Related documents

The prior-art survey carries the neighbouring artefact classes by family (procedure systems, workflow, policy, SRE, safety, agentic tooling). The differentiation document carries the claim-by-claim comparison against those families. The standards landscape carries the ISO/IEC, NIST, ITU-T and ETSI mappings and the no-conformance-claim rule. This document adds only what those three do not carry: the name collisions, the verdict-form crosswalks, and the evidence statement for the positioning claim.

# AOP Differentiation: Agentic Operating Engineering, Agentic Operating Procedure, Agent Skill, Domain Agent Harness, Agent, Agentic Operations Levels (Landscape Scope)

_Claim by claim: what the Agentic Operating Procedure states that each adjacent discipline does not, and what each of them states that AOP does not._

| Field | Value |
|---|---|
| Version | 0.1.0 |
| Status | Stable |
| Scope | Landscape Scope |
| Owner | Emmanuel A. Otchere |

## 1. How to read this table

Each row has four parts: what the adjacent discipline does well, what it does not state, what AOP states instead, and how the claim is checkable.

A row marked **Programme reasoning** is the programme's own argument rather than an externally checkable fact. Those rows are where the programme is weakest and where independent scrutiny is most welcome. A row marked **Externally checkable** can be confirmed by a reader without trusting the programme.

## 2. Workflow engines and durable execution

Representative systems: Temporal, Apache Airflow, Argo Workflows, Prefect, Dagster, Conductor, Netflix Conductor.

**What they do well.** Durable execution with automatic resumption after failure, first-class retry semantics, and a clear separation between workflow definition and task implementation. Temporal's deterministic replay model is a genuine engineering achievement, and Airflow's data-pipeline heritage has made scheduled batch orchestration unremarkable for the better part of a decade.

**What they do not state.** They do not state who is permitted to decide what inside a workflow. Task code is trusted code, and the workflow definition says what happens, not what an actor inside it may decide. There is no per-decision authority boundary, no requirement to record which rule applied, and no evidence obligation beyond application logs.

**What AOP states instead.** Every decision the execution actor may take alone is written down, separately from what happens. The authority check is performed outside the model context, so the actor cannot influence the outcome of the check that governs it. Every case carries an append-only record of the rule applied, the decision, the approver where relevant, and the outcome.

**Where the line is.** A workflow engine is the right tool for executing a flow. An AOP is the right tool for deciding who may act, on what authority, with what evidence. They compose: the AOP is the specification, the engine is one possible executor. The programme does not claim to replace durable execution, and the reference harness is deliberately built on a proven engine rather than inventing one.

## 3. Business process management

Representative systems and standards: BPMN 2.0 and the BPMN engines that implement it, Business Process Model and Notation tooling, and the enterprise suites built on it.

**What they do well.** A mature, expressive notation for modelled processes, with exchange formats, gateways, events, and a long record of real-world adoption in regulated enterprises. BPMN remains the most capable public notation for expressing a process with decision points and exception paths.

**What they do not state.** BPMN is a notation for a modelled process. The model states intended structure. It does not state an authority boundary for a non-human actor, nor an evidence obligation, nor a source-of-truth relationship between the model and what actually happens. The model is drawn, and drawings drift.

**What AOP states instead.** The procedure is compiled from observed work rather than drawn from intent, and carries provenance back to the cases it was compiled from. It is network-native by construction: variants with observed frequencies, decision points with their rules and thresholds, exception edges, and rework loops. The corridor is the rare case, not the normal one.

**Where the line is.** BPMN is a notation; AOP is an artefact class that happens to need a notation. The reference specification uses a machine-readable schema, and a BPMN export is a mapping in `aop-toolkit`, not a competing definition.

## 4. Policy engines and authorization

Representative systems: Open Policy Agent with Rego, Cedar, XACML, and cloud-native policy controllers built on them.

**What they do well.** Decoupling the decision from the decision-maker. Policies are written in a restricted language, evaluated against a structured input, and returned as a decision with an explanation. Cedar's formal verification properties and OPA's adoption inside Kubernetes controllers are substantial, and the fast-decision design is well understood.

**What they do not state.** A policy engine evaluates a decision that is put to it. It does not decide what the work is, who the actor is in relation to that work, what the actor was trying to achieve, what evidence is required to show the outcome was right, or how the work evolves when the policy set is complete but the situation is not covered.

**What AOP states instead.** The full operational specification: intent, context, constraints, authority, capabilities, coordination, control, and assurance. The policy engine becomes the mechanism that evaluates one part of it, the authority check, and it is evaluated outside the model context so the actor cannot influence the outcome of the check that governs it.

**Where the line is.** This is the sharpest boundary in the estate. An AOP is not a policy set. A policy set inside an AOP is a constraint expression evaluated by a policy engine, and the AOP states what the outcome of that evaluation obliges the actor to do.

## 5. Runbook and playbook automation

Representative systems: Rundeck, StackStorm, Packer, Ansible Automation Platform, and the runbook sections of general-purpose operations platforms.

**What they do well.** Turning an operator's knowledge into an executable sequence, with parameterisation, secret handling, and audit logs. For a linear procedure with a well-understood trigger, this is exactly the right tool, and it is a fraction of the cost of an agentic system.

**What they do not state.** The runbook assumes the operator chooses when to run it and interprets the result. There is no delegated decision authority, no authority boundary that the execution actor must respect at run time, and no requirement that the runbook know what the work looked like when it was written.

**What AOP states instead.** The procedure is a measurement of observed work rather than a hypothesis about it, and it states the authority boundary, the escalation threshold, and the evidence obligation. A runbook can be compiled from an AOP; it cannot be the AOP.

**Where the line is.** Runbooks are the natural output of the SOP-to-AOP translation when the work is linear and low risk. That is a legitimate and common case, and the programme does not treat it as a failure of the concept.

## 6. Agent orchestration frameworks

Representative systems: the widely used agent orchestration and tool-calling frameworks, and the model-provider agent stacks.

**What they do well.** Rapid construction of tool-using agents, with loops, memory, planning scaffolds and model integrations that would take a team months to assemble from primitives. They made agentic behaviour accessible, and the field needed that.

**What they do not state.** Their unit of composition is the agent and the tool call. There is no artefact that states the operational intent, the decision rights, the assurance obligations, and the evidence required. The instructions given to the model are not a specification: they are a context window, they admit multiple readings, and they are not versioned against a governance process.

**What AOP states instead.** A versioned operating standard with eight mandatory dimensions, a decision-rights model, and an evidence requirement, compiled from observed work with provenance, executed inside a harness that is itself the top-level AOP for its domain.

**Where the line is.** The framework is an implementation concern and belongs in `aop-toolkit` or `aop-reference-harness`. Nothing in the AOP model requires a particular orchestration framework, model, or tool-calling convention.

## 7. Orchestration and infrastructure platforms

Representative systems: Kubernetes, service mesh controllers, and general job orchestrators.

**What they do well.** Scheduling, placement, health, scaling and declarative desired state at infrastructure scale. The reconciliation loop is one of the best-engineered patterns in the discipline, and Kubernetes controllers are a mature answer to a question the AOP programme does not need to answer.

**What they do not state.** These systems reconcile declared desired state against observed state. They do not state, for the workload they run, what outcome is intended, which decisions the running actor may take, or what evidence demonstrates the outcome was achieved. A container that is healthy has not thereby accomplished anything.

**What AOP states instead.** The AOP states the outcome and the conditions; the platform reconciles infrastructure toward the desired state the AOP implies. The AOP's evidence model is the source of the drift signal that the platform's reconciliation cannot provide, because it measures work rather than resources.

**Where the line is.** The AOP programme consumes orchestration. It does not specify infrastructure.

## 8. Site reliability engineering and operational management

Representative sources: the Google site reliability engineering literature, the error-budget method, and the incident-command tradition.

**What they do well.** Treating operational work as an engineering discipline with explicit objectives, explicit error budgets, blameless review, and a well-developed escalation and incident-command practice. Much of the terminology this programme borrows for authority and escalation comes from that tradition.

**What they do not state.** The literature describes how humans should organize operational work. It does not specify an artefact that a non-human actor executes against, and it does not address delegation of decision rights to an automated actor as a design object.

**What AOP states instead.** The agentic case of the same discipline: a specified delegation of authority, with evidence obligations, an escalation boundary, and a maturity path from human-operated through assisted to agentic to autonomous.

**Where the line is.** This is the closest adjacency, and it is an extension rather than a rival. The SRE literature is where the operational objectives, the error-budget framing, and the escalation discipline come from. The AOP adds the delegated actor and the artefact that governs it.

## 9. The structural difference, summarised

| | Adjacent disciplines | AOP |
|---|---|---|
| Source of truth | Authored, or drawn, or configured | Compiled from observed work, with provenance |
| Structure | Flow, graph, or policy set | Network of variants, decision points, exception edges, rework loops |
| Decision authority | Implied by code or configuration, or delegated wholesale | Stated explicitly, per decision, with a boundary |
| Verification | Application logs, or a human noticing | An append-only case record per case, as a specified obligation |
| Coverage | As good as the authored artefact | Measured, because variants carry observed frequencies |
| Exception | A branch, a policy, or an incident | A first-class edge with its own rule and evidence |

## 10. The claims that are programme reasoning

These are stated openly because they are the claims most likely to be wrong.

1. **That the delegated actor needs a new artefact class.** An alternative position is that existing orchestration plus policy plus observability is sufficient, and that AOP is a naming convenience. The programme's answer is the evidence obligation: without a specified evidence requirement per case, a delegated actor's correctness is not checkable, and every claim about delegated execution reduces to an anecdote.
2. **That compilation from observation is tractable.** The observe, model, compile pipeline is the programme's largest engineering risk. A competing approach derives procedures from documented intent with a smaller evidence base. If compilation proves impractical in a domain, the AOP for that domain will be authored rather than compiled, and the programme's claim about provenance will not hold there.
3. **That the six-level hierarchy is the right decomposition.** The hierarchy is the programme's own framing, taken from the programme owner's stated conceptual spine. It has not been independently validated against other decompositions of the same problem space.

## 11. Related documents

- [`aop-prior-art-survey-landscape-scope.md`](aop-prior-art-survey-landscape-scope.md): the prior-art survey.
- [`aop-standards-landscape-landscape-scope.md`](aop-standards-landscape-landscape-scope.md): the standards landscape.

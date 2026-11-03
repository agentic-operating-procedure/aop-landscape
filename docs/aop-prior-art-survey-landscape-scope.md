# AOP Prior Art Survey: Agentic Operating Engineering, Agentic Operating Procedure, Agent Skill, Domain Agent Harness, Agent, Agentic Operations Levels (Landscape Scope)

_The systems, patterns and published work a reader will assume the Agentic Operating Procedure duplicates, and where each one stops._

| Field | Value |
|---|---|
| Version | 0.1.0 |
| Status | Stable |
| Scope | Landscape Scope |
| Owner | Emmanuel A. Otchere |

## 1. The purpose of a prior-art survey

Every new discipline is initially received as a rename. The survey exists so that the rename accusation can be answered specifically rather than rhetorically: by naming what each prior system does, where it stops, and which part of the AOP would have to be duplicated to cover the gap.

A survey that only finds differences is dishonest. Each entry below states the prior work at its strongest.

## 2. Operational procedure and work instruction systems

| Prior work | What it is | Where it stops |
|---|---|---|
| Standard operating procedures | Authored, reviewed, versioned procedure documents | Assume the executor follows the document; no delegated authority concept; linear structure |
| Work instructions | Task-level instructions attached to a job | Task granularity only; no intent, no decision rights, no evidence |
| Standard operating manuals | Equipment-specific operating procedure | Equipment scope; no operational governance layer |
| Quality management systems | Documented process with audit and corrective action | Audit of human process; no executable specification, no agent delegation |
| Runbooks and operational playbooks | Executable or semi-executable operational sequences | Assume a human selects and interprets; no stated authority boundary |
| Job aids and knowledge bases | Searchable operational knowledge | Retrieval only; no structure, no authority, no evidence obligation |

## 3. Workflow and orchestration

| Prior work | What it is | Where it stops |
|---|---|---|
| Temporal | Durable execution with deterministic replay and explicit retry semantics | Defines what happens; does not define who may decide what, or what evidence proves the outcome |
| Apache Airflow | Data-pipeline orchestration as code, with a strong scheduling and lineage model | Task graph; no delegated decision authority; lineage is of data, not of decisions |
| Argo Workflows | Kubernetes-native workflow specification and execution | Container orchestration of a graph; the actor inside a step is trusted code |
| Prefect, Dagster, Conductor | Alternative orchestration engines with different execution and scheduling models | Same boundary: flow semantics without an authority model |
| BPMN and its engines | Notation and engines for modelled processes with gateways, events and exception paths | Modelled intent; no source-of-truth relationship to observed work; no evidence obligation |

## 4. Policy and authorization

| Prior work | What it is | Where it stops |
|---|---|---|
| Open Policy Agent and Rego | General-purpose policy evaluation with a restricted language and explainable results | Evaluates a decision put to it; does not supply intent, actor role, or evidence obligations |
| Cedar | Formally verified authorization policy language with a rich schema and validation | Same boundary, with stronger formal guarantees on the decision it evaluates |
| XACML | Long-standing XML authorization standard with a policy and context model | Requests and attributes only; no operational lifecycle, no evidence model |
| Access-control and capability models | Subject, object, action, and context authorization | Authorization only; says nothing about operational intent or outcome verification |
| Policy-as-code in platform controllers | Policy enforced as a gate on infrastructure change | Guard at a resource boundary; the operational goal behind the change is unstated |

## 5. Site reliability and incident practice

| Prior work | What it is | Where it stops |
|---|---|---|
| Google site reliability engineering literature | Operational work as engineering, with error budgets, blameless review, and toils | Describes human organization; no artefact a delegated actor executes against |
| Incident command and escalation practice | Role assignment, severity, communication, and handover | Human-led; the authority to decide is assumed rather than specified |
| On-call and runbook practice | Rotations, escalation ladders, and documented remedies | Assumes a human reasons about the situation before acting |
| Change management and CAB practice | Approved change with risk assessment and rollback | Governs human-approved change; no continuously operating delegation |

## 6. Safety, governance and assurance

| Prior work | What it is | Where it stops |
|---|---|---|
| Standards for AI risk management and management systems | Organizational risk frameworks, inventories, impact assessment, and treatment plans | Program-level governance; no executable operational specification |
| Security and access-control engineering | Least privilege, separation of duties, and audit | Protect the system; do not specify the operation or the actor's decision rights |
| Formal methods and model checking | Proof of properties of specified systems | Requires the specification to exist first; the specification is the hard part here |
| Observability and telemetry platforms | Metrics, logs, and traces from running systems | Measure the system; do not state what evidence is required for a given operation |
| Data lineage and provenance tracking | Where data came from | Provenance of observations; not provenance of a published procedure back to the cases it was compiled from |

## 7. Agentic tooling and research

| Prior work | What it is | Where it stops |
|---|---|---|
| Agent orchestration tooling and model-provider agent stacks | Tool-using agents with loops, memory, and planning scaffolds | Composition unit is the agent and the tool call; no operating standard, no authority boundary |
| Multi-agent coordination frameworks | Role assignment, message passing, and delegation topologies | Coordination without a governing specification of authority |
| Planning and behaviour-tree literature | Search and policy structures for action selection | Selection algorithms; no specification of what the actor is permitted to do |
| Agent safety and alignment research | Training-time and evaluation-time alignment of model behaviour | Shapes the executor; does not specify the operational standard the executor operates within |
| Procedural knowledge extraction and process mining | Discovery of process models from event logs | Closest technical neighbour; produces a model of work, but not an operating standard with authority, control, and assurance obligations |

Process mining deserves particular attention: it is the closest technical prior art, because it establishes that observed event logs can be turned into a model of real work. The programme's claim is that the model is not the deliverable; the deliverable is the governing specification compiled from that model, and it carries the authority, control, and assurance obligations that a process model has no place for.

## 8. The three genuinely new artefacts

Everything above exists. The programme's claim is that three things do not, and that they are needed together.

1. **A procedure compiled from observed work, carrying provenance.** Process mining establishes the observation. AOP adds the compilation into a governing artefact with a source-of-truth relationship to reality.
2. **A stated decision-rights boundary for a delegated actor.** Policy engines evaluate; orchestration executes. Neither states, per decision, who may act alone and who must escalate.
3. **An evidence obligation as part of the specification.** Logging is retrospective. An AOP states, before execution, what evidence will demonstrate the outcome was correct.

## 9. Related documents

- [`aop-differentiation-landscape-scope.md`](aop-differentiation-landscape-scope.md): the claim-by-claim differentiation table.
- [`aop-standards-landscape-landscape-scope.md`](aop-standards-landscape-landscape-scope.md): the standards landscape.

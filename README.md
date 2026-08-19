# Víctor Rodrigo Gutiérrez Aréyzaga

I build security verification tools for teams that want evidence, not assumptions.

My work sits between QA and AppSec: authorization testing, reachability analysis, data-boundary verification, and AI interaction-contract discovery.

The goal is simple:

**define the claim, challenge the boundary, preserve reproducible evidence, and state exactly where the conclusion stops.**

Based in Mexico City.

---

## Haritzarri

Haritzarri is a family of deterministic verification tools built around one principle:

**claims are not evidence until the boundary has been challenged.**

Each tool focuses on a narrow, testable question.

### [lekuarri](https://github.com/rodrigo-areyzaga/lekuarri)

AI interaction contract verification and behavioral discovery.

lekuarri verifies whether an AI agent’s response to a user request honored a declared interaction contract. Its discovery pipeline can also probe an agent without prior knowledge of its behavioral contract, identify recurring behavioral patterns, generate targeted follow-up probes from its own findings, and produce candidate clauses bounded strictly by observed evidence.

`362 tests · cross-model behavioral testing · evidence-hashed verdicts · evidence-driven behavioral discovery`

> What behavioral boundary does this agent actually exhibit, and where does the evidence stop?

### [jabearri](https://github.com/rodrigo-areyzaga/jabearri)

API authorization verification for QA teams.

jabearri replays eligible object-level GET requests using a second effective credential value and compares the observed responses for evidence of cross-credential exposure.

`963 automated tests · controlled validation against OWASP Juice Shop, crAPI, and VAmPI · read-only staging workflow`

> Does the authorization boundary actually hold?

### [giltzarri](https://github.com/rodrigo-areyzaga/giltzarri)

Reachability and corridor analysis.

giltzarri identifies corridor nodes: services that expand forward reach from exposed surfaces because of where they sit in a graph, not because of what they store.

`Validated against segmented, flat, and hand-built topologies`

> Which nodes matter because of where they sit?

### [mugarri](https://github.com/rodrigo-areyzaga/mugarri)

Query and data-contract verification.

mugarri verifies whether query results stay inside a declared data contract, including allowed fields, forbidden fields, required fields, cardinality, and row-value constraints.

`59 tests · 9 live SQLite validation cases · zero external dependencies`

> Did this result stay within its declared contract?

---

## Supporting projects

### [corridor-lab](https://github.com/rodrigo-areyzaga/corridor-lab)

Docker-based lab used to develop and validate the reachability model behind giltzarri. Preserved as the experimental foundation for continued verification work.

### [crapi-auth-suite](https://github.com/rodrigo-areyzaga/crapi-auth-suite)

Cypress test suite targeting OWASP crAPI.

`17 passing tests · 3 spec files`

---

## Writing

[The Service That Stored Nothing Sensitive But Still Became High Priority](https://dev.to/victor_areyzaga/the-service-that-stored-nothing-sensitive-but-still-became-high-priority-40c4) — a practical exploration of why reachability can matter more than the sensitivity of the service itself.

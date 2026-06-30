# Víctor Rodrigo Gutiérrez Aréyzaga

I build security verification tools for teams that want evidence, not assumptions.

My work sits between QA and AppSec: authorization testing, reachability triage, query/data exposure boundaries, and AI interaction-contract verification.

The aim is simple: turn security expectations into reproducible checks with observable output.

Based in Mexico City.

---

## Haritzarri

A family of deterministic security verification tools. Each one tests one boundary.

*Haritz* means oak. *Arri* means stone. Together they reflect the idea that every tool is built on one testable security boundary.

### [mozorrarri](https://github.com/rodrigo-areyzaga/mozorrarri) *(formerly accguard)*

Checks whether protected resources cross ownership boundaries under replay.

`672 automated tests · external validation against Juice Shop and VAmPI`

> Does the authorization boundary actually hold?

### [giltzarri](https://github.com/rodrigo-areyzaga/giltzarri) *(formerly corridor-id)*

Identifies corridor nodes — services that expand forward reach from exposed surfaces, by graph position alone.

`Validated against segmented, flat, and hand-built topologies`

> Which nodes matter because of where they sit, not what they store?

### [mugarri](https://github.com/rodrigo-areyzaga/mugarri) *(formerly queryguard)*

Verifies whether query results stay inside a declared data contract: allowed fields, forbidden fields, required fields, cardinality, and row-value constraints.

`59 tests · 9 live SQLite validation cases · zero external dependencies`

> Did this result stay within its declared contract?

### [lekuarri](https://github.com/rodrigo-areyzaga/lekuarri)

Verifies whether an AI agent's response to a user request honored a declared interaction contract.

`Cross-model behavioral testing · evidence-hashed verdicts`

> Did this interaction honor its declared contract?

---

## Early-access feedback

I'm currently inviting developers, QA engineers, founders, or security practitioners to try any of these tools, and I'm looking for honest feedback on setup, workflow, evidence quality, limitations, and whether the tool would be useful in a real engineering environment.

Not a replacement for a pentest or audit — a way to test narrow security questions and help shape these tools.

Reach out via LinkedIn, or open an issue with "early-access feedback" in the title.

---

## Supporting projects

### [corridor-lab](https://github.com/rodrigo-areyzaga/corridor-lab)

The Docker lab giltzarri was built and validated against. No longer actively developed; preserved as the foundation for giltzarri's continued work.

> Is the right boundary being tested at all?

### [crapi-auth-suite](https://github.com/rodrigo-areyzaga/crapi-auth-suite)

Cypress test suite targeting OWASP crAPI. 17 passing tests, 3 spec files.

> Can ownership expectations be expressed as executable tests?

---

## Writing

[The Service That Stored Nothing Sensitive But Still Became High Priority](https://dev.to/victor_areyzaga/the-service-that-stored-nothing-sensitive-but-still-became-high-priority-40c4) — dev.to

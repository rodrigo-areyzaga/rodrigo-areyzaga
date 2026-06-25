# Víctor Rodrigo Gutiérrez Aréyzaga

I build security verification tools for teams that want evidence, not assumptions.

My work focuses on AppSec, authorization testing, reachability triage, query/data exposure boundaries, and detection-oriented security validation.

The common thread across these projects is simple: test whether security controls actually hold under realistic paths, replayable evidence, and observed outputs.

Based in Mexico City.

---

## Usable early tools

These tools are under active development. They are early, narrow, and intentionally focused: each one is built around a specific security question, reproducible evidence, and clear documentation of what it does and does not cover.

### [accguard](https://github.com/rodrigo-areyzaga/accguard)

Authorization regression testing for APIs, focused on OWASP A01, BOLA/IDOR, and cross-user access-control failures.

Captures authenticated HTTP traffic, replays authorization-relevant requests under a second user, and checks whether protected resources cross user boundaries.

672 automated tests · external validation against targets including OWASP Juice Shop and VAmPI · confirmed deterministic findings with documented reproduction commands.

> *Does the authorization boundary actually hold under replay?*

### [corridor-id](https://github.com/rodrigo-areyzaga/corridor-id)

Reachability and architecture triage for identifying where exposed surfaces create paths into deeper parts of a system.

Given a service topology, identifies corridor nodes — services that expand forward reach from exposed surfaces into deeper parts of the environment.

No asset-value labels. No manual classification. Graph position only.

Validated against segmented Docker topologies, flat topologies, and hand-built topology graphs.

> *Which nodes become important because of where they sit, not what they store?*

### [queryguard](https://github.com/rodrigo-areyzaga/queryguard)

Validation tooling for query behavior, data exposure, and security-relevant result sets.

Checks whether observed query results stay within a declared operation contract: allowed fields, forbidden fields, required fields, cardinality, and row-value constraints.

59 tests across five batches · 9 live SQLite validation cases · zero external dependencies.

> *Did this result stay within its declared contract?*

---

## Early-access feedback

I’m opening a small early-access feedback program for accguard, corridor-id, and queryguard.

The first 5 developers, QA engineers, founders, or security practitioners willing to try one of these tools can use it for free in exchange for honest feedback on setup, workflow, evidence quality, limitations, and whether the tool fits a real engineering environment.

This is not a replacement for a pentest, audit, or full AppSec program. It is a practical way to test narrow security questions and help shape the tools before they become commercial offerings.

Reach out via LinkedIn, or open an issue on the relevant repo with “early-access feedback” in the title.

---

## Supporting validation projects

### [corridor-lab](https://github.com/rodrigo-areyzaga/corridor-lab)

Docker lab demonstrating a path-indexed vs. value-indexed security triage mismatch.

A service with no sensitive data can become high-priority when it functions as a corridor to downstream sensitive systems — and leaving that corridor unmonitored can make the path impossible to reconstruct after it is used.

> *Is the right boundary being tested at all?*

### [crapi-auth-suite](https://github.com/rodrigo-areyzaga/crapi-auth-suite)

Cypress authorization-boundary test suite targeting OWASP crAPI.

17 passing tests across 3 spec files. Confirmed BOLA/IDOR on vehicle location endpoint and information disclosure on community posts.

> *Can ownership expectations be expressed as executable tests?*

---

## Writing

[The Service That Stored Nothing Sensitive But Still Became High Priority](https://dev.to/victor_areyzaga/the-service-that-stored-nothing-sensitive-but-still-became-high-priority-40c4) — dev.to

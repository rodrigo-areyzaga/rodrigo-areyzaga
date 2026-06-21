# Víctor Rodrigo Gutiérrez Aréyzaga

Security verification engineer focused on application security. I build tools and labs that test whether security controls actually hold — not whether they exist, but whether they work under realistic paths and replayable evidence.

Based in Mexico City. Focused on AppSec, authorization testing, and detection-oriented security validation.

---

## Projects

### [accguard](https://github.com/rodrigo-areyzaga/accguard)
Authorization regression testing tool. Confirms whether user B received the same protected resource as user A — deterministically, within configured scope. Validated against OWASP Juice Shop, crAPI, and VAmPI. 672 tests, confirmed BOLA findings on intentionally vulnerable targets.

> *Does the authorization boundary actually hold under replay?*

### [corridor-lab](https://github.com/rodrigo-areyzaga/corridor-lab)
A Docker lab demonstrating a path-indexed vs. value-indexed security triage mismatch. A service with no sensitive data can become high-priority when it functions as a corridor to downstream sensitive systems — and leaving that corridor unmonitored can make the path impossible to reconstruct after it is used.

> *Is the right boundary being tested at all?*

### [corridor-id](https://github.com/rodrigo-areyzaga/corridor-id)
Given a service topology, identifies which nodes are corridor nodes — services that expand forward reach from exposed surfaces into deeper parts of the environment. No asset-value labels. No human classification. Reach and graph position only. Currently parses Docker Compose files, with a format-agnostic core validated against hand-built topologies. Tested against four architecturally different topologies: two produce corridor nodes, two correctly produce none.

> *Which nodes become important because of where they sit, not what they store?*

### [crapi-auth-suite](https://github.com/rodrigo-areyzaga/crapi-auth-suite)
Cypress authorization-boundary test suite targeting OWASP crAPI. 17 passing tests across 3 spec files. Confirmed BOLA/IDOR on vehicle location endpoint (HIGH) and information disclosure on community posts (MEDIUM).

---

## Writing

[The Service That Stored Nothing Sensitive But Still Became High Priority](https://dev.to/victor_areyzaga/the-service-that-stored-nothing-sensitive-but-still-became-high-priority-40c4) — dev.to

---

## Learning log

[Cybersecurity](https://github.com/rodrigo-areyzaga/Cybersecurity) — a living record of my security education: Google Cybersecurity Professional Certificate, TryHackMe, Cisco Networking Academy, and the path that led to accguard, corridor-lab, and corridor-id.

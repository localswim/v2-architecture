# ADR 0002 · One localhost daemon and port

Accepted by Terry on November 6, 2026.

V2 serves one user on localhost through one daemon and one server port. Route
workspace, board and operational API requests to the exact selected scope on that
listener. The accepted workspace host already provides the shared listener.
Build new features on that path.

This replaces V1's separate listener for each board and its additional gateway
listener. Keep per-board storage, writer ownership, authority and recovery
boundaries inside the routed host. Clients can select distinct boards without
starting additional board servers. Preserve exact selection and stable routing
through restart and adoption.

Favor in-process components for the normal localhost installation. Terry leaves
internal service boundaries to the team. A separate service needs a concrete
operational or isolation reason and a documented lifecycle and failure boundary.
Any such design keeps one user-facing server port.

Qualify new alerts, publishing, update and compatibility paths through this
topology. The architecture continues to support the V1 operator outcomes
described in [ADR 0001](adr-0001-v1-behavior-oracle.md).

# ADR 0001 · V1 as the behavior oracle

Accepted by Terry on November 6, 2026.

The Python V1 is the reference for the behavior Terry relies on in daily use.
V2 is a greenfield replacement that reduces technical debt and makes the product
easier to maintain. When an expected workflow is unclear, check the supported V1
behavior and use it to define the V2 outcome.

Pin a V1 revision when building the compatibility ledger. Map supported V1
workflows and integrations to accepted V2 evidence, planned gaps or explicit
owner-approved differences. Refresh the ledger when V1 changes. Qualify the
accepted behavior through the ordinary browser, CLI and relevant API clients.
Use V1 behavior and contracts as evidence and implement the replacement through
the shared V2 core.

V2 can use a different internal design to deliver the same operator outcome.
[ADR 0002](adr-0002-single-localhost-daemon.md) records the intentional change
to V1's listener topology. Material differences in visible behavior or supported
integration contracts need an explicit disposition before a drop-in claim.
Preserve stronger safety boundaries when designing compatible operator paths.

The replacement plan includes synthetic qualification and adoption rehearsal.
Named live adoption, external delivery, remote credentials and release
publication retain separate owner gates.

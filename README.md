# localswim v2 architecture

High-level architecture and decision records for the Go + TypeScript 7.x clean-room reboot of localswim.

## Free and open source

localswim is and will remain free and open-source software. All localswim project repositories are public and use the MIT license.

See [LICENSE](LICENSE). Copyright (c) 2026 Terry Ott.

## Text file conventions

All localswim repositories use Unix-style LF line endings. `.gitattributes`
enforces LF for Git text files, and `.editorconfig` supplies the same editor rule.
Text files use UTF-8 and end with a newline; binary files retain their bytes.

## Status

Architecture work is in progress. Terry accepted the foundation, structure,
corrected runtime, interface, and operations packets on 2026-10-25. Unselected
alternatives and unverified numerical targets remain explicit recommendations.
Qualification/adoption is the current reviewed packet; final synthesis follows its
acceptance. This repository does not contain the v2 implementation.

## Architecture documents

The preserved notes retain their original candidate wording. Read the current
[owner decisions](docs/decisions/owner-decisions-2026-10-25-r7.txt) for subsequent
acceptance and standing public/MIT/LF and board-lane policy. The working lane rules
are also recorded in [AGENTS.md](AGENTS.md).

- [Bounded input brief and evidence rules](docs/inputs/architecture-input-brief-r2.txt)
- [Product scope](docs/design/01-product-scope.txt)
- [Evidence and reuse method](docs/design/02-clean-room-method.txt)
- [Quality attributes and proposed acceptance targets](docs/design/03-quality-attributes.txt)
- [Independent foundation review](docs/reviews/04-baseline-review.txt)

The accepted structure packet below includes a separately reviewed clarification
addendum. Read the original notes together with the addendum; their original wording
is preserved as evidence rather than silently rewritten after acceptance.

- [System topology](docs/design/05-system-topology.txt)
- [Domain and workflow policy](docs/design/06-domain-policy.txt)
- [Relationships and triage](docs/design/07-relationships-triage.txt)
- [Canonical state and audit](docs/design/08-state-audit.txt)
- [Independent structure review](docs/reviews/09-structure-review.txt)
- [Structure clarification addendum](docs/design/30-structure-addendum.txt)
- [Independent addendum review](docs/reviews/31-structure-addendum-review.txt)

The accepted runtime packet below includes its original findings, companion addendum
and fresh review closing those findings under stated preconditions. Read the original
notes with the addendum.

- [Persistence and recovery](docs/design/10-persistence-recovery.txt)
- [Ownership and lifecycle](docs/design/11-ownership-lifecycle.txt)
- [Local trust and security](docs/design/12-trust-security.txt)
- [Interface contracts](docs/design/13-interface-contracts.txt)
- [Original runtime review and findings](docs/reviews/14-runtime-review.txt)
- [Runtime contract addendum](docs/design/32-runtime-addendum.txt)
- [Independent runtime addendum review](docs/reviews/33-runtime-addendum-review.txt)

The accepted bootstrap recommendation proposes local certificate-issuer trust. It
is not an approved installation or a qualified browser/platform guarantee. Qualify
the trust scope, cookie scope, and human-issuance capability assumptions before use.
No trust store or live service was changed by this architecture work.

The accepted interface and operations notes below were authored in parallel from
the accepted runtime. Fresh review 19 checks the interfaces; review 24 checks
operations and their cross-packet consistency. Both passed with non-blocking
observations and were accepted through Terry's explicit browser-approval request.

- [CLI](docs/design/15-cli.txt)
- [Browser](docs/design/16-browser.txt)
- [Workspace](docs/design/17-workspace.txt)
- [Attachments and publisher inventory](docs/design/18-attachments.txt)
- [Independent interface review](docs/reviews/19-interface-review.txt)
- [Publishing and recovery](docs/design/20-publishing-recovery.txt)
- [Activity monitor](docs/design/21-monitor.txt)
- [Delivery and toolchain](docs/design/22-delivery-toolchain.txt)
- [Operational health and diagnostics](docs/design/23-observability.txt)
- [Independent operations and integration review](docs/reviews/24-operations-review.txt)

Tool availability is distinct from compatibility qualification. The delivery note
records stable TS7 availability and the generator's separate TS5 dependency; it does
not claim a successful combined build, schema equivalence, or platform qualification.

The qualification/adoption packet below has passed fresh independent review with
non-blocking observations and awaits owner review and approval. It defines required
evidence and execution gates; no tests, migration, trust setup, or cutover were run.

- [Qualification and acceptance strategy](docs/design/25-validation-strategy.txt)
- [Compatibility, coexistence, and adoption](docs/design/26-adoption.txt)
- [Independent qualification/adoption review](docs/reviews/27-qualification-review.txt)

The development method is a fresh implementation with disclosed source-derived
provenance, not a claim of independently isolated clean-room certification.
Legacy behavior citations refer to the public
[localswim user guide](https://github.com/TerryOtt/localswim/blob/main/README.md).

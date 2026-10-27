# localswim v2 architecture

High-level architecture and decision records for the Go + TypeScript 7.x clean-room reboot of localswim.

The **2026-10-27 [localhost scope reset](docs/slice01/22-localhost-scope-reset.txt)**
is the current direction: V1's local product on Go/TypeScript and SQLite, with
both browser UI and CLI using loopback-only HTTP. LAN access, TLS and certificate,
enrollment or delegation ceremonies are outside V2. SQLite durability and human/bot
approval boundaries remain. The [remaining-task overlay](docs/slice01/22-localhost-task-map.json)
supersedes conflicting transport and qualification requirements below. This is
an owner-directed scope change to implement; historical packets remain preserved.

Start with the [fresh-choice decision agenda](docs/reconsideration/44-decision-agenda.txt)
and [current owner direction](docs/decisions/fresh-choice-reassessment-2026-10-25.txt).
Terry reopened every earlier product and technical choice, including the candidate
language split. Working v1 is evidence of useful behavior; exact copying is optional,
and retention or departure needs a concrete case.

The first [consolidated architecture overview](docs/design/28-architecture-overview.txt)
and [independent final review](docs/reviews/29-final-review.txt) remain preserved
evidence. Their documentary consistency does not settle the best fresh design.

## Slice 01 implementation design

The first slice follows one board through browser and CLI reads, creation, edits,
comments, conflicts, reload/restart recovery, one attachment and export/restore.
Terry accepted its [scope contract](docs/slice01/01-scope-acceptance.txt) and
[independent scope review](docs/slice01/02-scope-review.txt) on 2026-10-25.
The detailed proposals cover [data and transactions](docs/slice01/03-data-transactions.txt),
[commands and API](docs/slice01/04-commands-api-cli.txt),
[sessions and browser recovery](docs/slice01/05-sessions-browser-recovery.txt),
[attachments and export/restore](docs/slice01/06-attachments-export-restore.txt), and
[build and acceptance evidence](docs/slice01/07-build-acceptance-evidence.txt).
The [independent seam review](docs/slice01/08-design-seams-review.txt) records three
required corrections. Read it with the
[companion clarification](docs/slice01/18-seam-clarifications.txt) and
[fresh correction review](docs/slice01/19-clarifications-review.txt).
Terry accepted that complete design/correction packet on 2026-10-25.
The proposed [implementation packet](docs/slice01/09-implementation-packet.txt),
[logical task breakdown](docs/slice01/09-task-proposals.json), and
[fresh readiness review](docs/slice01/10-readiness-review.txt) distinguish staged
contract freezes and qualification from product implementation. Read that review's
three ownership/publication findings with the
[task-map correction](docs/slice01/20-task-clarifications.txt) and
[fresh correction validation](docs/slice01/21-task-clarifications-review.txt).
Terry's acceptance gates task materialization and separately scoped execution.
These notes provide no implementation or runtime qualification evidence.

## Free and open source

localswim is and will remain free and open-source software. All localswim project repositories are public and use the MIT license.

See [LICENSE](LICENSE). Copyright (c) 2026 Terry Ott.

## Text file conventions

All localswim repositories use Unix-style LF line endings. `.gitattributes`
enforces LF for Git text files, and `.editorconfig` supplies the same editor rule.
Text files use UTF-8 and end with a newline; binary files retain their bytes.

## Status

The fresh-choice reassessment challenged product, stack/topology, storage, security,
interfaces, domain, operations and qualification. Independent reviews
[42](docs/reconsideration/42-review-foundations.txt) and
[43](docs/reconsideration/43-review-experience.txt) produced six correction/coverage
points addressed in [companion 46](docs/reconsideration/46-clarifications.txt);
[fresh review 47](docs/reconsideration/47-review-clarifications.txt) passed the closure.
The agenda contains recommendations, explicit unknowns and proposed distinguishing
evidence. Its [fresh independent final review](docs/reconsideration/45-review-agenda.txt)
passed with one nonblocking observation and no mandatory correction. Hierarchy shape
and blocking-cycle admission remain explicit unresolved choices in the next ledger.
No changed design, implementation or experiment is adopted by these notes.

Terry accepted the foundation, structure, corrected runtime, interface, operations,
and qualification/adoption packets on 2026-10-25. Final synthesis and fresh independent
validation of that first packet are finished and were handed off for Terry's final
review and approval. Its original decision records describe that historical scope;
the newer owner direction reopens its selections for comparison. This is architecture
evidence, not an implementation or qualified release.

## Architecture documents

The preserved notes retain their original candidate wording. Read the current
[owner decisions](docs/decisions/owner-decisions-2026-10-25-r8.txt) for subsequent
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

The accepted qualification/adoption packet below passed fresh independent review
with non-blocking observations. It defines required evidence and execution gates;
no tests, migration, trust setup, or cutover were run.

- [Qualification and acceptance strategy](docs/design/25-validation-strategy.txt)
- [Compatibility, coexistence, and adoption](docs/design/26-adoption.txt)
- [Independent qualification/adoption review](docs/reviews/27-qualification-review.txt)

The development method is a fresh implementation with disclosed source-derived
provenance, not a claim of independently isolated clean-room certification.
Legacy behavior citations refer to the public
[localswim user guide](https://github.com/TerryOtt/localswim/blob/main/README.md).

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

Architecture work is in progress. Terry approved foundation review gate 0004 on
2026-10-25. Its card remains Ready for Review as requested; that lane does not
negate the recorded approval. Unselected alternatives and unverified numerical
targets remain explicit recommendations. This repository does not contain the v2
implementation.

## Architecture documents

The preserved notes retain their original candidate wording. Read the current
[owner decisions](docs/decisions/owner-decisions-2026-10-25-r4.txt) for subsequent
acceptance and standing public/MIT/LF and board-lane policy. The working lane rules
are also recorded in [AGENTS.md](AGENTS.md).

- [Bounded input brief and evidence rules](docs/inputs/architecture-input-brief-r2.txt)
- [Product scope](docs/design/01-product-scope.txt)
- [Evidence and reuse method](docs/design/02-clean-room-method.txt)
- [Quality attributes and proposed acceptance targets](docs/design/03-quality-attributes.txt)
- [Independent foundation review](docs/reviews/04-baseline-review.txt)

The structure packet below has passed independent review and a separately reviewed
clarification addendum. It awaits Terry's acceptance at gate 0009. Read the original
notes together with the addendum; their original wording is preserved.

- [System topology](docs/design/05-system-topology.txt)
- [Domain and workflow policy](docs/design/06-domain-policy.txt)
- [Relationships and triage](docs/design/07-relationships-triage.txt)
- [Canonical state and audit](docs/design/08-state-audit.txt)
- [Independent structure review](docs/reviews/09-structure-review.txt)
- [Structure clarification addendum](docs/design/30-structure-addendum.txt)
- [Independent addendum review](docs/reviews/31-structure-addendum-review.txt)

The development method is a fresh implementation with disclosed source-derived
provenance, not a claim of independently isolated clean-room certification.
Legacy behavior citations refer to the public
[localswim user guide](https://github.com/TerryOtt/localswim/blob/main/README.md).

# localswim v2 architecture

High-level architecture and decision records for the Go + TypeScript 7.x clean-room reboot of localswim.

## Free and open source

localswim is and will remain free and open-source software. All localswim project repositories are public and use the MIT license.

See [LICENSE](LICENSE). Copyright (c) 2026 Terry Ott.

## Status

Architecture work is in progress. Terry approved foundation review gate 0004 on
2026-10-25. Its card remains Ready for Review as requested; that lane does not
negate the recorded approval. Unselected alternatives and unverified numerical
targets remain explicit recommendations. This repository does not contain the v2
implementation.

## Architecture documents

The preserved notes retain their original candidate wording. Read the current
[owner decisions](docs/decisions/owner-decisions-2026-10-25-r2.txt) for subsequent
acceptance and standing public/MIT policy.

- [Bounded input brief and evidence rules](docs/inputs/architecture-input-brief-r2.txt)
- [Product scope](docs/design/01-product-scope.txt)
- [Evidence and reuse method](docs/design/02-clean-room-method.txt)
- [Quality attributes and proposed acceptance targets](docs/design/03-quality-attributes.txt)
- [Independent foundation review](docs/reviews/04-baseline-review.txt)

The development method is a fresh implementation with disclosed source-derived
provenance, not a claim of independently isolated clean-room certification.
Legacy behavior citations refer to the public
[localswim user guide](https://github.com/TerryOtt/localswim/blob/main/README.md).

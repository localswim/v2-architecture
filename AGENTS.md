# Repository guidance

This repository holds the Go + TypeScript 7.x architecture work for localswim.
All localswim project repositories are public and MIT-licensed FOSS. Use UTF-8
text, Unix-style LF line endings, and a final newline; preserve binary bytes.
Keep real board data, runtime credentials, and private operational records out
of this public repository.

## Terry's board workflow

Terry clarified these lane meanings on 2026-10-25:

- **Ready for Work** includes scoped, authorized work with dependencies. Keep
  those dependencies; this lane does not mean the prerequisites are resolved.
- **Ready for Review (RFR)** means the only remaining step is Terry's review
  and approval. Finished architecture and decision proposals waiting only for
  review/approval belong here.
- **Needs Terry** means unfinished work cannot advance without a specific input
  or action only Terry can provide. State the concrete intervention needed,
  such as missing information, a decision required to finish the work, required
  access, or a manual step. Review/approval alone belongs in RFR.
- **Blocked** means neither Terry nor Bot can do anything to advance the work
  until an external condition changes, such as ordered test hardware arriving.
  Ordinary dependencies and pending reviews do not justify this lane.
- Dependent work stays Ready for Work while its prerequisite retains the
  appropriate lane. RFR alone does not approve a prerequisite or waive a gate.
- Move a selected card In Progress before substantive work or delegation.
  Terry controls Completed; Bot must not mark its own work Completed.

Use the shared localswim CLI for board reads and mutations. Never edit board
JSON directly. Preserve historical comments, superseded plans, and review evidence.

## Shared board owner notifications

The current monitor is built into the healthy shared service at
`C:\Projects\localswim`; reuse it and keep legacy JSON watchers/pools off.
Use the shared frozen runner with an absolute owned BOARD path:
`uv run --project C:\Projects\localswim --frozen --offline localswim-cli BOARD`.

On an explicit connect request, inspect `notifications status --json`, resolve
the current owning chat UUID from Codex app metadata, set
`notifications target THREAD_UUID` only if needed, enable only if disabled, then
verify enabled/target/board identity. Never use a remembered/example target.
Check exits; inspect status after uncertain writes rather than replaying blindly.
Target preserves enabled state and disable retains target. Documentation updates
or service startup alone do not activate notifications; honor explicit shutdown.

Committed Human edits coalesce after 15 seconds of quiet. One bounded
`codex queue` attempt can wake the chat without Terry adding a prompt. Bot edits
do not notify. There is no durable cursor/catch-up/retry; pending notices can be
lost on shutdown. Native `codex.exe` must be on the Windows service PATH.
Acceptance means queued, not completed or authorized ticket work.

Inspect sanitized `activity monitor-between SINCE UNTIL --json` metadata first
for queued alerts, using bounded pagination. Only complete, valid, nonempty
all-Bot results prove suppression safe. Preserve Human/unknown alerts and normal
work gates. Legacy filesystem watcher/pool commands and their optional extra are
retired. Do not launch/reload/stop old interfaces, reinstall the native watcher
dependency or recreate project-local watchers from historical code. Stale installed
launchers fail with built-in guidance; there is no old-startup compatibility flag
or environment override. Preserve legacy target/cursor/pending/lock files. Never
act on a remembered PID without verifying current process/ownership. Keep project
artifacts outside the shared installation. SSE status does not change this workflow.

## Fresh-eyes review exception

Terry clarified on 2026-10-29 that a fresh-eyes subagent review of work authored
by the parent is always permitted, even when no useful work can overlap. An
independent audit without the parent's preconceived conclusions is a useful
use of credits; parallel work is not a prerequisite for this review.

This supersedes earlier parallel-only delegation restrictions for that review.
It does not require fixed reviewer pairs or idle staffing. Keep other purely
serial work in the parent, provide evidence without prescribing a verdict, and
describe actual independence truthfully. Preserve task authorization, required
verification and explicit model/effort, depth and concurrency limits.

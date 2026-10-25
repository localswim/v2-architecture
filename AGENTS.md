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

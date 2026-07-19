# DECISION ENTRY TEMPLATE

> **Maintained by ④ Repository & Canon Management.** Matches `studio/06_Operations/DECISION_LOG.md`'s exact table columns (verify against the live file before use — this template mirrors it as of CYCLE-0001; if the live table's columns ever change, update this template to match, not the other way around). Only the Creator's own decisions belong in `DECISION_LOG.md`; do not use this template to record a department's internal working choice — that belongs in a handoff or task note instead.

---

## Adding a new row to `DECISION_LOG.md`

Append (never rewrite existing rows) a new row in this exact column order:

| ID | Date | Decision | Decided by | Evidence |
|---|---|---|---|---|
| `DEC-<next sequential 4-digit number>` | `<YYYY-MM-DD>` or `PENDING` | `<one-line statement of exactly what was decided — precise enough that a future reader does not need to re-derive scope from context>` | `<Creator / Director / other named authority — never a department symbol alone, since departments implement decisions but do not make them>` | `<pointer: thread / commit / file / TASK-ID that recorded or evidences this decision>` |

### Field notes

- **ID:** sequential, never reused, never renumbered even if a later decision supersedes an earlier one (mark the *decision text* as superseded if needed; do not delete or renumber the row).
- **Date:** use `PENDING` (not a blank cell, not a guessed date) when the decision has been proposed/requested but not yet made — see `DEC-0008`/`DEC-0009` in the live log for the exact pattern. Update the Date field to the real date only once the Creator has actually decided, in the same edit that fills in the Decision/Decided-by/Evidence fields if they were placeholders.
- **Decision:** state the decision itself, not the debate that led to it. If the decision has multiple parts, use a single cell with semicolons, matching the live log's existing style for compound decisions (e.g. DEC-0012's five-department model entry).
- **Decided by:** name the actual deciding authority. "Creator" is the normal value; "Director, unopposed" or "Creator (Conductor order, agent thread)" are acceptable when the live log's existing rows use that phrasing for a specific provenance nuance — match existing style rather than inventing a new phrasing convention.
- **Evidence:** a concrete pointer a future reader could actually follow — a thread reference, a commit SHA/message, a specific file, or a TASK-ID whose resolution embodies the decision. Never leave this cell as prose restating the decision itself.

### Do

- Append new rows at the bottom of the existing table, preserving all prior rows byte-for-byte.
- Cross-reference the new DEC-ID from any file whose status changes because of it (e.g. `SOURCE_OF_TRUTH.md`'s header note names `DEC-0008` by ID).

### Do not

- Do not edit an existing row's Decision text after the fact to "clean it up" — if a decision needs correction, that is itself a new decision requiring its own new row and its own Creator approval.
- Do not use this template to log a department's own working choice, a rejected proposal, or an UNDECIDED item — those belong in a handoff note, `TASK_QUEUE.md`, or `OPEN_QUESTIONS.md` respectively, not in `DECISION_LOG.md`.

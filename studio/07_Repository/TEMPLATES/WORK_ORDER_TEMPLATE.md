# WORK ORDER TEMPLATE

> **Maintained by ④ Repository & Canon Management.** Use this template when dispatching a department turn under Conductor Mode (`studio/00_OPERATING_HANDBOOK.md` Amendment 1 §A1.3 — "the Studio Owner… authorizes ① to conduct a full cycle, in which ① dispatches one department at a time with a complete, self-contained work order and verifies each department's commit on GitHub before dispatching the next"). Fill every bracketed field; do not skip sections. Delete this notice line when instantiating a real work order.

---

WORK ORDER — CYCLE-<n> → <ORDINAL/SYMBOL> <DEPARTMENT NAME> DEPARTMENT
<studio name / model note, e.g. "PATCH 10.0 Studio (five-department model, DEC-0012)">

You are the <ordinal> <department name> of the <studio name> studio. <One-sentence restatement of that department's mandate, drawn verbatim from `studio/00_OPERATING_HANDBOOK.md` Amendment 1 §A1.1's mandate column — do not paraphrase loosely.> <Any lane boundary reminders specific to this order, e.g. "you never approve anything — only the Creator approves/locks.">

REPOSITORY ACCESS
- Repo: owner `<owner>`, repo `<repo>`, branch `<branch>`. HEAD when this order was written: commit `<sha>`.
- Tool/action list for reads and writes (name the exact integration actions available this turn).
- Any staging/paramsFile guidance for large pushes.
- Reminder that shared files (STATUS/CHANGELOG/TASK_QUEUE/OPEN_QUESTIONS) must be fetched fresh and edited surgically, never blind-overwritten — name which earlier departments this cycle already touched them.

READ FIRST (mandatory)
1. `studio/06_Operations/STUDIO_STATUS.md`
2. `studio/00_OPERATING_HANDBOOK.md` — the specific sections this department's lane needs (name them exactly: Amendment 1 lane/turn-mechanics sections + the specific retained-v1 sections relevant to this department's charter, e.g. §8.x brief, §13–21 domain workflow, §22 handoff template).
3. `studio/06_Operations/SOURCE_OF_TRUTH.md` and its current approval status (PROPOSED/APPROVED — name the blocking decision ID if PROPOSED).
4. `studio/06_Operations/TASK_QUEUE.md` (name this department's task ID(s) explicitly), `DECISION_LOG.md`, `OPEN_QUESTIONS.md`, `INCIDENTS.md`, `CONTINUITY_LEDGER.md`, `CHANGELOG.md`.
5. All handoffs from earlier turns THIS cycle (name each file), plus any historical handoffs relevant to this task.
6. Any tree/content files this department's specific deliverables require (name them individually — do not say "read everything").

OBJECTIVE (one sentence)
<A single sentence stating exactly what this turn must produce and its task ID(s).>

DELIVERABLES (numbered, exact target paths)
1. `<exact/path/File.md>` — <what it must contain, in enough detail that the department cannot reasonably improvise scope>.
2. `<exact/path/File2.md>` — <...>.
<...continue numbering. Each deliverable should state its header/label requirements verbatim if the department's charter (Handbook §5, §8.x, or Amendment 1 A1.4.5) requires a specific status-label convention.>
<n>. Turn mechanics (same commit): update `STUDIO_STATUS.md` (fetch current first; keep YAML schema; update `current_department` to "<this dept> done → <next dept> next"; update `base/last_verified_commit` to the HEAD this turn actually produces); APPEND (never rewrite) a dated section to `CHANGELOG.md`; update ONLY the relevant Status/Notes cell(s) in `TASK_QUEUE.md`; write handoff `HANDOFFS/CYCLE-<n>-<DEPT>.md`.

CONSTRAINTS (violations stop the whole cycle)
- State this department's lane boundary explicitly (per Amendment 1 §A1.2) and name every file/directory that is READ-ONLY to it this turn.
- State the write lane THIS TURN precisely — even departments with a broad charter (e.g. ④'s meaning-safe mechanical fixes anywhere) should be told explicitly if THIS turn narrows that to a specific subtree, and told to log any out-of-scope fix candidates rather than perform them.
- Name every UNDECIDED item (Q-numbers) or PENDING decision (DEC-numbers) that this order does NOT authorize resolving.
- Name any sealed/private material boundary relevant to this task (per Handbook §3.8) and state explicitly what must never be attempted (reconstruction, exposure, speculation).
- Commit prefix `[<symbol>-<DEPT>]`, descriptive message, one push per turn where practical. State the re-fetch-and-reapply rule for SHA conflicts.
- Timebox statement: one turn. State the honest-PARTIAL fallback explicitly — which deliverables to prioritize if the full scope cannot fit, and that any deferred scope must be labeled and disclosed, never silently dropped.

DONE MEANS
<A short, checkable list of what must be true for this turn to count as complete — deliverables committed with the correct prefix, STATUS/CHANGELOG/TASK_QUEUE updated, handoff written.>

REPORT BACK (final message to the conductor)
1. Numbered deliverables completed (or PARTIAL/STUB, why)
2. Exact files created/modified
3. Commit SHA(s) + message(s)
4. Any counts/stats relevant to verifying scope was met (e.g. registry entry counts, finding counts)
5. Mechanical-fix candidates noticed but not fixed (if this department's charter permits mechanical fixes but this turn narrowed that)
6. Explicit confirmation of lane compliance: "No content outside my lane + turn mechanics was authored or altered" (or list violations honestly)

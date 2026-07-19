# TURN HANDOFF TEMPLATE

> **Maintained by ④ Repository & Canon Management.** Aligned with `studio/00_OPERATING_HANDBOOK.md` v1 §22 "Handoff and Run Record" field set, adapted to Amendment 1's per-department turn model. File naming per Amendment 1 §A1.4.4: `studio/06_Operations/HANDOFFS/CYCLE-<n>-<DEPT>.md`, where `<DEPT>` is one of `EP` / `LORE` / `VISUAL` / `REPO` / `QA`. (Pre-Amendment-1 single-agent runs used `RUN-<n>.md` instead — see `HANDOFFS/RUN-0001.md` for that legacy format; do not use it for department turns.) Delete this notice line when instantiating a real handoff.

---

# Turn Handoff — CYCLE-<n>-<SYMBOL> (<Department Name>)
- **Date:** <YYYY-MM-DD> · **Mode:** <Conductor Mode (dispatched by ① EP) / Creator-advanced turn> — <one clause on what kind of turn this is, e.g. "records turn, no canon rewritten" / "spec-drafting turn — no generation">
- **Base commit:** `<sha>` (<whose prior turn this was, e.g. "② Lore's CYCLE-<n> records commit">)

## What <dept symbol> did this turn

1. **<TASK-ID> — <short title>.** <What was produced, exact file path(s), and the key facts/scope covered. State explicitly whether any existing authoritative file was opened for writing, and if not, say so ("read-only — byte-for-byte unchanged").>
2. **<TASK-ID> — <short title>.** <...>
<...one numbered item per deliverable, in the same order as the dispatching work order's DELIVERABLES list.>
<n>. **Turn mechanics:** `STUDIO_STATUS.md` updated (`current_department` → "<this dept> done → <next dept> next"; `base_remote_commit`/`last_verified_commit` advanced to `<sha this turn actually produced>"). `CHANGELOG.md` appended (never rewrote existing entries) with a "<dated section header>" section. `TASK_QUEUE.md` — name exactly which cell(s) were touched and confirm every other row/column was left untouched.

## Decisions needed from the Creator (not made here)

- <Each open decision this turn surfaced but did not make, phrased as a question the Creator can answer directly.>
- <...>
- General: name the umbrella blocker(s) still governing this lane (e.g. DEC-0008 pending, I-0001 open) if relevant.

## Risks flagged (for ⑤ QA and future departments)

- <Each risk, drift, inconsistency, or gap this turn discovered but did not fix — with enough detail (file/section pointers) that a future turn does not need to rediscover it. If this turn found or is documenting a CONFLICT-FOR-QA item, name its ID here.>
- <...>

## What was NOT done (honest PARTIAL disclosure)

<If every deliverable in this turn's scope was fully produced, say so plainly ("Nothing in this turn's scope was left incomplete"). Then separately list what was deliberately NOT done because it exceeds this turn's authority or was explicitly out of scope — do not conflate "didn't fit in the timebox" with "wasn't authorized"; label each item correctly.>

## Next department: <next dept name>

- <What the next department's turn depends on from this one, if anything — or state plainly "independent, does not block on this turn's deliverables.">
- <Anything this turn produced that the next department should be aware of even though no cross-lane edit was requested of them.>

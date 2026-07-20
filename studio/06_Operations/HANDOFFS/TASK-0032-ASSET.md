# TASK-0032 — ASSET MANAGEMENT HANDOFF (ENV-SPEC-A/B/C spec LOCKs recorded)

**From:** Asset Management Agent · CYCLE-0006 (parallel lane) · 2026-07-20
**Authority:** Owner ruling DEC-0018, 2026-07-20 (`studio/06_Operations/DECISION_LOG.md`, DEC-0018 row, item 3)
**Work Order:** TASK-0032 (P1), dispatched by Executive Producer Agent at base commit `4e8ea889c39f55fb7888781bd778a7c79e59d2ad`
**Agent thread (audit):** https://hyperagent.com/thread/cmrsw2fco10cp07ad2r318zby

## What landed

| Item | Value |
|---|---|
| Lock commit | `828ef2a999ed5cf4d851147ce4b32187356f5986` — touches ONLY `studio/03_Assets/Asset_Registry.md` |
| Registry blob after commit | `ebe9381c9669d46f75d0490736cd28c054f9db70` (9,428 bytes) |
| Registry blob before commit | `03d574682c0d02337e96713085930585e9c7940f` (6,278 bytes) |
| Diff shape | one contiguous insertion (25 lines / 3,150 bytes) between "Environments — LOCKED" and "Style anchors (real PMU)"; zero deletions, zero modified lines |
| Pinned spec source | `studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md` PART I at git blob `1356127b39dae889f6559ffaacd4fe1c7e2f5356` (that file's state at base commit `4e8ea889`) — the exact Owner-approved bytes |

## Registry entry anchors (in `studio/03_Assets/Asset_Registry.md` @ `828ef2a9…`)

- Section: `#environment-plate-specs--locked-spec-locks-plates-pending-task-0033` — "Environment plate SPECS — LOCKED (spec locks; plates pending TASK-0033)"
- `#env-spec-a-kf-03--locked` — ENV-SPEC-A (KF-03) — LOCKED
- `#env-spec-b-kf-04--locked` — ENV-SPEC-B (KF-04) — LOCKED
- `#env-spec-c-kf-12--locked` — ENV-SPEC-C (KF-12) — LOCKED (carries the Q-20 caveat)

## Per-spec section pointers (pinned Gap_Specs bytes at commit `4e8ea889`)

- ENV-SPEC-A — KF-03 matched conversion pair (A1 8.0 settlement · A2 9.0 street):
  `https://github.com/lycacallenero55-cpu/patch-10.0/blob/4e8ea889c39f55fb7888781bd778a7c79e59d2ad/studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md#env-spec-a--kf-03-wave-converting-desert-wide--a-matched-pair-of-mid-conversion-plates`
- ENV-SPEC-B — KF-04 environment half only (B1 8.0 well-scaffold context · B2 9.0 Cha's Kitchen doorway):
  `https://github.com/lycacallenero55-cpu/patch-10.0/blob/4e8ea889c39f55fb7888781bd778a7c79e59d2ad/studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md#env-spec-b--kf-04-split-seam-cha--the-environment-half-only-two-context-plates`
- ENV-SPEC-C — KF-12 first+last frame pair (C1 9.0 street post-patch · C2 2.0 murim pass):
  `https://github.com/lycacallenero55-cpu/patch-10.0/blob/4e8ea889c39f55fb7888781bd778a7c79e59d2ad/studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md#env-spec-c--kf-12-world-testimony-flood-street-becoming-murim-pass--firstlast-frame-pair-the-centerpiece`

## Suggested checks (reviewers)

1. **Diff check:** commit `828ef2a9` modifies only `studio/03_Assets/Asset_Registry.md`; recompute the diff vs blob `03d57468` — expect a single insertion block, no other bytes changed; registry blob at the commit = `ebe9381c…`.
2. **Pin check:** blob SHA of `studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md` at `4e8ea889` = `1356127b…`; all three entries cite exactly that blob. The Gap_Specs file itself was NOT edited by this task (its blob is unchanged).
3. **Scope check:** exactly three entries (ENV-SPEC-A/B/C); NO entries for PART II (monster/extinction design) or PART III (registry-card UI) — both remain DRAFT/unlocked, gated on Q-21/Q-22; authority string "Owner ruling DEC-0018, 2026-07-20" on all three; ENV-SPEC-C carries the Q-20 caveat verbatim.
4. **Open-items check:** the entries record locks only — Q-20 (formal first-visual-canon adoption for dead-world 2.0) is recorded as PENDING, and no official Q-number or file-local OQ-VIS proposal item is resolved anywhere in the added bytes.
5. **Ledger check:** no ops ledgers were touched by Asset Management (EP records statuses); Asset Management commits in this task: `828ef2a9` (registry) + this handoff file only.

## For the Environment Art Agent (TASK-0033)

- Generate against the **pinned bytes**: fetch the spec file at blob `1356127b…` (or at commit `4e8ea889`) — not against any later revision of the DRAFT file. The lock covers PART I as pinned; the file's DRAFT label is by design (the LOCK lives in the registry).
- **ENV-SPEC-A** is a matched pair — A1+A2 share one wave-front angle and screen direction (the S06 match-cut depends on it).
- **ENV-SPEC-B** is the environment half ONLY — no Cha figure; her kit/pose (KIT-CHAR-004) and the FX-PATCH-on-character grammar question are outside this lock.
- **ENV-SPEC-C** is a camera-identical first+last pair; the lock authorizes the KF-12 trailer plates per DEC-0018 and does **not** resolve Q-20 (2.0 visual canon not formally adopted).
- The pinned spec text embeds PROPOSAL items (file-local OQ-VIS-1…8) with ③'s recommendations on record; the lock pins the text without ruling those items — where generation forces an unmade Owner choice, escalate via EP rather than deciding.
- House laws restated from the spec's own header: flat-2D law + gpt-image-2 engine (DEC-0003); no image bytes committed to the repo (TASK-0033 row: platform-hosted masters + sha256 recorded); Visual Review before any downstream use.

*Asset Management lane closed for TASK-0032: registry + this handoff only; no Gap_Specs edits; no ledger writes; no force-push.*

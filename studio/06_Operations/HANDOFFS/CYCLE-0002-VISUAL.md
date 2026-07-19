# Handoff — CYCLE-0002 ③ Visual Production Department

**From:** ③ Visual Production
**To:** ⑤ QA (GATE(③), per Amendment 2 §A2.2) — then back into the conducted cycle (④ Repo & Canon next, per the cycle order)
**Date:** 2026-07-19
**Base commit this turn started from:** `9345a5ef4d9fe76e845853303a805108c5ead6ac` (⑤'s GATE(④) PASS on OPS-0002; verified current HEAD via `github__list_commits` at read time). **Mid-turn interleave, anticipated and verified:** the dispatch pre-announced a parallel `[①-EP]` ops commit; it landed as `1f7c86d058880d94b859b89ee1b4c28fed592908` before ③'s push, touching ONLY four ops docs (`CHANGELOG.md`, `DECISION_LOG.md`, `STUDIO_STATUS.md`, `TASK_QUEUE.md` — verified via `github__get_commit` file list), none of ③'s cited sources. **③'s commit therefore lands on parent `1f7c86d0`.** The two ops cells the spec cites (TASK-0018 approval column "YES (locks later, per-item)"; TASK-0009's "<4s = editorial inserts" harmonization note) and the DEC-0008/DEC-0009 PENDING rows were re-verified unchanged at `1f7c86d0` after the interleave.

**Dispatch note for the record:** this is the SECOND dispatch of TASK-0018 — the first aborted mid-run on a platform auth error (401) with **zero commits**; ③ re-verified via `github__list_commits` that no `[③-VISUAL]` commit existed on `main` before this turn, so there was no partial repo state to reconcile. All source documents were re-verified byte-identical to HEAD blobs (git blob-sha1 comparison against the `9345a5ef` tree) before being cited.

---

## What was done

### TASK-0018 — Trailer v2 gap specs, DRAFT (DONE)

Produced **`studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md`** — one coherent DRAFT PROPOSAL document covering exactly the six keyframe gaps the CYCLE-0002 work order assigned (three environment plates, monster/extinction-"content" design, registry-card UI). Spec format per Handbook v1 §15.1/§15.4/§15.5/§16; `Art_Direction.md` (LOCKED v3, DEC-0003/DEC-0004) named as master over everything in the file. **Spec-draft ONLY: no locks, no generation, no canon edits** — every canon-silent choice is marked PROPOSAL and queued for the Owner.

Per-KF one-liners:

- **KF-03 (ENV-SPEC-A):** a matched PAIR of mid-conversion wide plates — A1: the prologue's 8.0 settlement (well scaffold, chalk-name tank, cookfire) with the FX-PATCH wall entering as a 20–25° diagonal front (angle = PROPOSAL); A2: a festival-dressed Haeseong street converting 9.0→10.0 at the same angle/direction so the S06 match-cut lands. All dressing canon-cited (prologue, Ch.1, script P30/P6, Environment_Bible, Effects_Bible).
- **KF-04 env half (ENV-SPEC-B):** the two seam-side context plates canon fixes — B1: the well-scaffold edge, lamplit night (8.0); B2: Cha's Kitchen exterior doorway, night rain, lantern (9.0; this IS Environment_Bible's already-listed "tram depot alley" gap, scoped to the doorway). Cha's v3 kit + the FX-PATCH-on-character ruling remain the KF's other blockers — cross-referenced, not re-spec'd.
- **KF-12 (ENV-SPEC-C):** the centerpiece first+last frame pair as one location wearing two worlds — C1: post-patch festival-night Haeseong street (10.0 palette); C2: rain-soaked 2.0 murim pass with a per-mass counterpart map (rails→cart-ruts, poles→waymarkers, clocktower→gate-tower, etc.). C2 would be the first visual canon for a dead world (palette + crackless-sky choice explicitly flagged as Owner-owned, OQ-VIS-7).
- **KF-07 (Part II):** monster design language "UNRENDERED CONTENT" — flat ink-black mass, confident silhouette, square-static fringe at edges only, exactly one high-detail zone; no accent/glow (accents belong to characters). Silhouette-through-smoke shows shape only; full anatomy withheld. Two named alternates offered; Moderator-distinctness rule stated so the static vocabulary can't collide with KIT-CHAR-006.
- **KF-08 attacker half (Part II):** one claw/blade-arm in frame only, caught in Han's proposed RIGHT (sword) hand; the body stays off-frame so KF-07's withhold survives; Han's half rides entirely on locked CHAR-001 assets. Fair-play binding stated: the trailer silhouette must be an honest outline of the eventual locked design — withhold, never lie.
- **KF-15 (Part III):** registry-card UI "LEDGER UNDER REVISION" — a Soryeong Academy paper roster card being overwritten live by the established cyan-on-black system-plaque layer, then stamped REWRITTEN; stamp/status text as overlay layers per the lettering law; three-tier type hierarchy; ×3 stamp beat map for S01; unnamed students proposed (Q-01 fair-play hazard documented). Original design; §III.2 records the PMU genre grammar precisely so ⑤ can verify we designed away from it.

### Turn mechanics — deliberately NOT performed this turn (declared deviation, not an omission)

Per ①'s CYCLE-0002 night-shift dispatch, **the Conductor holds the ops lease this cycle**: ③ did NOT touch `STUDIO_STATUS.md`, `CHANGELOG.md`, `TASK_QUEUE.md`, `DECISION_LOG.md`, or `OPEN_QUESTIONS.md` — ① performs all queue/status/changelog mechanics at cycle close. This deviates from the A1.4 pattern ②'s CYCLE-0002 turn followed (② updated status/changelog/queue itself); it is declared here plainly so GATE(③) evaluates lane compliance against the dispatch, not against the prior pattern.

---

## Reference-library use disclosure (OPS-0002 / CANON_REGISTRY §7 compliance)

- ③ read `studio/07_Repository/REFERENCES/PMU_style/INDEX.md` and viewed **five** shortlist strips read-only: PMU-086-D, PMU-142-D, PMU-144-D (card-UI grammar — informs the §III.2 originality clause), PMU-144-B (beast staging/legibility), PMU-103-B (environment staging). Each file was hash-verified byte-identical to its INDEX §A SHA-256 **before** viewing.
- Use was mood/line-weight/paneling sensibility calibration only. **No panel composition, pose, or design was copied or traced; the specs' design language is original to PATCH 10.0, and the card spec explicitly enumerates the genre conventions it declines.** No Drive file ids or links appear in any file this turn touched (licensing containment per OPS-0002; the Owner's residency ruling is queued as DEC-0015, PENDING in `DECISION_LOG.md` as of `1f7c86d0`).

## What the ⑤ gate should check

1. **Citation discipline** — every load-bearing canon claim in the spec carries a file+section pointer. Recommended spot-checks: the prologue/Ch.1 quotes in ENV-SPEC-A1/B2 (chalk-name and doorway lines), script P30/P32/P6 pointers, the FX-PATCH/FX-TESTIMONY/FX-QI verbatims against `Effects_Bible.md`, and the CANON_REGISTRY §2/§4 gap quotes.
2. **Label discipline** — DRAFT PROPOSAL banner at top plus per-Part banners; every canon-silent choice marked PROPOSAL; OQ-VIS-1…12 file-local numbering only (no official Q-numbers minted — ④ is appending from Q-15 this cycle under TASK-0019, so ③ minting numbers would collide).
3. **Night rules / scope** — no LOCK, no generation, no canon edit, no restructure; purely additive (two NEW files, zero existing files modified). No UNDECIDED item (Q-01…Q-14) or PENDING decision (DEC-0008/0009) resolved. Sealed twist bank not referenced, reconstructed, or hinted at (spec §II.4 carries an explicit sealed-material statement).
4. **Flat-2D law compliance** — every visual proposal is expressed inside Art_Direction.md's locked doctrine (ink/flat/cel constraints restated per plate; monster readability defined as silhouette-value discipline, not rendering).
5. **Lane compliance** — the commit touches exactly two files: `studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md` (new) and `studio/06_Operations/HANDOFFS/CYCLE-0002-VISUAL.md` (new — this file). Nothing else. No ops docs, no `manuscript/`, no `studio/07_Repository/`, no existing `02_Art`/`04_Storyboards` file modified.
6. **Commit hygiene** — ONE commit, `[③-VISUAL]` prefix, descriptive message. (The EP work order budgeted "one commit" for ③; the handoff rides in the same commit, matching ②'s CYCLE-0002 pattern.)

## ⑤-GATE MANIFEST (exact)

| # | Commit | Files |
|---|---|---|
| 1 | `[③-VISUAL] CYCLE-0002 ③: TASK-0018 Trailer v2 gap specs DRAFT …` (this turn's only commit, on parent `1f7c86d0` — see base-commit note above) | `studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md` (new) · `studio/06_Operations/HANDOFFS/CYCLE-0002-VISUAL.md` (new) |

Deviations, declared plainly:
1. **No ops-doc turn mechanics** (see above — Conductor holds the ops lease this cycle per dispatch; ① closes the books).
2. **Deliverable path** — the ①-EP work order names `studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md` and that is what was written. The KF Production Plan itself names no specs-file location. (③'s dispatch carried a fallback default of `studio/04_Storyboards/` "if unspecified" — the work order's explicit path wins; recorded here so nobody hunts for a phantom second file.)
3. Nothing else deviates: no PARTIAL work, no skipped scope — all six KFs' gaps are covered in the one deliverable.

## Open questions queued for the Owner (proposals only — ① assigns official numbers at close)

Twelve Owner choices are consolidated in the spec's bottom table (OQ-VIS-1…12), each with ③'s freely-rejectable recommendation. The three heaviest: **OQ-VIS-7** (KF-12's C2 frame would set the FIRST visual canon for dead-world 2.0 — palette + whole-sky choice; Owner must own it), **OQ-VIS-9** (monster design language selection + whether square-static on monster edges is acceptable next to the Moderator's proposed face-static), **OQ-VIS-11** (registry-card concept confirmation + the named-vs-unnamed-cards fair-play call against Q-01). Also queued for ①: OQ-VIS-12 recommends two follow-on TASK rows (full monster-design commission; system-UI family kit).

## Next department: ④ Repository & Canon Management (after GATE(③))

- ④'s TASK-0019 (registry stubs completion + OPEN_QUESTIONS cross-links from Q-15 + INDEX refresh) is independent of this deliverable; ④ may want to reflect the new file in INDEX and, when appending Q-15+ entries, can draw the candidate items directly from the spec's consolidated OQ-VIS table (①'s call which get formalized).
- No cross-lane edit is requested of ④ by this turn.

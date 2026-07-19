# Turn Handoff — CYCLE-0002-④ (Repository & Canon Management)

**From:** ④ Repository & Canon Management
**To:** ⑤ QA (GATE(④), per DEC-0013) · ① Executive Producer (dispatching conductor)
**Date:** 2026-07-19 · **Mode:** Conductor Mode, night-shift run (Night Rules §A2.4 in force) · **Task:** TASK-0019
**Base commit this turn started from:** `31b36ee39044c8d545a588443add7137c6d404d9` (⑤'s GATE(③) PASS; verified as HEAD via clone + `git fetch` at read time AND re-verified immediately before the content push — no interleave occurred; the content commit's sole parent is `31b36ee3`).

---

## What ④ did this turn (records only — compile, cite, never author)

### 1. CANON_REGISTRY §3 Locations/Environments — STUB completed

- **Nine rows added** to the main table: Haeseong market/fish street · tram depot alley (Cha's Kitchen exterior) · harbor & harbor clocktower · the three old bell towers (harbor/garrison/quad) · Han's dorm room · 8.0 set component plates (settlement wide / well scaffold / water-tank close / cookfire) · POST-PATCH (10.0) damaged-variant class · palimpsest set-pieces · Renewal chapel/guild hall/auction house. Every canonical fact is quoted or close-paraphrased from `00_prologue.md` / `01_the_ninth_world.md` / `Master_Project_Bible.md` / `story_bible.md` / `Environment_Bible.md` / `CONTINUITY_LEDGER.md` / `ep1_v3_script.md` with per-row pointers. This mirrors the FULL `Environment_Bible.md` "Locations still needing plates" gap list, closing the CYCLE-0001 stub exactly as its note 4 defined it.
- **Dead-world referenced locations minor registry added** (mirrors §1's dead-world characters pattern): the mountain (2.0) · the tower (3.0) · gate districts (5.0) · excavation-arc destinations — plus an explicit statement that 1.0/4.0/6.0/7.0 have NO located places in canon (documented silence, nothing invented).
- **Gap discipline:** every location without a LOCKED plate is recorded as a documented gap (the registry records gaps; it does not commission plates). Where ③'s new `Trailer_v2_Gap_Specs_DRAFT.md` (TASK-0018, gate-passed at `31b36ee3`) proposes a plate for a gap (ENV-SPEC-A1/A2, B1/B2, C1/C2), the row cites it strictly as **DRAFT PROPOSAL — not canon, awaiting per-item Owner lock**. Canon-silent fields (e.g., all visual/scene detail for the Renewal buildings; all dead-world visuals) are marked UNDECIDED/silence with the nearest open-question cross-link where one exists (Q-06 for the auction-house economy; T2-sealed adjacency for the bell towers' tuning origin).
- **§3 stub note replaced** with a completion note stating the above (the only §3 line removed).

### 2. CANON_REGISTRY §4 Powers/Effects — STUB completed

- **Two system-adjacent rows added:** Remnant economy (auction/"Ledger" — existence LOCKED, all mechanics UNDECIDED deliberately per Q-06) and Patch-scarring/leak phenomenon (both baseline instances recorded; Ha-eun's meaning recorded as T2-sealed with no inference; why-now recorded as a sealed open mystery).
- **Per-character/entity ability inventory added** (10 rows + a staff-silence note): Han's carried internals / named-skills pointer / Requiem uniques / non-system competencies; Si-woo's sword-Etude (documented silence: no named skill exists for him) and patch-scar; Ha-eun (scholarly abilities only; anomalies recorded, meaning sealed); Cha (rewrite-resistant residue, explicitly "not a power"); Moderators (pointer rows); extinction monsters (no abilities specified anywhere — documented silence). Closing note records that Im Dan-bi/Baek Do-yun/minor cast have no canon abilities. The named-skill count in canon remains exactly three, all Han's — the inventory documents that fact rather than padding it.
- **Two existing §4 rows updated (the only §4 lines removed), both §4-local and required by the task:**
  1. *Effects-grammar extension questions* — its "not yet in OPEN_QUESTIONS.md" clause was factually retired by this turn's own QA-09 work: now cites **Q-17/Q-18**; status `UNDECIDED (Q-17 / Q-18)`.
  2. *Monster / "extinction content" design* — its "zero visual spec exists at any status" claim became false at HEAD when ③'s gap specs landed: claim re-scoped to "at this registry's CYCLE-0001 build," with a CYCLE-0002 record-only update citing PART II as DRAFT PROPOSAL; status remains UNDECIDED (no approved spec).
- **§4 stub note replaced** with a completion note.

### 3. CANON_REGISTRY frame (additive only)

A second build note (CYCLE-0002 ④, TASK-0019) was added under the CYCLE-0001 build note, and **cross-cutting note 5** was appended recording: which stubs closed, which remain (minor/dead-world CHARACTERS, §1), the Q-15–Q-18 mapping, the newly referenced UNDECIDED items, and the one known-stale line deliberately left untouched (below). Notes 1–4 and the CYCLE-0001 build note are byte-identical.

### 4. OPEN_QUESTIONS.md — QA-09 cross-links (LANE EXCEPTION, declared)

- **Lane exception:** `studio/06_Operations/OPEN_QUESTIONS.md` is ①'s ops area; this turn's work order explicitly authorized ④ to write it, **scoped strictly to appending the QA-09 cross-links and new Q-15+ rows.** That is the only ops file touched, and only by appending.
- **Four pointer rows appended — exactly the four items QA-09 names, nothing more:** Q-15 (CM-01 cross-link) · Q-16 (SW-01 cross-link) · Q-17 (FX-PATCH-on-character, KF-04) · Q-18 (FX-ETUDE-FAIL, KF-06). Pointer-not-copy per QA-09's own recommendation: each row cites `CANON_REGISTRY.md` / `Trailer_v2_KF_Production_Plan.md` / `REVIEWS/CYCLE-0001_REVIEW.md` for substance rather than duplicating it. Q-01…Q-14 rows are byte-identical (verified by diff: the file's change is +4 lines, −0).
- **Collision check (task-required):** grepped the entire tree at `31b36ee3` for `Q-15`…`Q-29`. Result: **no minted Q-number ≥ Q-15 existed anywhere.** The only matches were reservations of this very lane — ③'s `Trailer_v2_Gap_Specs_DRAFT.md` header and `CYCLE-0002-VISUAL.md` ("④ is appending from Q-15… ③ mints nothing to avoid collision"), ①'s `CYCLE-0002-EP.md` ("next free numbers Q-15+"), ⑤'s `CYCLE-0002_GATE-VISUAL.md`, and the TASK-0019 queue row itself. No numbers were skipped; Q-15–Q-18 minted contiguously.
- **NOT minted, deliberately:** ③'s OQ-VIS-1…12 remain file-local proposal numbers — not absorbed, renumbered, or officialized (① decides formalization at cycle close, per ③'s own handoff). No Q-numbers were minted for the §3/§4 documented gaps either: those are already tracked in `Environment_Bible.md`'s gap list, the KF plan, and the OQ-VIS queue, and minting parallel numbers would duplicate ledgers — the opposite of what QA-09 asked for.

### 5. INDEX.md refresh (additive + corrective listing updates only; no restructure)

- **14 rows added:** `Trailer_v2_Gap_Specs_DRAFT.md` (02_Art) · 7 handoffs (`CYCLE-0001-QA`, `OPS-0001-EP`, `OPS-0002-REPO`, `CYCLE-0002-EP/-LORE/-VISUAL`, and this file) · 4 REVIEWS files (CYCLE-0001_REVIEW + three DEC-0013 gate reviews) · `ep2_outline_proposal.md` (WORK_IN_PROGRESS) · `REFERENCES/PMU_style/INDEX.md` (07_Repository).
- **13 corrective line updates:** as-of commit → `31b36ee3`; marker-convention sentence; Handbook row (+Amendment 2, v2.1); TASK_QUEUE row (→ TASK-0020, stale "this ④ turn" removed); DECISION_LOG row (→ DEC-0015; 0008/0009/0015 PENDING); OPEN_QUESTIONS row (→ Q-18); CYCLE-0001-REPO row ("this ④ turn" → "the CYCLE-0001 ④ turn"); REVIEWS directory row (no longer "empty"); 07_Repository section heading ("this turn" marker retired, "references" added); CANON_REGISTRY row (seven sections incl. §7; §3/§4 completion); `ep1_adaptation_variance.md` row (IN_REVIEW → ACCEPTED, QA-04 correction noted); both "Notes on this index" bullets (off-repo PMU pointer; the stale this-turn constraint sentence).
- **Both NEW-since-dispatch items are reflected** as required: CANON_REGISTRY §7 Reference Libraries (OPS-0002, `beac8a62`) and ③'s `Trailer_v2_Gap_Specs_DRAFT.md` (`ad1ce4e7`, marked DRAFT PROPOSAL in its row).

## Deviations & judgment calls, declared plainly

1. **Two commits, not one.** `CYCLE-0002-EP.md` budgeted "one commit" for ④; the TASK-0019 dispatch authorizes up to 3 + handoff. Content landed as ONE commit exactly as the EP budget anticipated; this handoff is a second commit because its ⑤-gate manifest must cite the content commit's SHA and blob hashes, which cannot exist before that commit does (the same chicken-and-egg QA-12 documented; OPS-0002 used the same trailing-handoff pattern).
2. **INDEX lists this handoff one commit early.** The `CYCLE-0002-REPO.md` row was written into INDEX in the content commit and the file lands in this immediately-following commit of the same turn — same-turn self-listing precedent as the CYCLE-0001 INDEX build. Between the two commits (minutes), that one row pointed at a not-yet-present file.
3. **Known-stale line left byte-identical (edit discipline):** §2's "Registry cards" row still reads as if no registry-card visual design exists at any status — true at CYCLE-0001 build, now predates ③'s PART III DRAFT PROPOSAL. §2 is outside this turn's authorized stub scope, so the row was NOT touched; the staleness is recorded in cross-cutting note 5 and here, and queued as a mechanical-fix candidate for a future ④ pass over §2.
4. **Registry rows referencing ③'s specs were double-checked for label discipline:** every citation of `Trailer_v2_Gap_Specs_DRAFT.md` in §3/§4 carries "DRAFT PROPOSAL"/"PROPOSED, not canon" language inline. Nothing PROPOSED was recorded as fact; no OQ-VIS recommendation was repeated as a decision.
5. **New observation surfaced, NOT recorded in the registry (outside this turn's stub scope) — candidate CONFLICT-FOR-QA for ⑤/②:** `manuscript/chapters/01_the_ninth_world.md` has Ha-eun say "Professor Im says mana has always sung…" and then "**She** gave me the Chorus catechism and a biscuit," while `Character_Bible.md` CHAR-005 specifies Proctor/Prof. Im Dan-bi as "~40s **male**" (Master_Project_Bible §7 and story_bible.md state no gender). Either the library scene's "Professor Im" is a second, undesigned Professor Im, or two locked-lane sources disagree on Im Dan-bi's gender. Registering it properly means touching §1 (not authorized this turn) — flagged here with both pointers for ⑤ to adjudicate or a future ④ registry pass to record as IM-01. No Q-number minted for it (not within this turn's QA-09 authorization).
6. **No writes anywhere else.** STUDIO_STATUS.md, CHANGELOG.md, TASK_QUEUE.md, DECISION_LOG.md untouched (① holds the ops lease and does cycle-close mechanics). No manuscript/, 02_Art/, 04_Storyboards/, readers/, REVIEWS/ writes. No locks, no retcons, no decisions made or implied, no Drive ids/links anywhere (DEC-0015 containment), no sealed material consulted or characterized beyond existing "sealed" pointers.

## ⑤ GATE(④) manifest — exact files / commits / blobs

| # | Commit | Files (blob SHA-1 at that commit) | Shape |
|---|---|---|---|
| 1 | `cedeb5841e508c6ff3ea36dba89f8865fb2dbb12` — `[④-REPO] TASK-0019: complete CANON_REGISTRY §3/§4 stubs + OPEN_QUESTIONS Q-15–Q-18 + INDEX refresh` (sole parent `31b36ee3…`) | `studio/07_Repository/CANON_REGISTRY.md` → `d0323b8dbcf108c371a45499394c09df0b625749` · `studio/07_Repository/INDEX.md` → `677669fb616245d447c9206bc79a227880ef45ff` · `studio/06_Operations/OPEN_QUESTIONS.md` → `1efc9529aaff6019bf0de8178d5cedafff7a63bf` | CANON_REGISTRY +44/−4 (the 4 removed lines are exactly: §3 stub note, §4 stub note, FX-extension-questions row, monster-design row — all replaced in-place; all other lines byte-identical) · INDEX +27/−13 (13 corrective replacements + 14 new rows) · OPEN_QUESTIONS +4/−0 (pure append) |
| 2 | this commit — `[④-REPO] HANDOFFS: add CYCLE-0002-REPO` | `studio/06_Operations/HANDOFFS/CYCLE-0002-REPO.md` (new file; SHA in this commit's tree) | pure addition |

**Losslessness verification performed by ④ after commit 1:** local `git hash-object` (= sha1(`"blob <len>\0"` + bytes)) of all three files matches GitHub's reported blob SHAs at `cedeb584` exactly (values above); commit parent verified `31b36ee3`; per-file numstat verified against the local diff before push. Re-derivable by ⑤ via `github__get_commit`/`git ls-tree`.

## What was left gap-marked rather than filled (and why)

Everything the sources are silent on: all missing environment PLATES (documented gaps — plates are ③'s to spec and the Owner's to lock, never the registry's to fill); Renewal chapel/guild hall/auction house visual+scene detail (canon gives factions only); all dead-world visuals including the 2.0 palette (first definition exists only as ③'s OQ-VIS-7 proposal — recorded as awaiting Owner); monster abilities/taxonomy (canon silent); Si-woo's named skills, Ha-eun's Etude ability (canon silent — recorded as documented silences); Ha-eun's anomaly meaning and the bell towers' tuning origin (T2-sealed — recorded as sealed, zero inference); why patches leak now (sealed open mystery). Per the razor: no lore was authored, no UNDECIDED item resolved, no proposal promoted.

## Next: ⑤ GATE(④), then ① cycle close

- ⑤ can opcode-diff commit 1 against the shape table above; every registry change outside §3/§4 is one of: the added build note, added note 5 — nothing else.
- ① at cycle close: TASK-0019 status cell, CHANGELOG/STATUS mechanics (ops lease); decide whether to formalize any OQ-VIS-1…12 items (Q-19+ are the next free numbers); consider deviation item 5 (Professor Im) for ⑤'s queue; §2 registry-cards row mechanical fix remains a queued candidate for a future ④ turn.

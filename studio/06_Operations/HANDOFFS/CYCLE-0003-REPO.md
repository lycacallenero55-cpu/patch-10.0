# Turn Handoff — CYCLE-0003-④ (Repository & Canon Management)

**From:** ④ Repository & Canon Management
**To:** ① Executive Producer (dispatching conductor) · ⑤ QA (cycle-end FULL-CYCLE review per Amendment 3 / DEC-0016 — no per-department gate follows this turn)
**Date:** 2026-07-19 · **Mode:** Conductor Mode, night-shift tick (Night Rules §A2.4 in force, carried forward by Amendment 3) · **Task:** TASK-0023
**Base commit this turn started from:** `04f08e824573a4b5f05be43d67516ca1508980d2` (①'s session tick; verified as HEAD via clone at read time AND re-verified via `github__get_commit` immediately before the content push — no interleave occurred; the content commit's sole parent is `04f08e82…`).

---

## What ④ did this turn (records only — compile, cite, never author; all four dispatch items)

### 1. CANON_REGISTRY §2 "Registry cards" row — refreshed, record-only (the staleness note 5 flagged)

- **Diff shape: one line replaced in place** (the row itself). On the §4 monster-row precedent from TASK-0019: the stale claim ("a visual UI design that does not currently exist anywhere in the repo at any status") is re-scoped to "at this registry's CYCLE-0001 build," and a **CYCLE-0003 update (record only)** clause now records that ③'s DRAFT PROPOSAL exists — `studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md` PART III ("LEDGER UNDER REVISION" recommended, pure-plaque/pure-paper alternatives named; stamp/bracket, interim-typeface, and named-vs-unnamed-students choices queued via ③'s OQ-VIS-11; family kit via OQ-VIS-12), gate-passed at `31b36ee3`.
- **Nothing decided:** the row states "PROPOSED, not canon: no design exists until the Owner selects and locks"; status cell is `UNDECIDED (no approved spec; UI-concept PROPOSAL pending Owner — Q-22)`. Pointers added: Gap_Specs PART III (DRAFT PROPOSAL) + `OPEN_QUESTIONS.md` Q-22. The Q-22 formalization and TASK-0022 (PROPOSED) queue position are compiled from `OPEN_QUESTIONS.md`/`TASK_QUEUE.md`, not asserted. No design content copied beyond the proposal's name and its queued-choices list (same depth as the monster-row precedent).

### 2. CANON_REGISTRY — QA-239 quote-form nits, exactly the three named cells

- **§3 dead-world "The tower (3.0)" row:** quoted string now `"had once been a promise between apprentices"` — byte-exact substring of Ch.1:109 ("A ring of chalk-white stone that had once been a promise between apprentices.").
- **§3 dead-world "The mountain (2.0)" row:** quoted string now `"The man who could cut rain"` — byte-exact substring of Ch.1:107, the keepsake passage that row cites.
- **§4 "Cha Mi-ran — rewrite-resistant residue" row:** `manuscript/bible/story_bible.md` "Cast" added to the source-pointer cell (the file whose sentence "The patch failed to rewrite how she salts broth." the row quotes verbatim, modulo the conventional mid-sentence lowercase). Quote text unchanged, per QA-239's own prescription (citation add, not requote).
- **Cross-cutting note 6 appended** (the registry diff's only added line) recording items 1–2, the untouched adjacent candidate (deviation (c) below), and the razor attestations. Every other registry line — including §1, §5–§7, notes 1–5, and both build notes — is byte-identical; total registry diff **+5/−4**.

### 3. REFERENCES/PMU_style/INDEX.md polish (QA-218 + QA-219) — diff +4/−4, all in place, no rows deleted

- **QA-218:** §A heading → "28 reviewed rows (27 effective reference strips)"; a **Count correction (QA-218, applied CYCLE-0003 ④)** sentence added to the §A intro (names PMU-142-A as the ch.142 site-banner capture artifact; effective set **27**; ch.142 contributes 3 usable references, not 4; row kept for provenance); the PMU-142-A row's Ref cell marked `⚠ *(capture artifact — provenance only, not a reference)*`. Row, SHA-256, and description untouched.
- **QA-219:** §B.2 thumbnail sub-count "~180 hash-named … files" → "**211** hash-named … files raw / **172** distinct names, the same thumbnails recurring across the 7 folder captures — counts verified by ⑤, QA-219". The enclosing exact totals (260 / 345 / 5 / 85 / 357), which ⑤ verified correct, are untouched.

### 4. studio/07_Repository/INDEX.md refresh — diff +15/−9 (9 corrective in-place replacements + 6 added rows; no restructure)

- **Corrective replacements (9):** as-of pointer → `04f08e82…` (CYCLE-0003 ④ refresh, TASK-0023); marker-convention sentence; Handbook row (Amendments 1–3; Amendment 2 gate mechanics SUPERSEDED-with-pointer to DEC-0016/Amendment 3, §A2.4 carried forward); TASK_QUEUE row → TASK-0024; DECISION_LOG row → DEC-0016 (0008/0009/0015 still PENDING); OPEN_QUESTIONS row → Q-22 (Q-19–Q-22 minted by ① at CYCLE-0002 close); CYCLE-0002-REPO row's stale "this turn" marker retired; PMU_style INDEX row (reflects this turn's QA-218/QA-219 corrections); "Last refresh" notes bullet.
- **Rows added (6):** `HANDOFFS/CYCLE-0002-CLOSE.md` (new, CYCLE-0002 ①) · `HANDOFFS/CYCLE-0003-EP.md` (new, CYCLE-0003 ①) · `HANDOFFS/CYCLE-0003-LORE.md` (new, CYCLE-0003 ②) · `REVIEWS/CYCLE-0002_GATE-REPO.md` (new, CYCLE-0002 ⑤) · `WORK_IN_PROGRESS/professor_im_investigation_DRAFT.md` (new, CYCLE-0003 ②, marked **DRAFT, records only; resolves NOTHING**) · `HANDOFFS/CYCLE-0003-REPO.md` (this file, self-listed — deviation (b)). This is the complete new-file set since the last refresh base `31b36ee3` (verified by tree diff `31b36ee3..04f08e82`), plus the self-listing.

## Deviations & judgment calls, declared plainly

1. **Two commits (content + this handoff).** Dispatch authorized 1–2. Same trailing-handoff rationale as OPS-0002/CYCLE-0002: the ⑤ manifest below cites the content commit's SHA and blob hashes, which cannot exist before that commit does.
2. **INDEX lists this handoff one commit early** — same-turn self-listing, CYCLE-0001/CYCLE-0002 ④ precedent (QA-235 verified it as declared last cycle). Between the two commits (minutes), that one row pointed at a not-yet-present file.
3. **Adjacent quote-form candidate left byte-identical (edit discipline):** the registry's §1 Cha "Identity" row quotes the same salts-broth sentence, also without the story_bible pointer. QA-239 names exactly three cells and the §1 row is not one of them, so it was NOT touched; logged here and in cross-cutting note 6 as a mechanical-fix candidate for a future ④ pass.
4. **QA-239 claim vs repo reality, one nuance (adapted minimally, flagging for ⑤):** the string "a man who could cut rain" IS verbatim elsewhere in Ch.1 — line 7, "he had studied under a man who could cut rain." QA-239 measured the mountain row against its cited pointer (the keepsake passage, Ch.1:107: "The man who could cut rain."), so the row now carries the keepsake-passage form exactly as prescribed. No citation change was needed; recorded so ⑤'s re-verification doesn't trip on the line-7 coincidence.
5. **PMU INDEX §C left byte-identical:** §C still reads "Reviewed: 28 strips (4 per chapter…)" and "the 28 rows in §A". QA-218's recommended action targets §A's heading/half-line, and the dispatch's wording-stays-minimal constraint reads on that; the §C echo of the corrected framing is logged as a candidate, not fixed.
6. **CANON_REGISTRY §7 PMU row left byte-identical:** its "28 of them integrity-verified and visually reviewed" remains literally true (28 files were verified and reviewed); the reference-set framing correction lives at the PMU INDEX per QA-218's own recommendation. Candidate only if ⑤ judges the echo material.
7. **Stale Handbook subtitle noticed, not fixed (①'s lane):** `00_OPERATING_HANDBOOK.md` line 2 still reads "(Amendments 1–2 + retained v1 body)" and the version note still says "Amendments 1 and 2 below are binding," though Amendment 3 now exists and is binding. Outside ④'s lane under this dispatch — flagged to ① as a mechanical-fix candidate.
8. **No new registry build note:** this pass is mechanical (4 cells + 1 note), not a section build; it is recorded as cross-cutting note 6 and inside the refreshed cells themselves rather than as a third top-of-file build note. Judgment call, reversible.
9. **No writes anywhere else.** STUDIO_STATUS/CHANGELOG/TASK_QUEUE/DECISION_LOG/OPEN_QUESTIONS untouched (①'s ops lease — no lane exception this turn); no manuscript/, 02_Art/, 04_Storyboards/, readers/, REVIEWS/ writes; no locks, no retcons, no decisions made or implied, no Q-numbers minted, no Drive ids/links anywhere (DEC-0015 containment; token-level scan of all changed files run before push), no sealed material consulted or characterized beyond existing "sealed" pointers.

## ⑤ full-cycle-review manifest — exact files / commits / blobs (④'s turn)

| # | Commit | Files (blob SHA-1 at that commit) | Shape |
|---|---|---|---|
| 1 | `201edb3f739ae760827c6cea7ed0627209ccd817` — `[④-REPO] TASK-0023: registry mechanical pass …` (sole parent `04f08e824573a4b5f05be43d67516ca1508980d2`) | `studio/07_Repository/CANON_REGISTRY.md` → `f8da9aa2092d5fddeca5faae244f326b7e40fd1f` (61,928 B) · `studio/07_Repository/INDEX.md` → `250062811617a82e14a36f75f91ee9d0368bf22d` (29,562 B) · `studio/07_Repository/REFERENCES/PMU_style/INDEX.md` → `bbf0d21d9952f92aab14986c8a92c959e5556c21` (17,640 B) | CANON_REGISTRY **+5/−4** (the 4 removed lines are exactly: §2 registry-cards row, §3 mountain row, §3 tower row, §4 Cha row — all replaced in place; the 1 net-new line is cross-cutting note 6; every other line byte-identical) · INDEX **+15/−9** (9 corrective replacements + 6 new rows) · PMU_style INDEX **+4/−4** (heading, §A intro sentence, PMU-142-A Ref cell, §B.2 sub-count — all in place; no row deleted) |
| 2 | this commit — `[④-REPO] HANDOFFS: add CYCLE-0003-REPO` | `studio/06_Operations/HANDOFFS/CYCLE-0003-REPO.md` (new file; SHA in this commit's tree) | pure addition |

**Losslessness verification performed by ④ after commit 1:** local `git hash-object` (= sha1(`"blob <len>\0"` + bytes)) of all three files matches GitHub's independently reported blob SHAs at `201edb3f` exactly (values above); commit parent verified `04f08e82…`; per-file numstat verified against the local diff before AND after push (`git diff 04f08e82..origin/main`); local worktree vs `origin/main` diff empty. Re-derivable by ⑤ via `git ls-tree` / `github__get_commit`.

**Suggested ⑤ checks (cycle-end review):** opcode-diff commit 1 against the declared four cells + note 6; re-verify the two normalized quotes character-for-character against Ch.1:107/109 and the Cha pointer against `story_bible.md` "Cast" (mind deviation item 4's Ch.1:7 coincidence); QA-218/QA-219 numbers against `REVIEWS/OPS-0002_GATE-REPO.md` evidence (27 effective / 211 raw / 172 distinct); the six INDEX additions against the tree diff `31b36ee3..04f08e82`; token-level Drive-id scan of the changed files.

## What was left as-is (and why)

Everything outside the four dispatch items: §1's Cha "Identity" row and the PMU §C/registry-§7 echoes (deviations 3/5/6 — outside the named cells); the Gap-Specs INDEX row's OQ-VIS sentence (still true; Q-20/Q-21/Q-22 now cover the three heavyweight items, recorded in the OPEN_QUESTIONS row instead); the Handbook subtitle (①'s lane, deviation 7). Nothing UNDECIDED was resolved: Q-22 stays open and pending the Owner; the §2 row records a proposal's existence, not a selection.

## Next

- **⑤** reviews this turn as part of the CYCLE-0003 full-cycle review (② + ④ turns) at cycle end, per Amendment 3.
- **①** at cycle close: TASK-0023 status cell + CHANGELOG/STATUS mechanics (ops lease); the Handbook-subtitle mechanical fix (deviation 7) is ①'s to take or queue; QA-240 remains with ② (done this cycle per ②'s handoff); the §1 Cha-row pointer candidate rides along on ④'s next registry pass.

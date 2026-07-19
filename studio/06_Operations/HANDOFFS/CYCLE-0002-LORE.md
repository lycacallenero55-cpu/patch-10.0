# Handoff — CYCLE-0002 ② Lore Department

**From:** ② Lore Department
**To:** ⑤ QA (GATE(②), per Amendment 2 §A2.2) — then back into the conducted cycle (③ Visual next, per the cycle order)
**Date:** 2026-07-19
**Base commit this turn started from / built against:** `928dd419ca6a0fbd85aa30a1ecc739bccb773b7c` (verified current HEAD via `github__list_commits` at both the start and end of this turn — no SHA conflict occurred; no re-fetch/re-apply was needed).

---

## What was done

### TASK-0008 — QA-04 correction (DONE)

Corrected `manuscript/manhwa/ep1_adaptation_variance.md` per `CYCLE-0001_REVIEW.md`'s QA-04 finding. The finding: the record previously stated the "For the well" callback line was rendered as text in NEITHER the script nor the readers. This was a misreading of a source the record itself correctly cited — `ep1_v3_script.md` P40 explicitly reads `💭 "She refuses tips. So I hide them. For the well."` — the callback IS present as script text. It is dropped only at the readers layer (`episode1_part2.html`: "SHE ALWAYS REFUSES TIPS. SO I LEAVE THEM WHERE SHE'LL ONLY FIND THEM LATER." — no "for the well" anywhere).

**Two spots were surgically corrected**, both flagged by the CYCLE-0001_REVIEW.md verdict block as needing the same fix:
1. The variance table's "Hidden tip under the bowl; 'For the well,' he didn't say" row (Notes column).
2. Synthesis finding #2 in "Top continuity-risk findings (synthesis)," which made the same slightly-imprecise claim in its own words.

Both now state precisely: the callback is present in adaptation-canon (script) text, and dropped specifically at the derivative-output (readers) layer — not absent from both. The practical, currently-published conclusion is unchanged (per `SOURCE_OF_TRUTH.md`'s precedence rule, readers supersede script wording, so the *currently published* EP.1 genuinely lacks the echo either way) — only the "in either the script or the readers" phrasing was wrong, and only that phrasing was touched.

A one-line revision note was appended at the very bottom of the file: **"Corrected per CYCLE-0001_REVIEW QA-04, CYCLE-0002 ②."**

Nothing else in the file changed — same ~30-row table (every other row byte-identical), same six synthesis findings (finding #2's other sentences unchanged), same header/labels, same "Dialogue-wording precedence summary" section (its own representative-examples list already correctly described this exact row as "The well-callback payoff line: script 'For the well' (P40, present as text) → readers... (dropped)" — consistent with the correction, not contradicting it), same "Cross-references to OPEN_QUESTIONS.md" section.

### TASK-0017 — EP.2 "Last Day" outline proposal (DONE)

Produced `studio/06_Operations/WORK_IN_PROGRESS/ep2_outline_proposal.md` — a DRAFT PROPOSAL beat map for EP.2, explicitly labeled as NOT a script and NOT canon, with TASK-0005 (the actual script) remaining gated on DEC-0008 + Owner word-approval exactly as before. Contents:

- **13 beats**, cold-open ("72 hours, one bag") through the midnight sky-tear/banner cliffhanger ("Are you still there?"), each citing its grounding source (`CONTINUITY_LEDGER.md`, `Master_Project_Bible.md`'s locked Ch.2 beats, `story_bible.md`'s drafting log + Keepsakes list, `manuscript/chapters/01_the_ninth_world.md`'s existing Ha-eun scene text, `ep1_v3_script.md`'s own EP2 PREVIEW note, `readers/episode1_part2.html`'s endcard tease). Two beats (Si-woo dream callback, night-watch bridge) are explicitly flagged "(PROPOSAL — connective only)" since no independent source states they occur — offered as low-risk pacing bridges only, not asserted as canon.
- **Known continuity anchors section**, covering exactly the five anchors the work order named: Day −3/countdown acceleration, Ha-eun's debut, the midnight-speaking banner, the end-of-Ch.2 sky-crack, and the no-wound-reset rule.
- **Adaptation notes**: a proposed Part 1/Part 2 strip split (Beats 1–8 / Beats 9–13), explicitly framed as a pacing suggestion for ③ Visual to accept or reject at storyboard time, not an instruction — no ③-lane file (`Art_Direction.md` or any other) was opened or modified.
- **Three Owner decision blocks, all QUEUED, none decided:**
  - **Q-02** — Han's 9.0 keepsake choice. Options recorded with one-line implications each: Si-woo's practice score (centers the Han–Si-woo bond, slight Ch.3 foreshadow risk); festival token (centers the world itself, lower specificity); "other" (unscoped, would need a new item introduced first). Left explicitly UNDECIDED.
  - **Q-04** — Ha-eun romance default OFF. Noted as an honored constraint (Beat 3 written with zero romantic framing); no change requested, not treated as a new question.
  - **Q-14** — key-visual poster timing. Noted as an open Owner question this outline does not answer, flagged only because EP.2 prep being underway may make it a timelier moment to revisit.
- No new OPEN_QUESTIONS.md entry was added. Q-01 (Im Dan-bi's Ch.3 first-death candidacy) is referenced only as a constraint the outline's Beat 4 deliberately avoids foreclosing — not resolved, not given a new number.
- The sealed twist bank (`twist_bank_PRIVATE.md`, Q-12) is not referenced, reconstructed, named, or hinted at anywhere in the outline.

---

## What the ⑤ gate should check

1. **QA-04 fix precision** — confirm the corrected row and synthesis finding #2 in `ep1_adaptation_variance.md` now accurately state: script P40 contains "For the well" as text; readers (`episode1_part2.html`) do not; the practical published-EP.1 conclusion is unchanged. Confirm no other row/finding/section in the file was altered (a byte-diff against the CYCLE-0001 ② version, excluding the two corrected spots and the new bottom revision note, should show zero other changes).
2. **Outline grounding** — spot-check that every one of the outline's 13 beats either cites a real source correctly or is honestly flagged "(PROPOSAL — connective only)." Recommend checking Beats 3 (Ha-eun debut), 8–10 (keepsake funeral/hairpin/9.0 choice), and 13 (midnight tear/banner) first, since those are the most load-bearing.
3. **UNDECIDED discipline** — confirm Q-02 is presented as options only, with no lean or recommendation smuggled in; confirm Q-04 is correctly treated as an honored constraint rather than a new question; confirm Q-14 is noted, not answered. Confirm Q-01 is referenced only as a non-foreclosure constraint.
4. **Sealed-twist compliance** — confirm no sentence in either deliverable references, names, reconstructs, or hints at `twist_bank_PRIVATE.md`'s contents.
5. **Lane compliance** — confirm the commit touches exactly: `manuscript/manhwa/ep1_adaptation_variance.md`, `studio/06_Operations/WORK_IN_PROGRESS/ep2_outline_proposal.md`, `studio/06_Operations/STUDIO_STATUS.md`, `studio/06_Operations/CHANGELOG.md`, `studio/06_Operations/TASK_QUEUE.md` (Status cells of TASK-0008/TASK-0017 only), and this handoff file — nothing else. No chapter, `story_bible.md`, `Master_Project_Bible.md`, the EP.1 script, any reader, or any ③/④/⑤ file should appear in the diff.
6. **Commit hygiene** — prefix `[②-LORE]`, one commit, descriptive message covering both deliverables.

---

## Open questions (unchanged status, just cross-referenced here)

- **Q-02** (Han's 9.0 keepsake choice) — UNDECIDED; options now recorded in `ep2_outline_proposal.md` §4 for the Owner's eventual pick.
- **Q-04** (Ha-eun romance default OFF) — unchanged; honored, not altered.
- **Q-14** (key-visual poster timing) — unchanged; noted as newly-relevant, not answered.
- **Q-01** (Im Dan-bi's Ch.3 first-death candidacy) — unchanged; referenced only as a non-foreclosure constraint on Beat 4.
- **Q-12** (sealed twist bank custody) — unchanged; not touched, not referenced.

No new open question was added this turn.

---

## Timebox note

Both deliverables were completed in full within this turn — nothing is PARTIAL. The corrective edit was genuinely surgical (two spots plus one revision-note line); the outline proposal is complete at 13 beats with all three required Owner decision blocks queued.

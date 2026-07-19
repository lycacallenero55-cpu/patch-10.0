# QA Review — CYCLE-0001 Cycle Audit
- **Date:** 2026-07-19 · **Author:** ⑤ Quality Assurance · **Task ID:** TASK-0016
- **Scope:** all four CYCLE-0001 commits (① `d5c66125`, ② `31b3272c`, ③ `5284fdd1`, ④ `6753353c`) for lane compliance and commit hygiene; the cycle's new records (`story_bible_tagging_proposal.md`, `ep1_adaptation_variance.md`, `Kit_Specs_DRAFT.md`, `Trailer_v2_KF_Production_Plan.md`, `CANON_REGISTRY.md`, `INDEX.md`, `PROMPT_LIBRARY.md`, `ARCHIVE/README.md`, `TEMPLATES/*`) for accuracy and doc quality; CM-01 and SW-01 adjudication evidence; a continuity spot-audit against `STUDIO_RULES.md` §5 and `CONTINUITY_LEDGER.md`. QA authority is to report and recommend — this review makes no semantic edit to any canon, spec, or record file owned by another department, and adjudicates disputed interpretations only as evidence-weighing recommendations, never as rulings (Handbook §8.5 "Authority").

> **Note on severity scale:** the dispatching work order specifies S1 (blocks production/corrupts truth) / S2 (causes errors) / S3 (cosmetic/process) for this review. The Handbook §8.5/§21 template and `QA_REVIEW_TEMPLATE.md` instead define S0–S4 (CRITICAL/BLOCKER/MAJOR/MINOR/POLISH). This is itself a minor doc-quality drift between the work order and the template it's meant to use (see QA-11). Findings below use the work order's S1–S3 scale as instructed, with an S0/S4-equivalent noted in brackets where the Handbook scale would classify a finding differently, so nothing is lost in translation.

---

## (a) Lane-compliance audit

Verified via `github__get_commit` file-change lists against Amendment 1 §A1.2's write-lane ownership map.

### Commit ① `d5c66125b1e6977b75c6dc64a78ad03c557adf88` — `[①-EP]`
**Files changed:** `README.md` · `studio/00_OPERATING_HANDBOOK.md` · `studio/06_Operations/CHANGELOG.md` · `studio/06_Operations/DECISION_LOG.md` · `studio/06_Operations/HANDOFFS/CYCLE-0001-EP.md` · `studio/06_Operations/STUDIO_STATUS.md` · `studio/06_Operations/TASK_QUEUE.md`.
**Lane check:** ①'s lane = root `README.md` · `studio/00_STUDIO_RULES.md` · `studio/00_OPERATING_HANDBOOK.md` · `studio/06_Operations/` (except ⑤'s four files). Every changed file falls inside this lane; none of ⑤'s reserved files (`REVIEWS/`, `CONTINUITY_LEDGER.md`, `VALIDATION_PROFILE.md`, `INCIDENTS.md`) were touched.
**Verdict: COMPLIANT.**
**Commit hygiene:** prefix `[①-EP]` present; message is descriptive and lists the four substantive actions (Amendment 1, DEC-0012, task activation, status sync). Good.

### Commit ② `31b3272c37e5e5565f06ca41139e4bf34021092a` — `[②-LORE]`
**Files changed:** `manuscript/manhwa/ep1_adaptation_variance.md` · `studio/06_Operations/CHANGELOG.md` · `studio/06_Operations/HANDOFFS/CYCLE-0001-LORE.md` · `studio/06_Operations/STUDIO_STATUS.md` · `studio/06_Operations/TASK_QUEUE.md` · `studio/06_Operations/WORK_IN_PROGRESS/story_bible_tagging_proposal.md`.
**Lane check:** ②'s lane = `manuscript/` (`bible/`, `chapters/`, `manhwa/`). `ep1_adaptation_variance.md` is inside `manuscript/manhwa/` — compliant. The remaining five files are all within the Amendment 1 shared carve-out (`TASK_QUEUE.md`, `WORK_IN_PROGRESS/`, `HANDOFFS/` own-turn note, `STUDIO_STATUS.md` + `CHANGELOG.md` turn mechanics) available to any department during its own turn.
**Verdict: COMPLIANT.** No canon file (`story_bible.md`, `00_prologue.md`, `01_the_ninth_world.md`, `ep1_v3_script.md`, `Master_Project_Bible.md`) appears in the changed-file list — confirms ②'s own claim that these were read-only this turn.
**Commit hygiene:** prefix `[②-LORE]` present; message accurately summarizes both deliverables and explicitly states the byte-for-byte-unchanged canon files by name. Good — this is the strongest commit message of the four for verifiability (it names exactly what was NOT touched).

### Commit ③ `5284fdd1e58982da9168c76b50134e4878c7d7f2` — `[③-VISUAL]`
**Files changed:** `studio/02_Art/Kit_Specs_DRAFT.md` · `studio/04_Storyboards/Trailer_v2_KF_Production_Plan.md` · `studio/06_Operations/CHANGELOG.md` · `studio/06_Operations/HANDOFFS/CYCLE-0001-VISUAL.md` · `studio/06_Operations/STUDIO_STATUS.md` · `studio/06_Operations/TASK_QUEUE.md`.
**Lane check:** ③'s lane = `studio/02_Art/` · `studio/03_Assets/` · `studio/04_Storyboards/` · `studio/05_Production/` · `readers/`. Both new files fall inside `02_Art/` and `04_Storyboards/` respectively — compliant. Remaining files are the same shared turn-mechanics carve-out as above.
**Verdict: COMPLIANT.** No existing `02_Art/`, `03_Assets/`, or `readers/` file was modified — `Character_Bible.md`, `Asset_Registry.md`, `Environment_Bible.md`, `Effects_Bible.md`, and both reader HTML files are untouched, confirming ③'s own "spec-draft phase only" claim.
**Commit hygiene:** prefix `[③-VISUAL]` present; message is long but precise — explicitly states the reason no generation happened (I-0001 + per-item approval law, both cited) and names the CM-01 flag. Good.

### Commit ④ `6753353cb2d62a7f55b72d359cd16da53d79ff93` — `[④-REPO]`
**Files changed:** `studio/06_Operations/CHANGELOG.md` · `studio/06_Operations/HANDOFFS/CYCLE-0001-REPO.md` · `studio/06_Operations/STUDIO_STATUS.md` · `studio/06_Operations/TASK_QUEUE.md` · `studio/07_Repository/ARCHIVE/README.md` · `studio/07_Repository/CANON_REGISTRY.md` · `studio/07_Repository/INDEX.md` · `studio/07_Repository/PROMPT_LIBRARY.md` · `studio/07_Repository/TEMPLATES/DECISION_ENTRY_TEMPLATE.md` · `studio/07_Repository/TEMPLATES/QA_REVIEW_TEMPLATE.md` · `studio/07_Repository/TEMPLATES/TURN_HANDOFF_TEMPLATE.md` · `studio/07_Repository/TEMPLATES/WORK_ORDER_TEMPLATE.md`.
**Lane check:** ④'s lane = `studio/07_Repository/` (`CANON_REGISTRY.md`, `INDEX.md`, `TEMPLATES/`, `PROMPT_LIBRARY.md`, `ARCHIVE/`), plus meaning-safe mechanical fixes anywhere. All eight new files sit exactly inside `studio/07_Repository/**` — compliant. Remaining four are the shared turn-mechanics carve-out.
**Verdict: COMPLIANT.** No canon or spec content was authored outside the named lane; ④'s own charter's "meaning-safe mechanical fixes anywhere" allowance was correctly NOT exercised this turn (confirmed zero changes to any file outside `07_Repository/**` and the four turn-mechanics files) — ④'s handoff explicitly disclosed the mechanical-fix candidates it chose to log rather than act on, which is the correct discipline for a records-only turn.
**Commit hygiene:** prefix `[④-REPO]` present; message is the most detailed of the four, itemizing every new file's contents and naming both CM-01 and SW-01 explicitly with rationale. Good — this is a model example for future work-order commit-message expectations.

**Lane-compliance summary: all four commits COMPLIANT, no violations found.** All four commit messages carry the correct department prefix and a message specific enough to reconstruct scope without opening the diff. No cross-lane edits, no silent canon touches, no undisclosed scope reduction detected in any of the four turns.

---

## (b) TASK-0008 verification (`manuscript/manhwa/ep1_adaptation_variance.md`)

Spot-checked against `manuscript/chapters/00_prologue.md`, `manuscript/chapters/01_the_ninth_world.md`, `manuscript/manhwa/ep1_v3_script.md`, `readers/episode1_part1.html`, `readers/episode1_part2.html` — full text of all five sources read and cross-referenced line-by-line for every row below.

### QA-01 — Ha-eun Ch.1 omission claim: VERIFIED
The record's claim that Ha-eun's entire prose Ch.1 library scene (bell towers, tuning fork, the four-note melody, "Haven't we met, senior? ... No. You don't.") is absent from both the script and both readers is confirmed exactly. `01_the_ninth_world.md` contains the full ~900-word scene verbatim. `ep1_v3_script.md` jumps directly from P55 (Han's private realization about the leaked dream) to P56 (rooftop moon-check) with zero Ha-eun content anywhere in its 58 panels. `readers/episode1_part2.html` likewise jumps from the black "THE REALIZATION" section straight to the rooftop/moon-skip/endcard with no Ha-eun scene. The variance record's characterization of this as "the single largest omission" and its cross-reference to `CONTINUITY_LEDGER.md`'s pre-existing note ("Yoo Ha-eun: introduced in prose Ch.1 only… manhwa debut = EP.2") are both accurate.
- **Confidence:** HIGH.

### QA-02 — DIALOGUE_REWORDED example verbatim check ("Proctor's fail call"): VERIFIED
Record claims: prose = `"Point and match," said the proctor... "Seo Han. Practical: fail. Attendance: perfect."`; script P48 = `"Point. Seo Han — fail."`; readers = `"POINT. SEO HAN — FAIL. AGAIN."` All three quotes check out exactly against source. Script drops "match" and "Attendance: perfect" as the record claims; readers add "AGAIN," which the record correctly notes is present in neither prose nor script.
- **Confidence:** HIGH.

### QA-03 — "11:58 → Midnight" claim: VERIFIED
Prose (`01_the_ninth_world.md`): `"On the roof of the old hall, at 11:58, he checked the moon."` Script P56: `📦 "Midnight. The old dorm roof. I check the moon every night."` Reader Part 2: `<div class="tho">EVERY NIGHT, I CHECK THE MOON.</div>` — no time given at all. This is an exact three-way match to the record's claim: prose's precise 11:58 → script's vaguer "Midnight" → readers drop the time entirely. The record's observation that this quietly erodes a deliberate cross-chapter numeric rhyme (the prologue's own 11:58 wind-stop) is well-supported and correctly flagged as texture drift, not a contradiction.
- **Confidence:** HIGH.

### QA-04 — 'well' setup/payoff asymmetry claim: VERIFIED-WITH-CORRECTION
This is the one substantive error found in TASK-0008. The record's row and its Top-Findings synthesis (#2) both state: *"the explicit unspoken 'For the well' callback... is NOT rendered as text in either the script or the readers (both use a more generic 'leave them where she'll only find them later' gloss)."*
This is **incorrect for the script**. `ep1_v3_script.md` P40 reads: `💭 "She refuses tips. So I hide them. For the well."` — the script explicitly contains "For the well" as text, and the record's own Notes column cites "Script P40" as its source for this very row, meaning the error is a misreading of a source it correctly identified, not a missing citation. The claim IS correct for the readers: `episode1_part2.html`'s wording is `"SHE ALWAYS REFUSES TIPS. SO I LEAVE THEM WHERE SHE'LL ONLY FIND THEM LATER."` — no "for the well" anywhere.
**Correction:** the payoff callback ("For the well") is present in the ADAPTATION_CANON script layer but dropped specifically at the DERIVATIVE-OUTPUT (readers) layer — i.e., the asymmetry the record flags is real, but it happens one layer later in the precedence chain than stated, and per `SOURCE_OF_TRUTH.md`'s own precedence rule (readers supersede script wording), the *currently published* version of EP.1 genuinely does drop the payoff line, so the record's practical conclusion (readers-as-published lack the "for the well" echo) still stands. Only the "in either the script or the readers" phrasing is wrong; the record should read "dropped between the script and the readers" or simply "absent from the currently published readers text (though present in the superseded script draft)."
- **Confidence:** HIGH. **Severity of the correction: S3** (localized wording-precision issue; does not change the practical continuity conclusion or any load-bearing fact, since the readers — the higher-precedence source — do lack the line either way).

### QA-05 — Remaining spot-checks (supporting rows, sampled beyond the four required)
- **"First bowl's on the house" tic-line drift** (prose "on the house" → script "free" → readers "on me"): verified exactly as quoted across all three sources.
- **"Attendance: perfect" omission**: verified — the phrase appears in prose only (`01_the_ninth_world.md`), absent from script P48 and both readers. Confirmed as a clean OMITTED_FROM_ADAPTATION case, correctly distinguished from the compressed-but-present "Point/fail" fragment (QA-02).
- **9 days → 3 days countdown**: verified consistent across prose, script P57-58, and reader Part 2's "MY COUNT SAID NINE DAYS LEFT" / "THE WORLD JUST ANSWERED: THREE" — matches `CONTINUITY_LEDGER.md` baseline exactly, as the record claims.
- **Callus-hand text-only caveat**: the record correctly notes that neither the script nor the readers repeat the word "left" for Cha's callus (prose alone says "her left hand"); the record correctly scopes this as a text-only finding and defers the art-side check to ③/⑤ — this review's continuity spot-audit (section (d) below) covers that follow-up.

### TASK-0008 Verdict: **VERIFIED-WITH-CORRECTIONS**
Six required rows checked plus five supporting rows; five of six required claims are exact and well-evidenced; one (QA-04, the well-callback asymmetry) contains a source-misreading that should be corrected in the record's wording before it is cited elsewhere, though the underlying continuity observation survives the correction. No load-bearing plot fact was found contradicted by this record anywhere it was checked — the record's own "no load-bearing plot fact was found to be contradicted" synthesis claim (finding #6) held up under this independent spot-check. Recommend ② amend QA-04's row and synthesis-finding #2 to read "absent from the currently published readers (present in the now-superseded script draft)" rather than "absent from either." This is a wording-precision fix to a record, not a canon edit, and is within ②'s own lane to correct on its next turn.

---

## (c) CONFLICT adjudication evidence

### CM-01 — Cha Mi-ran v2-era kit-sheet reuse vs. Asset_Registry deprecation

**Source quote 1** — `studio/02_Art/Character_Bible.md` CHAR-004:
> "Dual master `2ec02dec…` · kit sheet exists (v2 era `f8b56b3a…` — usable for expression reference)."

**Source quote 2** — `studio/03_Assets/Asset_Registry.md` DEPRECATED section:
> "All v1 painterly-era and v2 SL-flat-era assets (old covers, old casting sheets `c10f…`/`1a75…`, composed-page tests `4d147beb…`/`5ac71fe7…`, horizontal-seam tears `55d895e7…`/`1f5e0a4e…`). Historical record only."

**Source quote 3** — `Asset_Registry.md` APPENDIX, DEPRECATED-ERA TITLES:
> "v2 SL-era — 'Seo Han — SL-style take 1/2/3', 'Si-woo / Ha-eun — master (locked style)', '… angles & expressions', **'Cha Mi-ran — dual master (locked style)'**."

**Cross-check** — `manuscript/bible/story_bible.md`, section "SUPPORTING CAST REFERENCE SET v2 (locked style — pending user approval)":
> "CHA dual master: `22f7ac35…` · sheet (both eras): **`f8b56b3a-8e6e-496f-9927-103b508ed23d.png`** · accents: rust dust (8.0) / lantern amber (9.0)"

**Analysis:** the exact asset ID Character_Bible calls "usable for expression reference" (`f8b56b3a…`) is independently confirmed, via `story_bible.md`'s own section header, to belong to the "SUPPORTING CAST REFERENCE SET **v2**" — i.e., Character_Bible's own citation self-identifies the asset as v2-era. Asset_Registry's DEPRECATED section blanket-deprecates "all v2 SL-flat-era assets," and its Appendix's deprecated-title blacklist includes a title reading "Cha Mi-ran — dual master (locked style)" under its explicit "v2 SL-era" heading — closely matching (though not with an exact verbatim string match to) "Cha Mi-ran — dual-era design / proportion fix," the alternate phrasing ④'s handoff and Kit_Specs_DRAFT.md both use when describing this same blacklist entry. Both of ④'s and ③'s handoffs independently arrived at the same reading of this conflict, and this review's own direct source read reaches the same conclusion by a third path (the story_bible.md cross-check), which increases confidence that this is not merely a case of departments repeating each other's assumption.

There is a small residual ambiguity worth naming honestly: the Appendix's blacklist title string is not a byte-for-byte match to the ID `f8b56b3a…`'s own generation title in the platform Library (this review has no tool access to the platform Library UI to confirm the exact display title independently) — the identification rests on (1) the ID matching exactly between Character_Bible and story_bible.md's "v2" section, and (2) the blacklist's "v2 SL-era" category heading applying to "ALL" such assets per Asset_Registry's own DEPRECATED section wording, which is unambiguous even without the exact title string matching perfectly.

**Recommendation:** the "generate fresh in v3" reading is better supported. Character_Bible.md's claim is the weaker of the two positions — it cites a single asset as an exception to a blanket rule stated by a different LOCKED-lane file (Asset_Registry.md), without itself stating why this asset should be exempt from the "ALL v2 SL-flat-era assets" deprecation. Asset_Registry.md's rule is categorical, unconditional, and is the file `SOURCE_OF_TRUTH.md` and `00_STUDIO_RULES.md` §2 both designate as *the* single source of truth for LOCKED asset status — Character_Bible.md is `VISUAL_SPEC` (design facts), not the asset-status authority. Recommend ③ Visual Production (on its next turn) either (a) update Character_Bible.md CHAR-004's parenthetical to remove "usable for expression reference" and instead note the sheet as historical/non-referenceable, or (b) if the creator wants to preserve the v2 sheet as a deliberate documented exception, add that exception explicitly to Asset_Registry.md's DEPRECATED section with a stated reason, rather than leaving two LOCKED-lane files in silent disagreement. `Kit_Specs_DRAFT.md`'s own KIT-CHAR-004 spec already assumes the safer "generate fresh in v3" path, so no downstream production work is blocked by leaving this un-adjudicated a while longer — the fix is a small in-file correction whenever ③ next touches Character_Bible.md, gated on Creator awareness (not necessarily a full DEC-ID ruling, since it's an asset-usability question already anticipated to resolve to "generate fresh" either way) — ⑤ makes this recommendation but performs no edit to either file.

### SW-01 — Si-woo year-label mismatch

**Source quote 1** — `studio/01_Lore/Master_Project_Bible.md` §7:
> "**YOON SI-WOO** — 16, earnest sword-Etude junior; 'telegraphs kindness the way others telegraph attacks'..."

**Source quote 2** — `manuscript/bible/story_bible.md`, "Cast (living, 9.0)":
> "**Yoon Si-woo** — 2nd-year, earnest sword-Etude student; keeps trying to 'fix' senior Han's swordwork..."

**Analysis:** both sources agree on every substantive fact about Si-woo (age 16, sword-Etude discipline, "telegraphs kindness" characterization, fixation on fixing Han's elbow, PATCH-SCARRED status). Only the year-label word differs: "junior" (Master_Project_Bible) vs. "2nd-year" (story_bible.md). "Junior" is genuinely ambiguous in English academic usage — it can mean a specific class-year (US high-school convention: 3rd of 4 years) or can be used loosely as a synonym for "younger/lower-ranked student" without a precise year attached. "2nd-year" is unambiguous but does not by itself establish how many years the academy program runs, so there is no independent arithmetic check available in the current canon to resolve which is the typo and which is intended (unlike, say, checking against a stated total-years figure for Soryeong Academy, which does not exist in any file read this cycle).

**Recommendation:** this is non-load-bearing and low-risk exactly as ④'s handoff characterizes it — no scene, dialogue, or visual depends on the specific word. Recommend ② Lore (content owner for both files, since Master_Project_Bible content authority and story_bible.md are both ② domains) pick one term and apply it in both places on its next lore-touching turn, with a light preference for "2nd-year" since it is unambiguous where "junior" is not — but this is a stylistic pick, not something requiring escalation to the Creator as a DEC-ID ruling, since neither reading changes any established fact (age, characterization, or plot role are identical either way). ⑤ recommends only; no edit made to either file by this review.

---

## (d) Continuity spot-audit

Checked the cycle's four new content-bearing files (`Kit_Specs_DRAFT.md`, `Trailer_v2_KF_Production_Plan.md`, `ep1_adaptation_variance.md`, `CANON_REGISTRY.md`) against `studio/00_STUDIO_RULES.md` §5 (LOCKED micro-rules) and `studio/06_Operations/CONTINUITY_LEDGER.md` baseline.

| Micro-rule (§5) | Checked against | Result |
|---|---|---|
| Ha-eun: NO hairpin ever; tuning fork in RIGHT hand | `Kit_Specs_DRAFT.md` KIT-CHAR-003: "**NEVER draw a hairpin on her.**... silver tuning fork in RIGHT hand"; repeated again in its "Continuity micro-rules binding this kit" subsection ("NO hairpin ever. This is the single hardest constraint on this kit..."; "Tuning fork in RIGHT hand (never left)") | **CORRECT and reinforced twice** in the same document — no drift. |
| Si-woo: bandage plaster on LEFT cheek | `Kit_Specs_DRAFT.md` KIT-CHAR-002: "bandage on **LEFT cheek**" (cited from Character_Bible, restated again in its own micro-rules subsection: "Bandage plaster on **LEFT cheek** (never right, never absent...)") | **CORRECT**, matches `CONTINUITY_LEDGER.md`'s "bandage LEFT cheek (minor training scuff — cosmetic constant)" exactly. |
| Cha: wrench callus on LEFT hand | `Kit_Specs_DRAFT.md` KIT-CHAR-004: "wrench callus **LEFT hand**" (cited twice: main description and its own micro-rules subsection, "Wrench callus on **LEFT hand** (not right) — in both eras") | **CORRECT**, matches `CONTINUITY_LEDGER.md`'s "callus LEFT hand" and prose's explicit "her left hand" exactly. |
| Han: scar LEFT eyebrow / sword RIGHT hand / watch LEFT coat pocket | `CANON_REGISTRY.md` §1 Seo Han: "scar through **LEFT eyebrow**... bag strap over RIGHT shoulder..."; separate Key Objects row: "Pocket watch... carried in Han's **LEFT coat pocket**" | **CORRECT** on all three, matches STUDIO_RULES §5 verbatim. |
| Proctor Im Dan-bi: BLACK hair greying, never blonde | `CANON_REGISTRY.md` §1 and `story_bible.md`'s "PART 2 CONSISTENCY ANCHORS" note ("BLACK greying hair, glasses — never blonde") | **CORRECT**, consistently stated everywhere checked. |
| Sky-crack: diagonal, branching, progresses, never identical twice | `Trailer_v2_KF_Production_Plan.md` KF-01/KF-02 rows: explicitly requires KF-02 to be "visibly grown" and "not be a recolor" relative to KF-01, correctly invoking "Art_Direction's progression law" | **CORRECT** — the plan actively defends this rule rather than merely restating it, a good practice. |

**Does `CANON_REGISTRY.md` contradict `CONTINUITY_LEDGER.md` anywhere?** No contradiction found. Every fact cross-checked between the two (Han's baseline knowledge state, Si-woo's dream status, Ha-eun's manhwa-debut deferral, Cha's callus/memory state) matches exactly, and `CANON_REGISTRY.md` §5 (Timeline Anchors) explicitly defers to `CONTINUITY_LEDGER.md` as "the authoritative state ledger" rather than duplicating it — the correct custodial relationship per Amendment 1 (④ manages the registry that points to ⑤'s ledger, not the other way around).

**One near-miss worth flagging (not a violation):** `Kit_Specs_DRAFT.md`'s KIT-CHAR-004 section states Cha's height as "~172cm commanding" (matching STUDIO_RULES §5's "~172cm" exactly) but its "Required views/poses" subsection later says the height "should read as 'commanding' relative to other characters in any multi-character plate" without restating the numeric figure at that second mention — this is not an error (the number is stated correctly once, earlier in the same document), but it is exactly the kind of single-citation pattern that risks drifting to an unstated approximation ("tall," "imposing") in a future turn that only skims the later subsection. No fix needed now; flagged for awareness only.

**Continuity spot-audit verdict:** No violations found in any of the six checked micro-rules across the four audited files. The cycle's new documents show consistently correct, often doubly-reinforced citation of the locked micro-rules — this is a genuinely clean result, not merely an absence of evidence (all six rules were positively checked and matched, not just "not found to conflict").

---

## (e) Doc-quality findings

### QA-06 — `README.md` line for `07_Repository/` matches actual deliverables
Verified: README.md's tree lists `07_Repository/ ← canon registry, repo index, templates, prompt library, archive (④)`, which accurately names all five ④ deliverables and the correct owning symbol. No fix needed — ④'s own handoff already confirmed this and this review independently re-verifies it. **Severity:** N/A (confirmation, not a finding).

### QA-07 — INDEX.md's REVIEWS/ description is accurate
`INDEX.md` states `studio/06_Operations/REVIEWS/` "contains only `.gitkeep`" as of HEAD — verified via direct directory listing: the only file present is `.gitkeep`. Accurate at time of writing (this review is what changes that). No fix needed.

### QA-08 — PROMPT_LIBRARY.md anchor pointers resolve to real headings
Spot-checked two of the four appendix anchors PROMPT_LIBRARY.md cites: `studio/03_Assets/Asset_Registry.md`'s `## APPENDIX — Library lookup table (archived 2026-07-19)` — confirmed this exact heading exists verbatim in the live file. The other three anchors (`Art_Direction.md` Appendix A, `Image_Workflow_QA.md` appendix, `Video_Workflow.md` appendix) were not opened this cycle (outside this order's required-reading list) and are marked **UNVERIFIED** — not confirmed broken, simply not checked. Recommend a future ④ or ⑤ turn close this gap explicitly rather than assume it from the one confirmed anchor.
- **Severity:** S3. **Confidence:** the one checked anchor is HIGH; the other three are UNVERIFIED, not LOW-confidence-negative.

### QA-09 — CM-01/SW-01 not yet logged in OPEN_QUESTIONS.md
`CANON_REGISTRY.md` and both ③/④ handoffs treat CM-01 and SW-01 as tracked "CONFLICT-FOR-QA" items, but neither appears as a row in `studio/06_Operations/OPEN_QUESTIONS.md` (Q-01 through Q-14, read in full this cycle — no CM/SW-prefixed or equivalent entry exists). Similarly, the two effects-grammar extension questions `Trailer_v2_KF_Production_Plan.md` explicitly recommends logging ("Recommended new TASK_QUEUE / OPEN_QUESTIONS items... not created by this plan") have not been added anywhere by any of the four cycle turns — correctly so, since each turn's own constraints scoped writes to specific named cells and none authorized new OPEN_QUESTIONS rows. This is a **process gap, not a data-loss risk** — both conflicts are fully evidenced with source pointers in `CANON_REGISTRY.md` and this review, so nothing is at risk of being forgotten, but the studio's two parallel "unresolved item" ledgers (`OPEN_QUESTIONS.md` for story/world questions, `CANON_REGISTRY.md`'s CONFLICT-FOR-QA tag for canon-record disagreements) are not currently cross-linked, which could cause a future reader checking only `OPEN_QUESTIONS.md` to miss these two items entirely.
- **Severity:** S3 (process/discoverability gap; no fact is at risk, only findability). **Confidence:** HIGH. **Recommended action:** ① (or whichever department next has an authorized `OPEN_QUESTIONS.md` write) add four short pointer rows (CM-01, SW-01, and the two FX-grammar-extension questions) that simply cross-reference `CANON_REGISTRY.md`/`Trailer_v2_KF_Production_Plan.md` rather than duplicating their content — consistent with the repo's existing pointer-not-copy convention (`PROMPT_LIBRARY.md`'s own stated design principle).

### QA-10 — Label discipline: consistently present and correct
Every new file this cycle carries an explicit status header at or near its top: `story_bible_tagging_proposal.md` = "DRAFT PROPOSAL"; `ep1_adaptation_variance.md` = "RECORD — IN REVIEW"; `Kit_Specs_DRAFT.md` = "DRAFT — NOT LOCKED"; `Trailer_v2_KF_Production_Plan.md` = "PLAN — IN REVIEW"; `CANON_REGISTRY.md` = "RECORD — DRAFT, recommend-only"; `INDEX.md`/`PROMPT_LIBRARY.md`/`ARCHIVE/README.md` = "RECORD"/"POINTER INDEX"/policy-record framing respectively; all four `TEMPLATES/*` files carry a "Delete this notice line when instantiating a real [item]" placeholder-marker convention. No file was found presenting DRAFT-status content as if it were RECORD/LOCKED. **No violations found.**
- **Severity:** N/A (positive finding).

### QA-11 — Work-order severity scale drifted from the Handbook/template it's meant to align with
Noted at the top of this review: the Amendment-1-era work-order convention used to dispatch this very cycle's ⑤ turn specifies a 3-tier S1–S3 severity scale, while `studio/00_OPERATING_HANDBOOK.md` §8.5/§21 and the ④-built `QA_REVIEW_TEMPLATE.md` (both read this cycle) specify a 5-tier S0–S4 scale. This is not a contradiction inside any single file — each file is internally consistent — but it is a cross-document drift between the *dispatching convention* and the *template/handbook it's supposed to align with*, of exactly the kind Handbook §21's "Current known audit traps" section warns to check for rather than assume settled.
- **Severity:** S3. **Confidence:** HIGH. **Recommended action:** ① (owner of the work-order convention and of the Handbook) reconcile the two scales next time either is touched — either fold the work order's 3-tier scale into the Handbook's 5-tier one (recommended, since S0/S4 cover real cases — secret exposure and cosmetic polish — that S1/S3 alone would have to awkwardly absorb), or formally amend the Handbook to the simpler 3-tier scale and update `QA_REVIEW_TEMPLATE.md` to match. Not performed by this review since neither the Handbook nor the template is in ⑤'s write lane.

### Duplication risk check
`PROMPT_LIBRARY.md` explicitly states it duplicates no prompt text (verified: reading its full body confirms no verbatim prompt strings appear, only pointers, contents-summaries, and usage rules in prose). `CANON_REGISTRY.md` similarly quotes/close-paraphrases rather than duplicating full passages, and explicitly defers to `CONTINUITY_LEDGER.md` rather than re-deriving it. No duplication risk found in any of the cycle's new files.

---

## (f) Process findings

### QA-12 — STATUS commit-pointer drift (flagged by ④, independently confirmed)

**Evidence, re-verified independently this turn:**
- ③'s commit (`5284fdd1…`) sets `STUDIO_STATUS.md`'s `base_remote_commit`/`last_verified_commit` to `31b3272c37e5e5565f06ca41139e4bf34021092a` — but `31b3272c…` is ②'s own resulting SHA (the commit ③ started *from*), not the SHA ③'s own turn produced. Confirmed via `github__get_commit` on `5284fdd1…`: the actual commit that resulted from ③'s turn has SHA `5284fdd1e58982da9168c76b50134e4878c7d7f2`, which is what the STATUS *should* have recorded but does not.
- The same pattern recurs at every observed handoff this cycle: ②'s STATUS update (inside commit `31b3272c`) records `base_remote_commit: d5c66125…` — again, ①'s resulting SHA (the base ② started from), not ②'s own resulting SHA (`31b3272c…` itself).
- ④'s commit (`6753353c…`) is the sole exception: its `STUDIO_STATUS.md` update (read directly from the live file at HEAD) correctly records `base_remote_commit: 5284fdd1e58982da9168c76b50134e4878c7d7f2` and `last_verified_commit: 5284fdd1e58982da9168c76b50134e4878c7d7f2` — but this is ③'s resulting SHA (correct as ④'s *base*, since ④ built on top of it), not ④'s own resulting SHA `6753353c…`. So even the "fixed" case is actually just the drift pattern's SAME one-commit-behind convention applied consistently — every department's STATUS update states the commit it started FROM, never the commit its own turn produces (which cannot be known until after the commit exists, an inherent chicken-and-egg problem for any single-commit turn that bundles the STATUS update into the same push as its content).

**Assessment:** this is a real, confirmed, cycle-wide convention gap — every one of the four cycle turns exhibits it, meaning it is not a one-off mistake by a single department but a structural gap in the turn-mechanics instruction itself (Amendment 1 §A1.4 step 4 says "update STUDIO_STATUS.md" but does not specify HOW a turn should record a commit SHA that does not exist yet at write time). Its actual damage this cycle was zero: every department in this cycle read live files rather than trusting the stale STATUS pointer (confirmed by this review's own read-first pass, which likewise ignored the stale pointer and fetched every file fresh), so no wrong decision resulted. But the risk compounds the more cycles run without a fix — a future, less careful turn (or a differently-instructed subagent) that DOES trust `base_remote_commit` at face value would silently work from a commit one turn stale, potentially missing the most recent turn's changes entirely.

**Severity: S2** (this is a "will cause errors if unaddressed" case per the work order's definition — it has not yet caused an error, but the mechanism for one is now confirmed present in 100% of sampled turns, and the failure mode it invites — trusting a stale pointer — is exactly the anti-pattern Handbook §3.1 "Repository law" warns against: "do not claim a change is shared until the remote commit is verified"). Not S1, because no downstream turn this cycle actually was misled by it (every turn independently re-verified via live reads); not S3, because the risk is not merely cosmetic — a future turn trusting the pointer would work from wrong state.
**Confidence:** HIGH (directly confirmed via `github__get_commit` cross-checks on all four commits, not inferred).

**Recommended convention going forward:** the cleanest fix does not require guessing a not-yet-existent SHA. Recommend Amendment 1 §A1.4 be amended (① owns the Handbook) to specify: *"A turn's STUDIO_STATUS.md update sets `base_remote_commit` to the commit this turn started from (this is always knowable at write time and answers 'what did I build on') and leaves `last_verified_commit` either equal to `base_remote_commit` (if no other commit was independently verified this turn) or updated by the NEXT turn's read-first pass, which — per §A1.4 step 1's own 'trust commits, never memory' rule — already re-verifies the actual HEAD via `github__list_commits`/`get_commit` before proceeding, and can then correct the previous turn's stale pointer as a meaning-safe mechanical fix (within ④'s existing 'mechanical fixes anywhere' charter, or as this review's own turn-mechanics update below) rather than treating it as an error to chase down after the fact."* In short: rename the ambiguous field's practical meaning to "commit I started from" (always answerable), and assign self-correction to the NEXT reader's mandatory verification step rather than asking each turn to predict its own future SHA. This review's own turn-mechanics update (section 5 of the work order) applies exactly this convention, and states so explicitly, as a worked example for future turns rather than silently doing something different from what it recommends.

---

## (g) Verdict block

### Cycle verdict: **PASS-WITH-FINDINGS**

**Rationale:** all four commits are lane-compliant with no violations; the cycle's new records are, on close verification, substantively accurate (TASK-0008's one error is a minor, non-load-bearing wording-precision issue, not a fabrication or a canon contradiction); the continuity spot-audit found zero micro-rule violations across six checked rules in four documents; both flagged conflicts (CM-01, SW-01) are genuine, well-evidenced, and correctly left un-adjudicated by their originating departments per their charters. Nothing found rises to S1/BLOCKER. The findings that exist are real and worth Creator/① attention but do not corrupt canon, break a locked asset, or invalidate any of this cycle's deliverables — hence PASS-WITH-FINDINGS rather than a clean PASS (findings exist and matter) or FAIL (nothing found blocks production or corrupts truth).

### Top-5 findings, ranked

1. **QA-12 — STATUS commit-pointer drift, cycle-wide (S2, HIGH confidence).** Every one of the four turns recorded the wrong commit convention in `STUDIO_STATUS.md`'s front-matter; zero actual harm this cycle (every turn re-verified live), but the failure mode is now proven present in 100% of samples and risks a future turn trusting stale state. Needs an Amendment 1 §A1.4 clarification from ①.
2. **QA-04 — TASK-0008's well-callback claim is a source-misreading (S3, HIGH confidence).** The variance record says "For the well" appears in neither the script nor the readers; it actually appears in the script (P40) and is dropped only at the readers layer. The practical conclusion (published EP.1 lacks the echo) survives the correction, but the record's own citation contradicts its own claim and should be fixed by ② on its next lore turn.
3. **QA-09 — CM-01/SW-01/two FX-extension questions are fully evidenced in `CANON_REGISTRY.md`/`Trailer_v2_KF_Production_Plan.md` but not cross-linked into `OPEN_QUESTIONS.md` (S3, HIGH confidence).** Discoverability gap, not a data-loss risk — recommend four short pointer rows on ①'s or the relevant department's next `OPEN_QUESTIONS.md`-touching turn.
4. **CM-01 (Cha Mi-ran v2 kit-sheet conflict) — genuine two-source disagreement, evidence favors deprecating the v2 sheet (see section (c)).** Not yet a production blocker since `Kit_Specs_DRAFT.md` already assumes the safer "regenerate fresh" path, but the underlying Character_Bible.md/Asset_Registry.md disagreement should be reconciled by ③ so the two LOCKED-lane files stop silently disagreeing.
5. **QA-11 — work-order severity scale (S1–S3) drifted from the Handbook/QA_REVIEW_TEMPLATE scale (S0–S4) (S3, HIGH confidence).** Cosmetic/process-level; both scales are internally consistent, they just don't match each other across documents. Reconcile whenever either is next touched by ①.

*(SW-01 and the STATUS-drift recommendation's implementation are the two items that would otherwise round out a top-7; both are already carried in sections (c) and (f) above and are lower-severity/lower-urgency than the five ranked here.)*

### What ① should put in front of the Creator

1. **DEC-0008 ruling remains the umbrella item** — nothing in this audit changes that recommendation; it is out of scope for ⑤ to weigh in on beyond confirming (as this review does) that every Cycle-1 deliverable correctly stayed inside the DEC-0008-compliant scope of proposals/records/drafts, with zero canon or asset-lock changes made anywhere this cycle.
2. **CM-01** — recommend the Creator either (a) bless "generate fresh in v3, treat the v2 Cha sheet as historical-only" (the reading this review's evidence favors, and the path `Kit_Specs_DRAFT.md` already assumes), or (b) explicitly carve out the v2 sheet as a documented exception in `Asset_Registry.md` if the Creator specifically wants it preserved as a reference — either resolves the two-file disagreement cleanly.
3. **SW-01** — low-stakes; recommend simply telling ② which term ("2nd-year" recommended for its lack of ambiguity) to standardize on next time it touches either file. Does not need a formal DEC-ID.
4. **QA-12 (STATUS drift)** — recommend approving the §A1.4 convention clarification proposed in section (f) so future cycles stop generating a new instance of this same finding every turn.
5. **TASK-0008's QA-04 correction** — a one-line wording fix ② can make next time it's in `ep1_adaptation_variance.md`'s lane; flagged here so it doesn't get cited elsewhere with its current, slightly-wrong phrasing in the meantime.

---

## Summary

- **Findings by severity:** S1 — 0 · S2 — 1 (QA-12) · S3 — 5 (QA-04 correction, QA-08, QA-09, QA-11, plus this review's own note on the severity-scale drift being itself S3) · S4/polish-equivalent — 0.
- **Findings by confidence:** HIGH — 9 (QA-01, QA-02, QA-03, QA-04, QA-06, QA-07, QA-09, QA-10, QA-12) · MEDIUM — 0 · LOW — 0 · UNVERIFIED (explicitly, not LOW) — 1 (QA-08's three unchecked PROMPT_LIBRARY anchors).
- **Lane-compliance verdict:** ①②③④ — all four commits **COMPLIANT**, zero violations, all four commit messages carry correct prefix + descriptive scope.
- **Recommended next steps for ① / Creator:** see "What ① should put in front of the Creator" above, items 1–5. No item on this list blocks CYCLE-0001 from being reported COMPLETE to the Creator.

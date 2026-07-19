# Q-19 — Professor Im Investigation (TASK-0024) — DRAFT

**DRAFT — INVESTIGATION REPORT FOR THE OWNER. THIS REPORT RESOLVES NOTHING.**
The ruling on Q-19 belongs to the Owner alone. No canon file, spec file, script, reader, or record row is edited by this task; nothing below locks, retcons, or decides any UNDECIDED item (Q-01…Q-22 all remain open). Every quote below is transcribed byte-exact from the pinned sources; every claim of silence was verified by search-and-absence. Night rules (Handbook Amendment 2 §A2.4, carried forward by Amendment 3) and the DEC-0008 canon-rewrite block are honored: this document is additive DRAFT, records-only.

- **Author:** ② Lore Department, CYCLE-0003 (TASK-0024, dispatched per `HANDOFFS/CYCLE-0003-EP.md`).
- **Date:** 2026-07-19.
- **Base commit:** `35f09648fae50ac6118129101211d4aec08dfaba` (HEAD at dispatch; all locators below are against this tree).
- **Provenance:** QA-238 (S2, `REVIEWS/CYCLE-0002_GATE-REPO.md`) verified the conflict real; QA-241 added the pronoun-ambiguity evidence; ① minted Q-19 at CYCLE-0002 close and queued this investigation ahead of any EP.2 drafting or Im visual work (⑤ rates the conflict S1 BLOCKER if either proceeds unresolved).

## 0. The question (Q-19, quoted from `OPEN_QUESTIONS.md`)

> Q-19 Professor Im identity/gender conflict (QA-238, S2): Ch.1:159/161 "Ask Professor Im," … "I did. She gave me the Chorus catechism…" vs Character_Bible CHAR-005 "~40s male; BLACK hair greying at temples". Same person (source contradiction needing authorized correction) or two distinct Professor Ims? Owner ruling or ② investigation recommended BEFORE EP.2 drafting or any Im visual work (⑤ rates S1 if proceeded unresolved).

## 1. Method

Full clone of `main` at the base commit. Case-aware pattern search for `Professor Im` / `Master Im` / `Im Dan-bi` / `DAN-BI` / `proctor` / `professor` across every tracked file (all `manuscript/`, `readers/`, `studio/` `.md` and `.html` files); every hit read in context; silences verified by zero-match against the same patterns. Asset ids are quoted truncated (`0f602652-…`) per house record style; they are platform asset ids, not Drive ids (QA-236 class) — this file contains no Drive ids or links (DEC-0015).

## 2. Evidence table

### 2a. Named Im references (prose → franchise canon → story bible → visual spec/locks → adaptation → DRAFT specs → compiled registry)

| # | Source (file : line — section) | Exact quote (byte-exact; bracketed ellipses mark trims) | Bearing |
|---|---|---|---|
| E1 | `manuscript/chapters/01_the_ninth_world.md` : 15 — sparring scene, Si-woo speaking | "It's just — you're *almost* there. Everyone says theory students can't fight, but your bones are good. Master Im says bones don't lie." | "**Master** Im" (martial honorific), quoted on a body/combat-assessment maxim by a sword-Etude student. Possibly-distinct third reference (per QA-238); no gender. |
| E2 | `manuscript/chapters/01_the_ninth_world.md` : 145 — library scene, Ha-eun speaking | "Professor Im says mana has always sung and always will, one Chorus, one pitch. Fine. Then why do the oldest things in this city sing a quarter-tone off, senior? What were they tuned *to*?" | Ch.1's "Professor Im" is the campus authority on **Chorus/mana doctrine** — subject-matter datum. No gender in this line. |
| E3 | `manuscript/chapters/01_the_ninth_world.md` : 159 — library scene, Han speaking | "Ask Professor Im," he said, standing, gathering his notes. | Han names one salient "Professor Im" with zero disambiguation, in a mana-doctrine context. |
| E4 | `manuscript/chapters/01_the_ninth_world.md` : 161 — library scene, Ha-eun replying to E3 | "I did. She gave me the Chorus catechism and a biscuit." | **The female-gendering line.** The "She" can only be the Professor Im of E3 that Ha-eun asked. One half of the Q-19 conflict pair. |
| E5 | `studio/01_Lore/Master_Project_Bible.md` : 20 — §2 COMPLETE STORY, CH.2 locked beats | "compressed goodbyes; Professor Im Dan-bi's warmth; […]" | Ch.2 warmth/introduction beat is locked. **Genderless.** |
| E6 | `studio/01_Lore/Master_Project_Bible.md` : 21 — §2, CH.3 locked beats | "a loved named character dies (First-Death rule; candidate Im Dan-bi — UNDECIDED)" | Q-01 linkage. Genderless. |
| E7 | `studio/01_Lore/Master_Project_Bible.md` : 50 — §7 CHARACTERS | "**IM DAN-BI** — ~40s combat-theory professor/proctor; weary ritual kindness (48 stamped failures, zero reports); Ch.3 first-death CANDIDATE (undecided)." | The lore dossier: **combat-theory** professor/**proctor**; "48 stamped failures" ties Im to Han's examinations (see §2b). **No gendered pronoun anywhere in MPB** (QA-238's ancillary item, confirmed). |
| E8 | `manuscript/bible/story_bible.md` : 44 — "## Cast (living, 9.0)" | "- **Professor Im Dan-bi** — Combat Theory professor; protects his scholarship; kind. (Introduce Ch.2. First-Death-rule candidate for Ch.3 — decide at drafting.)" | Three ancillary items in one line: (i) "Combat Theory professor" (vs E2's mana-doctrine subject); (ii) "protects **his** scholarship" — pronoun-ambiguous per QA-241: "his" = Im (gendering him male) or = the failing student whose scholarship Im's zero-reports kindness protects; (iii) "(Introduce Ch.2.)" — the on-page-introduction plan. |
| E9 | `manuscript/bible/story_bible.md` : 40 — same Cast section (context for E8's pronoun) | "- **Seo Han** — MC. "Stone Senior": theory-scholarship third-year, 0–47 in practicals, never dropped out. […]" | **Han is the cast's theory-scholarship holder with the failure streak** — the natural antecedent for E8's "his scholarship" under the QA-241 alternate reading, via E7's "(48 stamped failures, zero reports)". |
| E10 | `manuscript/bible/story_bible.md` : 70 — "## Drafting log" | "- [ ] Ch.2 — "Last Day" (compressed: goodbyes, Im Dan-bi shine, headmaster speech w/ planted sentence, keepsake funeral + hairpin silence, 9.0 keepsake chosen, midnight tear + banner "Are you still there?")" | Ch.2 "shine" beat; genderless. |
| E11 | `manuscript/bible/story_bible.md` : 146 — "## PART 2 CONSISTENCY ANCHORS" (production log) | "MINOR CAST: proctor Im Dan-bi 0f602652-… (BLACK greying hair, glasses — never blonde)" [asset id truncated here] | The published EP.1 Part 2 panels were generated against the Im Dan-bi design lock. Words genderless; the anchor is the CHAR-005 male design. |
| E12 | `manuscript/bible/story_bible.md` : 147 — same section, CONSISTENCY RULE | "This fixes the g5/g10 drift (proctor identity, floor/bg, golden-hair slip, awkward sword/body)." | Production history: "proctor identity" drift and a "golden-hair slip" were fixed by anchoring to the Im design — the origin context of "never blonde". |
| E13 | `studio/02_Art/Character_Bible.md` : 27–29 — CHAR-005 | "## CHAR-005 · PROCTOR/PROF. IM DAN-BI" · "Design lock `0f602652…`. ~40s male; BLACK hair greying at temples (**never blonde**); thin rectangular glasses low on nose; dark-grey instructor coat; clipboard + rubber stamp." · "Animation notes: stamps without looking; pushes glasses with middle finger; sighs are punctuation. Status: Ch.3 first-death CANDIDATE (undecided)." | **The male half of the conflict pair — and the ONLY primary source that uses the word "male"** (see E15/E16: the other locked surfaces state design facts without it). Title merges the roles: "PROCTOR/PROF." |
| E14 | `manuscript/manhwa/ep1_v3_script.md` : 76 — EP2 PREVIEW | "## EP2 PREVIEW (for planning): Last Day — Ha-eun debut (library, the humming, "haven't we met"), Professor Im intro, unnoticed goodbyes, keepsake funeral + the hairpin with no story, headmaster's festival speech, midnight: the sky tears and the banner asks a question it's never asked." | Adaptation plan: "Professor Im intro" is EP.2 content. Genderless. |
| E15 | `studio/00_STUDIO_RULES.md` : 33 — "## 5. Continuity Micro-Rules (LOCKED — checked every panel)" | "- Proctor Im Dan-bi: BLACK hair greying at temples (never blonde); rectangular glasses low on nose." | LOCKED micro-rule row. States hair/glasses facts; **does not contain the word "male."** |
| E16 | `studio/03_Assets/Asset_Registry.md` : 16 and : 55 | "CHAR-005-M | Proctor Im Dan-bi design lock | 0f602652-…" [id truncated] · "CHAR-005-M | "Proctor Im Dan-bi — design lock"" | LOCKED asset record rows. The lock is the image asset itself; the registry text states no gender word. |
| E17 | `studio/02_Art/Kit_Specs_DRAFT.md` : 177 — Moderator kit, micro-rules note (DRAFT doc) | "[…] that list is character-specific to Han/Si-woo/Ha-eun/Cha/Im Dan-bi/the hairpin/the sky-crack" | Name-check confirming Im's row belongs to the §5 LOCKED list (E15). |
| E18 | `studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md` : 172 — PART III registry-card UI (DRAFT doc) | "[…] Im Dan-bi's rubber stamp, "stamps without looking" (Character_Bible CHAR-005), "Practical: fail. Attendance: perfect." (`01_the_ninth_world.md`) […]" | A DRAFT spec already juxtaposes CHAR-005's stamp with Ch.1:31's **unnamed-proctor** fail call — implicit identification of the Ch.1 proctor with Im Dan-bi in a ③ proposal document. |
| E19 | `studio/07_Repository/CANON_REGISTRY.md` : 60–65 — §1 entry "Proctor / Professor Im Dan-bi" (compiled record, ④'s lane) | Identity row (: 63): "~40s combat-theory professor/proctor; weary ritual kindness (48 stamped failures for Han, zero reports — protects his cover without acknowledging it)." · Visual row (: 65): "~40s male; BLACK hair greying at temples (**never blonde**); […] clipboard + rubber stamp." | Two compiled-record data points: (i) the registry glosses E7/E8 as "48 stamped failures **for Han** […] protects his **cover**" — the studio's own record already read E8's "his" with the Han-antecedent; (ii) the "male" in the visual row is compiled from E13, not an independent source. Registry recommends, never rules — cited as documentation of prior in-house reading, not as canon. |

### 2b. The unnamed EP.1 proctor (identity-bearing adjacency — the proctor is never named in prose, script, or readers)

| # | Source (file : line) | Exact quote | Bearing |
|---|---|---|---|
| E20 | `manuscript/chapters/01_the_ninth_world.md` : 5 | "Seo Han had failed forty-seven practical examinations in a row […]" | The count entering Ch.1: 47. Ch.1's on-page exam is #48. |
| E21 | `manuscript/chapters/01_the_ninth_world.md` : 31 | ""Point and match," said the proctor, and then, with the weariness of ritual: "Seo Han. Practical: fail. Attendance: perfect."" | The on-page proctor, unnamed, ungendered in prose ("the proctor" — no pronoun anywhere in the scene). "Weariness of ritual" echoes E7's "weary ritual kindness". |
| E22 | `manuscript/chapters/01_the_ninth_world.md` : 7 / : 23 / : 187 | "so that no proctor in ten years had once leaned forward and thought, *wait.*" · "The proctor called positions." · "he endured it the way he endured proctors and customs officers and one memorable exorcist" | Generic proctor references; no identity or gender. |
| E23 | `manuscript/manhwa/ep1_v3_script.md` : 56 / : 62 — P42, P48 | "P42. Sparring hall. Bored proctor, clipboard. 💬 PROCTOR: "Practical re-exam number forty-eight. Seo Han."" · "P48. 💬 PROCTOR (sigh): "Point. Seo Han — fail." […]" | The script stages the proctor with **CHAR-005's exact tells** — the clipboard prop (E13) and the sigh (E13 "sighs are punctuation") — still unnamed, ungendered in text. |
| E24 | `readers/episode1_part2.html` : 126 / : 155 (published derivative output) | speaker label "PROCTOR": "PRACTICAL RE-EXAM NUMBER FORTY-EIGHT. SEO HAN." · "POINT. SEO HAN — FAIL. AGAIN." | The published EP.1 text names the speaker only "PROCTOR" — **no name, no gender, anywhere in published text**. The published panel ART was anchored to the Im Dan-bi male design (E11–E12); art content is outside this text-only verification (flagged, not verified — same scope discipline as the variance record). |
| E25 | `studio/02_Art/Art_Direction.md` : 35 | "**Environment/character anchor stacks** (plate + master per call + restated hair/scar/outfit text) ended the drift class of bugs (changing proctor face, floors, golden-hair slips, broken anatomy)." | Corroborates E12's production history. |
| E26 | `studio/02_Art/Environment_Bible.md` : 7 — ENV-001 | "[…] proctor's lectern (far wall) […]" | Role furniture in the locked sparring-hall plate; no identity content. |
| E27 | `studio/06_Operations/CONTINUITY_LEDGER.md` : 4 | "cover intact (0–48 practicals after EP1's exam)" | Ledger-level confirmation of the 48 count that E7 attributes to Im's stamp. |

**Why 2b matters:** E7's "(48 stamped failures, zero reports)" + E20/E21/E27's arithmetic (47 before Ch.1 + the on-page #48) means MPB itself credits Im Dan-bi with stamping the failure administered **on-page in Ch.1** by "the proctor." Read with E23 (CHAR-005 props/tells in the script) and E11–E12 (published panels anchored to the CHAR-005 design), the repo's own documents treat Ch.1's unnamed exam proctor as Im Dan-bi in all but name. This is **new evidence assembled by this investigation** (not in QA-238/QA-241), and it qualifies the ancillary item "Im Dan-bi introduced on-page only in Ch.2" (E8's "(Introduce Ch.2.)", E14): the *named, narrative* introduction is Ch.2, but on the proctor-identity reading Im Dan-bi is already on-page unnamed in Ch.1 prose and already visually published in EP.1 Part 2's exam panels.

### 2c. Documented silences (verified by zero-match)

| Surface | Result |
|---|---|
| `manuscript/chapters/00_prologue.md` | ZERO Im/professor/proctor references. |
| `readers/episode1_part1.html` | ZERO. |
| `studio/06_Operations/CONTINUITY_LEDGER.md` | ZERO Im references (its charter is per-scene state baselines; Im has no entry — E27 is the only adjacency). |
| `studio/02_Art/Effects_Bible.md` | ZERO. |
| `studio/04_Storyboards/` (both files) | ZERO. |
| Readers, both files, "catechism"/"biscuit" | ZERO — **the female-gendering line E4 has no published-adaptation counterpart**; Ha-eun's library scene is wholly deferred to EP.2 (per the variance record). The conflict has not shipped to the derivative-output text layer. |

### 2d. Operations / QA trail (context, not canon)

Q-01 (`OPEN_QUESTIONS.md` : 2) — Ch.3 first-death candidacy, UNDECIDED, unaffected here. Q-19 (: 20) — this question. QA-238 + QA-241 (`REVIEWS/CYCLE-0002_GATE-REPO.md` : 97–139) — the registration this report executes. `CHANGELOG.md` : 101 and `STUDIO_STATUS.md` : 20 — the mint and the standing S2 warning. `WORK_IN_PROGRESS/ep2_outline_proposal.md` Beats 3–4 — the EP.2 beats this ruling gates. `manuscript/manhwa/ep1_adaptation_variance.md` : 41 — the fail-call variance row (adaptation trimmed "Attendance: perfect").

**Census:** 19 named-Im evidence rows (E1–E19) across 10 files + 8 unnamed-proctor / identity-adjacent rows (E20–E27) + 6 verified silences. The word "male" occurs in exactly one primary source (E13); the female pronoun in exactly one (E4); every other surface is genderless or ambiguous (E8).

## 3. The conflict pair, exactly

- `manuscript/chapters/01_the_ninth_world.md` : 159 / : 161 — "Ask Professor Im," → "I did. **She** gave me the Chorus catechism and a biscuit." (MANUSCRIPT_CANON)
- `studio/02_Art/Character_Bible.md` CHAR-005 : 28 — "~40s **male**; BLACK hair greying at temples (**never blonde**); […]" (VISUAL_SPEC carrying a LOCKED design asset, E16)

Under the one-person premise these cannot both stand. Under the two-person premise neither needs to move. Which premise is true is not derivable from the repo — it is an authorial fact only the Owner holds.

## 4. Reading A — TWO DISTINCT IMs (surname collision)

Ch.1's "Professor Im" (E2–E4) is a **Chorus-doctrine academic, female**, existing so far only in dialogue; CHAR-005's **Im Dan-bi** is the ~40s male combat-theory professor/proctor, design-locked, to be introduced on-page (named) in Ch.2.

**What each text then means.**
- E2/E3/E4 cohere internally: Ha-eun (a theory student, E9-adjacent) consulted the mana-theory authority; Han recommended the same woman; she answered with orthodoxy ("the Chorus catechism") — exactly what a doctrine academic would hand a student poking at the one question orthodoxy cannot answer. The subject-matter tension QA-238 recorded (Chorus/mana doctrine vs "combat-theory") dissolves: each Im owns their subject.
- E1's "Master Im" most naturally binds to Im Dan-bi under this reading (a sword-Etude student quoting a *combat*-theory instructor on bones, with the martial honorific "Master"), but the binding is genuinely open — a sub-question the Owner would need to settle at Ch.2/EP.2 drafting.
- E7/E8's dossiers describe only Im Dan-bi; the theory Im has **no dossier, no design, no registry row** — under Reading A that is a real, permanent gap in an otherwise fully-dossiered cast, created retroactively.
- E20–E27 (proctor identity) is untouched: Im Dan-bi still stamps Han's 48 failures; the published EP.1 proctor panels stay correct.

**Evidence FOR A:** the subject-matter split (E2 vs E7/E8); "(Introduce Ch.2.)" (E8) sits more comfortably if Ch.1's dialogue-Professor-Im is somebody else; E4's "She" needs no correction; surname collision is naturalistic.

**Evidence AGAINST A:** total bible/spec silence about any second Im (in a canon where every referenced authority figure has a dossier, the silence is anomalous — though silence is absence-of-record, not disproof); E3's undisambiguated "Ask Professor Im" reads as unique reference within the academy; the production surface only ever conceived one Im (E11, E16).

**New canon obligations if the Owner rules A:** (1) the theory Im becomes a real minor character — needs at minimum a name or standing disambiguator (e.g., by field or given name) authored by the Owner via ②, as new canon (DEC-0008-sensitive: additive dossier, not a rewrite); (2) `Character_Bible.md` / MPB §7 / story_bible Cast additions (②/③ lanes, Owner-approved); (3) ④ registry: a second-Im row plus an IM-01 CONFLICT-FOR-QA closure note; (4) Ch.2/EP.2 must introduce Im Dan-bi with explicit disambiguation so readers do not bind E4's "She" to him; (5) a design (③) only if/when the theory Im is ever staged on-page — E4-type dialogue mentions require none; (6) E1's "Master Im" binding recorded whichever way the Owner rules it.

## 5. Reading B — ONE IM, SOURCE CONTRADICTION

Ch.1's Professor Im IS Im Dan-bi; then E4's "She" and E13's "~40s male" are a hard locked-lane contradiction, and one source must be corrected under authority.

**Precedence picture (`SOURCE_OF_TRUTH.md` — itself PROPOSED, DEC-0008 PENDING; the ladder informs, the Owner rules):**
- The "male" textual claim lives at rank 6 (`02_Art` VISUAL_SPEC, E13) — **below** chapters (rank 5, E4).
- But the design **asset** CHAR-005-M sits in `Asset_Registry.md` at rank 3 ("LOCKED visual facts"), **above** chapters — if the depicted sex of a locked design titled "Proctor Im Dan-bi — design lock" counts as a locked visual fact of that character (the registry text itself never says "male"; the fact lives in the image, E16).
- MPB (rank 4, above chapters) is genderless (E7) and adjudicates nothing.
- So the ladder does not mechanically settle B: it turns on whether the asset's depiction is a rank-3 "visual fact" or merely rank-6 spec support. Both readings of the ladder are defensible; **an Owner ruling is required either way**, and rank 1 (explicit creator instruction) overrides the ladder regardless.

**Sub-branch B1 — male stands; the prose line is the erratum.** Correction touches exactly one canon word: E4's "She" → "He" in `manuscript/chapters/01_the_ninth_world.md` (MANUSCRIPT_CANON). Interactions: this is a substantive canon rewrite — **blocked by DEC-0008's pending state and by night rules**; it can only be executed after an explicit Owner ruling (and through ②'s lane, archive-don't-delete, with a revision note; the variance record and ledger need no change — the line has no adaptation counterpart yet, E2c). Downstream: EP.2's adaptation of the library scene (outline Beat 3 pulls the Ch.1 text verbatim) must carry the corrected pronoun; ④ records IM-01 as resolved-by-ruling. Everything else in §2 already coheres with B1.

**Sub-branch B2 — female stands; the design record is the erratum.** Correction touches: `Character_Bible.md` CHAR-005 (E13), the LOCKED design asset CHAR-005-M and its `Asset_Registry.md` rows (E16), `studio/00_STUDIO_RULES.md` §5 row (E15), the registry visual row (E19), plus a redesign (③) and — via E11/E12/E24 — a decision about the **already-published EP.1 Part 2 exam-proctor panels**, which were anchored to the male design. Interactions: `SOURCE_OF_TRUTH.md`'s own header blocks "asset-lock changes" while DEC-0008 is pending — B2 is **double-blocked** (pending register + night rules) and is the only branch that breaks a locked asset (S1-class event under Handbook §21 if done carelessly). The §5 micro-rule row sits in the same LOCKED list as the DEC-0006 micro-locks (E15/E17); whether its lock authority derives from DEC-0006 or from the ART v3 FINAL LOCK event is itself a records question — under either derivation, unlocking is Owner-level. A B2 mitigation exists that keeps the published panels: declare the EP.1 exam proctor a **different person** from Professor Im (female) — but that voids E7's "48 stamped failures" gloss (MPB correction needed) and effectively re-creates a two-person structure with the roles swapped; it inherits most of Reading A's obligations plus MPB surgery.

**Evidence FOR B (one Im):** the anomalous silence about any second Im; E3's unique-reference phrasing; CHAR-005's merged title "PROCTOR/PROF." matching prose usage of both "Professor Im" (E2–E4) and an exam proctor (E20); combat-theory at an Etude academy plausibly covers Chorus doctrine (Etudes ARE applied mana — E2's catechism answer is not out of subject for E7's professor); the registry's compiled reading of E8 (E19) removes the one textual "male-leaning" pronoun from the scales, leaving E13 alone against E4 — a one-word-vs-one-word conflict typical of an inadvertent drift, not of two planned characters.

**Evidence AGAINST B:** the subject-matter registers still sit oddly (a combat-theory proctor as the source of "the Chorus catechism"); "(Introduce Ch.2.)" plus E14's "Professor Im intro" read most simply if Ch.1's speaking references were meant to point elsewhere — though dialogue mentions before a planned on-page debut are ordinary craft, and §2b's proctor identification already stretches "Introduce Ch.2" under B regardless of gender.

## 6. Implications either way

- **EP.2 pipeline (TASK-0005 / TASK-0017).** The outline's Beat 3 (Ha-eun debut — adapts the Ch.1 library scene, i.e., the E2/E3/E4 text) and Beat 4 (Im Dan-bi warmth/introduction — stages Im on-panel) are both direct dependents. Until Q-19 is ruled: no EP.2 script words for either beat (⑤'s S1 escalation, `STUDIO_STATUS.md` : 20). Under A, Beat 4 needs disambiguation language and Beat 3 keeps E4 verbatim. Under B1, Beat 3's adaptation must carry the corrected pronoun AND the prose correction must land first or simultaneously — publishing EP.2 with "He" while Ch.1 prose still reads "She" would put two published surfaces in live contradiction. Under B2, Beat 4 cannot be staged at all until redesign.
- **Future Im visual work (③).** All Im generation is ruling-blocked. Under A: the male CHAR-005 design stays valid for Im Dan-bi; a second-Im design becomes a *potential* future need (none needed for EP.2 — E4 is a mention, not an appearance). Under B1: CHAR-005 stays valid unchanged. Under B2: CHAR-005-M is deprecated (archive-don't-delete → Asset_Registry DEPRECATED section), redesign + relock required, and the published EP.1 exam-proctor panels need an Owner call (leave as-is with an errata record, republish, or re-attribute the proctor) — republication itself is separately blocked by DEC-0008.
- **CONTINUITY_LEDGER / registry hygiene.** The ledger is correctly Im-silent today (baseline format; QA-238 already ruled out format-stretching). Whichever way Q-19 goes, Im enters the ledger when EP.2 lands — the ruling must precede that entry or the ledger inherits the ambiguity. ④'s next authorized registry pass should record IM-01 as a §1 CONFLICT-FOR-QA row now (already QA-recommended) and, post-ruling, close it citing the decision; under A the registry additionally needs the second-Im row; under B2 the E19 visual row and E15/E16 rows all change under the same ruling's authority.

## 7. Resolution options (all require Owner ruling; none is actioned by this report)

- **OPTION 1 — Rule TWO IMs.** Declare Ch.1's Professor Im a distinct female Chorus-doctrine academic; Im Dan-bi unchanged. *Cost:* zero edits to existing canon bytes; new obligations instead — name/disambiguator, dossier additions, registry row, Ch.2 disambiguation care, E1 binding (all additive, Owner-approved). *Risks:* minor-cast bloat; the bibles' historical one-Im silence becomes a permanent oddity; reader-confusion risk in Ch.1's library exchange persists until Ch.2 manages it; a second "Professor Im" at one academy invites future drift if disambiguation discipline ever slips.
- **OPTION 2 — Rule ONE IM, MALE (design stands; prose erratum).** Authorize the one-word correction of Ch.1 : 161 ("She" → "He") through ②'s lane with archive-don't-delete + revision note. *Cost:* the smallest possible: one word, one revision note, IM-01 closure; no asset, no republication (E4 has no published derivative counterpart, §2c). *Risks:* overrides what may have been a deliberate authorial signal in the prose (only the Owner knows); requires piercing the DEC-0008 canon-edit block by explicit ruling; leaves the mild subject-matter oddity of E2 (absorbable — a combat-theory professor reciting standard Chorus catechism contradicts nothing on record).
- **OPTION 3 — Rule ONE IM, FEMALE (prose stands; design record falls).** Correct CHAR-005 + §5 row + registry; deprecate/redesign CHAR-005-M; decide the published EP.1 panel question. *Cost:* highest — breaks a locked asset (S1-class handling), touches four record surfaces plus ③ design work, and raises a republication question that DEC-0008 separately blocks. *Risks:* destabilizes the exact design that production hardened against drift (E12/E24); the keep-the-panels mitigation (exam proctor ≠ Im) forces MPB surgery on E7's "48 stamped failures" and re-creates a two-person structure anyway.

## 8. Recommendation (clearly labeled; freely rejectable; decides nothing)

② recommendation, conditional on the one fact only the Owner holds — what E4's "She" was *meant* to do:

- If "She" was **inadvertent** (drafting drift against the already-locked male design): **Option 2** — it is the only resolution whose total cost is one word, and the assembled evidence (one-source "male" E13 vs one-source "She" E4, all other surfaces genderless or ambiguous, one-Im production history, §2b's proctor identification) is fully coherent under it.
- If "She" was **intentional** (a female professor was meant to exist in that scene): **Option 1** over Option 3 — it preserves both the prose and the locked/published visual record at zero retcon cost, paying instead in additive bookkeeping. Option 3 is recommended **against** unless the Owner positively wants Im Dan-bi female on creative grounds that outweigh a locked-asset break and a published-art question.

② holds no view on which condition is true and this report resolves nothing.

## 9. Fair-play check (Handbook fair-play law: withhold, never lie)

- **Reading A:** the narration never lied — it withheld that two Ims exist. E4 remains true in-world. Residual risk is confusion, not deception; Ch.2's introduction must disambiguate for the withhold to stay fair.
- **Reading B1:** no *in-world* lie — E4 becomes an out-of-world drafting error, and Ch.1 prose is published canon text, so the correction is a visible erratum (archive-don't-delete + revision note keeps faith with readers). **Flag:** if EP.2 shipped "He" while Ch.1 still read "She" (or vice versa), the two published surfaces would actively contradict — to a cross-reader that reads as the text having lied somewhere. Sequencing the correction with EP.2 (per §6) prevents this.
- **Reading B2:** no published **text** ever asserted Im's maleness (E24: "PROCTOR" only; prose never genders the proctor) — the male commitment shipped only in the art layer. Correcting to female makes published EP.1 panels retroactively wrong (art erratum, not narrative lie); the panels-preserving mitigation avoids even that at the price described in §5/§7.
- Net: **no reading forces the conclusion that the narration has LIED to the reader as written today**; the lie-risk is prospective and lives entirely in mis-sequenced corrections (B1 flag above) — a scheduling discipline, not a story problem.

## 10. Sealed-territory note (T2 discipline)

One analytically relevant line is deliberately **not pursued**: E4 is reported speech by Yoo Ha-eun, whose own truth is PRIVATE_SEALED (T2) — story_bible Cast: "(See private bank T2 — do not reveal.)". Evaluating her reliability as a witness to Professor Im's gender would require reasoning about what Ha-eun is and knows — sealed-adjacent. **Marked SEALED (T2); line of analysis stopped.** This report treats E4 at face value as ordinary dialogue, and any resolution that turns on Ha-eun's hidden nature is the Owner's territory alone. No twist-bank content is referenced, reconstructed, or hinted at anywhere in this report.

## 11. What this report does not do

No canon, spec, script, reader, or record file was edited by this task (the same turn's separate QA-240 banner fix on `ep1_adaptation_variance.md` is a records-only status correction, pre-authorized by the CYCLE-0003 dispatch, and touches no Im content). No Q-number minted or closed; Q-01/Q-19 remain OPEN; no lock touched; no UNDECIDED item resolved; no Drive ids/links; no generation. Registry IM-01 recording remains ④'s lane; the ruling remains the Owner's.

---

*② Lore Department · CYCLE-0003 · TASK-0024 · base `35f09648…` · DRAFT — awaiting Owner ruling on Q-19.*

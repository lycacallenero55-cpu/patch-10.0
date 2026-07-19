# QA Review — CYCLE-0003 Full-Cycle Review (first under Amendment 3 / DEC-0016)

- **Date:** 2026-07-19 · **Author:** ⑤ Quality Assurance · **Task ID:** CYCLE-0003 cycle-end review (Handbook Amendment 3 §A3.3; assigned in `HANDOFFS/CYCLE-0003-EP.md`)
- **Scope:** EVERY commit of CYCLE-0003 — the seven commits from base `ecd652b69fad1e946b00e7c9e70e8f75e6e18613` (CYCLE-0002 close) to HEAD `21971bd416ca1956287d73bad6d5b6d7c319d8b0`: ①'s three ops commits (`35f09648`, `04f08e82`, `21971bd4`), ②'s turn (`b5767294`, `27190692`), ④'s turn (`201edb3f`, `107bb408`), plus the PLAN-level ③ skip. Review dimensions per §A3.3: lane compliance, content verification against canon/spec sources and the laws (v1 §3, `00_STUDIO_RULES.md` §5, SOURCE_OF_TRUTH precedence), label discipline, turn mechanics (A1.4), and the cycle-wide cross-cutting checks (night rules, leak scan, sealed material, ledger hygiene). ⑤ verifies and recommends; it fixes nothing (Handbook §8.5/§21). This review touches ONLY this one new file; STATUS/CHANGELOG recording of the review is ①'s at cycle close (ops lease, see QA-245).
- **Method:** independent verification from a fresh clone of `github.com/lycacallenero55-cpu/patch-10.0` at HEAD (`git ls-remote` confirms `main` is the ONLY branch, at `21971bd4…`). Nothing was taken from department reports on faith: every diff was re-derived opcode-level from raw blob bytes (difflib over `git show` output), every claimed blob SHA-1 recomputed from bytes (`sha1("blob <len>\0" + bytes)`), every quoted evidence string re-read at its claimed file:line in the base tree, and every silence claim re-verified by zero-match search. Department handoff manifests were compared against ⑤'s own derivations only AFTER those derivations were complete.

---

## (a) Commit chain + attribution — CLEAN

`git log` parent-links from the fresh clone (authoritative, = GitHub bytes):

| # | Commit | Parent | Prefix | Files touched | In-lane |
|---|---|---|---|---|---|
| 1 | `35f09648fae5` | `ecd652b6` (base) | `[①-EP]` | HANDBOOK · CHANGELOG · DECISION_LOG · HANDOFFS/CYCLE-0003-EP.md · STUDIO_STATUS · TASK_QUEUE (6) | ✅ ① lane |
| 2 | `b5767294817d` | `35f09648` | `[②-LORE]` | `manuscript/manhwa/ep1_adaptation_variance.md` · `WORK_IN_PROGRESS/professor_im_investigation_DRAFT.md` (2) | ✅ ② lane + shared WIP carve-out |
| 3 | `271906926faa` | `b5767294` | `[②-LORE]` | `HANDOFFS/CYCLE-0003-LORE.md` only | ✅ own-turn handoff |
| 4 | `04f08e824573` | `27190692` | `[①-EP]` | STUDIO_STATUS only | ✅ ① lane |
| 5 | `201edb3f739a` | `04f08e82` | `[④-REPO]` | `07_Repository/CANON_REGISTRY.md` · `07_Repository/INDEX.md` · `07_Repository/REFERENCES/PMU_style/INDEX.md` (3) | ✅ ④ lane |
| 6 | `107bb408cb35` | `201edb3f` | `[④-REPO]` | `HANDOFFS/CYCLE-0003-REPO.md` only | ✅ own-turn handoff |
| 7 | `21971bd416ca` | `107bb408` | `[①-EP]` | STUDIO_STATUS only | ✅ ① lane |

Exactly the seven expected commits; strictly linear (each sole-parented on its predecessor); nothing interleaved, nothing unattributed; author timestamps strictly increasing (10:58:04Z → 12:17:50Z); no other branch exists on the remote. ⑤'s reserved files (REVIEWS/, CONTINUITY_LEDGER, VALIDATION_PROFILE, INCIDENTS) untouched cycle-wide. All seven messages carry the correct department prefix and reconstruct scope without opening the diff (house standard met). **Lane-compliance verdict: all seven commits COMPLIANT.**

## (b) ① governance mechanics — VERIFIED

- **Handbook (35f09648): insertion-only, Amendment 2 byte-preserved.** Numstat +37/−0. Opcode diff = exactly two insert blocks: the 2-line SUPERSEDED banner (+ trailing blank) under the Amendment 2 heading, and the 35-line Amendment 3 block (§A3.1–A3.6 + separator) before "RETAINED v1 TEXT". Removing exactly those inserted lines from the new blob **recomputes the prior blob `eb25469c17353fd9c3c3afeb64cc3741ef5d26dc` byte-for-byte** — the Amendment 2 body is preserved unmodified, as the banner promises. Amendment 3 text correctly carries §A2.4 Night Rules forward and confines supersession to A2.1–A2.3.
- **DECISION_LOG: pure single-row append.** DEC-0016 row only (+1/−0). Decided-by reads "Creator (web order, conductor thread)" — the flow change is **recorded as the OWNER'S decision, not made by ①** (night-rules compliant; see also (e)).
- **TASK_QUEUE: one cell + one row exactly.** TASK-0023 status cell PROPOSED → "READY (CYCLE-0003 ④ …)"; TASK-0024 row appended (IN_PROGRESS, ② Lore, records-only, ruling stays with Owner). Nothing else changed (+2/−1).
- **CHANGELOG: pure append** (+6/−0 at EOF): DEC-0016/flow change + CYCLE-0003 opening entry, accurate against the tree.
- **`HANDOFFS/CYCLE-0003-EP.md`: complete work order** — cycle order under A3.2, per-department assignments with objectives/constraints/success criteria (②a QA-240, ②b TASK-0024, ④ TASK-0023, ⑤ full-cycle review), standing constraints (night rules, DEC-0008, DEC-0015 containment, sealed bank), risks.
- **③ skip recorded with reason (Amendment 3 §A3.2)** in all three places checked: CYCLE-0003-EP.md ("zero night-legal scope — all ③ work gated on Owner rulings Q-20/Q-21/Q-22, TASK-0003, DEC-0009"), CHANGELOG entry, and STATUS. ✅
- **STATUS replacements consistent at each point.** 35f09648: cycle open, ② in flight, ④ READY, resume ②→④→⑤→①. 04f08e82: ② DONE citing the real SHAs (`b5767294`, `27190692`), `last_verified_commit` = 27190692, resume ④. 21971bd4: ④ DONE citing `201edb3f`/`107bb408`, `base_remote_commit` = 04f08e82 / `last_verified` = 107bb408 (QA-12 convention honored), resume ⑤ full-cycle review with correct scope and the CRITICAL-halt rule restated. No claim in any of the three STATUS states was found ahead of, or behind, the actual tree at its commit.

## (c) ② turn — VERIFIED (QA-240 + TASK-0024)

**(c1) QA-240 banner fix (`b5767294`).** Opcode diff of `ep1_adaptation_variance.md` (base blob `63b63bfd`, 36,943 B → `f526a278`, 36,952 B): exactly ONE replace opcode, line 3 → line 3; 84 lines before and after; every other byte identical. New wording "**RECORD — ACCEPTED (⑤ gate-verified CYCLE-0002; per QA-240)**" is accurate to ledger truth: `TASK_QUEUE.md` TASK-0008 = "ACCEPTED (⑤ gate-verified CYCLE-0002)"; CHANGELOG records the transition; GATE(②) `2532de41` verified the record. Inline citation was one of the two dispatch-authorized forms; the dispatch's success criterion (diff confined to the banner) is met exactly.

**(c2) TASK-0024 investigation DRAFT (`dcafd924…`, 30,472 B, +156 lines).**
- **Lane / records-only:** ②'s two commits touch only the 2 authorized files + own handoff. No canon file modified beyond the authorized banner line; OPEN_QUESTIONS.md untouched this cycle (last touched at base `ecd652b6`); **Q-01…Q-22 all still open**; no Q minted/closed; no lock; no retcon; TASK_QUEUE/STATUS/CHANGELOG correctly left to ① (declared).
- **Evidence spot-check — 30 rows/quotes re-verified byte-exact at the declared base tree `35f09648`,** including all dispatch-mandated items: the **conflict pair** (Ch.1:159 "Ask Professor Im," he said…; Ch.1:161 "I did. She gave me the Chorus catechism and a biscuit."; Character_Bible CHAR-005:27–29 incl. ":28 ~40s male; BLACK hair greying at temples (**never blonde**)…"); the **48-failures arithmetic chain** (MPB §7:50 "(48 stamped failures, zero reports)" + Ch.1:5 "failed forty-seven practical examinations in a row" + Ch.1:31 on-page exam #48 + script :56 P42 "Practical re-exam number forty-eight." with clipboard and :62 P48 "(sigh)" — CHAR-005's exact tells — + CONTINUITY_LEDGER:4 "0–48 practicals after EP1's exam"); the **published-panel anchor** (story_bible:146 "MINOR CAST: proctor Im Dan-bi 0f602652-… (BLACK greying hair, glasses — never blonde)" and :147 the g5/g10 "proctor identity… golden-hair slip" fix log); plus E1/E5/E6/E8/E9/E10/E14/E15/E16/E17/E18/E19/E22 and the readers' :126/:155 PROCTOR lines. All hold.
- **Negative claims verified by absence:** "catechism"/"biscuit"/"She gave" have ZERO matches in `readers/episode1_part1.html` AND `readers/episode1_part2.html` — the E4 "She" line has **no published-adaptation counterpart**, exactly as claimed. Also re-verified ZERO Im/professor/proctor content in 00_prologue.md, readers part 1, Effects_Bible, both 04_Storyboards files, and CONTINUITY_LEDGER (E27 the only adjacency). The 19-rows/10-files/8-adjacent/6-silences census arithmetic is exact.
- **Sealed-territory discipline:** §10 quotes story_bible:42's "(See private bank T2 — do not reveal.)" accurately, marks the Ha-eun witness-reliability line **SEALED (T2)** and stops; zero twist-bank reference, reconstruction, or inference anywhere in the file. ✅
- **UNDECIDED / Owner discipline:** DRAFT banner states it "RESOLVES NOTHING"; both readings argued through SOURCE_OF_TRUTH precedence with the register's own PROPOSED/DEC-0008-pending status acknowledged; all 3 options expressly require Owner ruling; the ② lean is conditional, clearly labeled, and freely rejectable; **fair-play check present and sound** — its conclusion (no reading means the narration has lied as published today; the lie-risk lives in mis-sequenced future corrections, a scheduling discipline) follows from the verified evidence, in particular the E24 finding that published text never names or genders the proctor and §2c's no-counterpart result.
- **Handoff (`27190692`):** manifest (turn shape, parents, blob SHAs, byte sizes, one-line diff claim) matches ⑤'s independent derivation in full; deviations (two commits per live dispatch; inline citation; additive sweep widening; no ops writes) declared plainly and check out. Quote-convention nits logged as QA-244 (S4).

## (d) ④ turn — VERIFIED (TASK-0023)

**(d1) `CANON_REGISTRY.md` (+5/−4, blob `f8da9aa2`, 61,928 B).** Opcode diff = exactly 4 in-place replaces + 1 insert, confined to the declared zones; every other line byte-identical:
- **§2 "Registry cards" row (:99) — record-only refresh** on the monster-row precedent: records ③'s PART III "LEDGER UNDER REVISION" DRAFT PROPOSAL (gate-passed `31b36ee3`) with "PROPOSED, not canon: no design exists until the Owner selects and locks"; status cell stays **UNDECIDED** with the Q-22 pointer; queued choices compiled from OPEN_QUESTIONS/TASK_QUEUE; **no design content adopted**. ✅
- **QA-239 cells now byte-exact — re-verified against sources:** §3 mountain row (:133) quotes "The man who could cut rain" = Ch.1:107 keepsake passage, byte-exact; §3 tower row (:134) quotes "had once been a promise between apprentices" = Ch.1:109, byte-exact; §4 Cha row (:170) gains exactly the `manuscript/bible/story_bible.md` "Cast" pointer (story_bible:43 carries the quoted salts-broth sentence verbatim; quote text unchanged per QA-239's own prescription). Minimal-change proof: each of the three rows differs from its predecessor by exactly the prescribed substring/pointer and nothing else.
- **Note 6 (:225) appended** — accurately describes (a)/(b), declares the untouched §1 adjacent candidate, restates the razor. ✅
- **The two declared verbatim-coincidence adaptations handled correctly:** (1) Ch.1:7 does contain lowercase "a man who could cut rain" ("he had studied under a man who could cut rain") — but QA-239 measured the row against its cited pointer, the keepsake passage, so the ":107 The man…" form is the right normalization; ④'s deviation 4 flagged this precisely so this review wouldn't trip on it. Confirmed. (2) The Cha-row quote keeps conventional mid-sentence lowercase "the patch…" vs story_bible's sentence-initial "The patch…" — citation-add, not requote, per QA-239. Confirmed.
- **QA-239 status transition:** correctly noted as fixed in the INDEX's GATE-REPO row; no prior QA number renumbered or altered anywhere in the cycle's diffs.

**(d2) `REFERENCES/PMU_style/INDEX.md` (+4/−4, blob `bbf0d21d`, 17,640 B).** All four changed lines in place, no row deleted. §A heading → "28 reviewed rows (27 effective reference strips)" + count-correction sentence naming PMU-142-A; the PMU-142-A row kept, SHA-256/description untouched, Ref cell marked "⚠ (capture artifact — provenance only, not a reference)"; §B.2 → "211 … raw / 172 distinct names … counts verified by ⑤, QA-219". **The 27-effective framing and the 211/172 figures match ⑤'s own prior verified numbers exactly** (OPS-0002 gate: QA-218 "effective reference set is 27"; QA-219 "211 raw / 172 distinct"). The enclosing totals (260/345/5/85/357), previously verified, are untouched. ✅

**(d3) `07_Repository/INDEX.md` (+15/−9, blob `25006281`, 29,562 B).** 9 corrective in-place replacements + 6 added rows, no restructure — re-verified against the actual tree: as-of pointer → `04f08e82` (the true refresh base); Handbook row → Amendments 1–3 with Amendment 2 SUPERSEDED pointer (matches the actual file); counters → TASK-0024 / DEC-0016 (0008/0009/0015 still PENDING — matches DECISION_LOG) / Q-22 (matches OPEN_QUESTIONS); stale "this turn" marker retired on the CYCLE-0002-REPO row; PMU row updated consistently with (d2); "Last refresh" note updated. All 6 added rows point at files that exist at HEAD (CYCLE-0002-CLOSE, CYCLE-0003-EP, CYCLE-0003-LORE, CYCLE-0002_GATE-REPO, professor_im_investigation_DRAFT — correctly marked "DRAFT, records only; resolves NOTHING" — and the same-turn self-listed CYCLE-0003-REPO, declared deviation, CYCLE-0001/0002 precedent). Tree-diff `31b36ee3..04f08e82` + this turn confirms this is the COMPLETE new-file set — no tracked file is missing from the index. ✅

**(d4) Handoff (`107bb408`):** manifest (commit SHAs, sole-parent, all three blob SHA-1s + byte sizes, per-file diff shapes incl. "the 4 removed lines are exactly the four declared cells") matches ⑤'s independent derivation in full; deviations 1–9 all declared and all check out, including deviation 9 (no ops/lane-external writes — confirmed by the commit file lists).

## (e) Cross-cutting — one CRITICAL finding; all else clean

- **Night rules (§A2.4, cycle-wide):** additive DRAFT/record work only — ✅ no LOCK created/changed (all status-cell values in touched rows unchanged except the authorized TASK-0023 cell and the recorded-UNDECIDED §2 refresh), no retcon (the only canon-file edit is the authorized 1-line banner on a RECORD file), no restructure (all diffs in-place/append), **no Owner decision made** — DEC-0016 is recorded as decided by "Creator (web order, conductor thread)", and everything else decision-shaped is queued (Q-19 options report, Q-22 pointer, DEC-0008/0009/0015 untouched-PENDING).
- **Sealed twist bank:** untouched cycle-wide (off-repo per DEC-0002/Q-12; no commit references, reconstructs, or infers toward it; ②'s DRAFT §10 stop-line verified).
- **DEC-0015 containment / leak scan:** every file TOUCHED this cycle was token-scanned — **no CYCLE-0003 commit added any Drive id/link** (all 396 added lines clean; the ids present in ②'s DRAFT are platform asset ids in truncated `0f602652-…` form, QA-236 class). **HOWEVER**, the mandated cycle-wide scan surfaced a pre-existing repo-state breach: the PMU source folder's Drive id is present in the repo at HEAD — see **QA-242 (S0 CRITICAL)**. DEC-0015 containment is therefore **NOT intact** at HEAD, contrary to the standing-constraint line in the cycle plan.
- **Commit-message discipline:** all seven messages correct-prefixed, descriptive, and truthful against their diffs (each verified above). ✅

## (f) Ledger hygiene

- QA ledger stood at **QA-241** (CYCLE-0002_GATE-REPO). This review's findings are numbered **QA-242 through QA-247**; ledger now ends at **QA-247**.
- ④'s pass did not renumber or damage any prior QA reference (all QA-mentions added this cycle — QA-218/219/238/239/240/241 — are consistent with their definitions; no existing QA-ID string was modified in any cycle diff).
- Known leftovers flagged, not fixed, per below: QA-246 (①-lane Handbook subtitle/v-note) and QA-247 (④-lane §1 Cha citation candidate + "28" echoes — already self-logged by ④).

---

## Findings

### QA-242 — Drive-folder id/link of the Owner's private PMU folder present in the PUBLIC repo (DEC-0015 containment breached; pre-existing, surfaced by this review's cycle-wide scan)
- **Severity:** S0 CRITICAL
- **Confidence:** HIGH
- **Type:** repository / private-material (v1 §3.8)
- **Evidence:** (1) `studio/03_Assets/Asset_Registry.md` line 67 ("Reference library provenance" note) carries the FULL `drive.google.com/drive/folders/<folder-id>` URL of the Owner's "pick me up" folder — introduced at `da35b6d` ("[ARCHIVE] final knowledge drain from novel thread", pre-department bootstrap) and live at HEAD. (2) `studio/06_Operations/CHANGELOG.md` line 89 (CYCLE-0002 HALT entry) carries the bare 33-char folder id — introduced at `7befebf` ("[①-EP] HALT…", an ①-lane ops commit that predates DEC-0015 and was never gated). This review deliberately does NOT reproduce the id. Both occurrences predate CYCLE-0003 (present at base `ecd652b6`); **no CYCLE-0003 commit introduced or touched them**. No prior review scanned these files: QA-214 (OPS-0002 gate) and QA-236 (CYCLE-0002 gate) were explicitly scoped to the gated turns' delivered files only, and both found their scoped files clean (correctly). Nothing on record waives the occurrences.
- **Governing source:** the studio's own standard — `REFERENCES/PMU_style/INDEX.md` :24: sharing was "anyone with link" at index time, so "publishing ids here would be equivalent to publishing the content"; `CANON_REGISTRY.md` §7 :214 ("zero Drive file ids/links are stored in this public repository"); `HANDOFFS/CYCLE-0003-EP.md` standing constraint ("DEC-0015 containment: no Drive ids/links in any repo file"); v1 §3.8 private-material law; QA-11 S0 = "secret exposure … Stop pipeline."
- **Consequence:** anyone reading this public repository can reconstruct the folder URL and reach the Owner's Drive folder of copyrighted third-party scanlation copies (folder still link-public at last check, per STATUS/DEC-0015). By the studio's own recorded equivalence this is publication of the content — licensing exposure to the Owner plus exposure of a private-folder pointer. It also falsifies the repo's containment claims (see QA-243).
- **Owner role:** OWNER (ruling required; this is DEC-0015's subject matter, now with two concrete in-repo occurrences and higher urgency). Executing lanes after the ruling: ① (CHANGELOG line), ③ (Asset_Registry line), ④ (record corrections).
- **Recommended action (recommendations only; ⑤ fixes nothing):** (i) **Immediately** (Owner, zero-repo-cost): restrict the Drive folder's link-sharing — DEC-0015 option (a) — which neutralizes the live exposure regardless of repo history. (ii) Rule DEC-0015 (a)/(b) and additionally rule HOW to remediate the in-repo occurrences: forward-redaction commits by the owning lanes (①/③) vs. history rewrite — noting a history rewrite is itself an S0-class action that only the Owner may order, and that the id persists in git history under any forward-only fix. (iii) ⑤ recommends an INCIDENTS.md entry at ①'s cycle close (recurring-risk bar met: the breach survived five review passes because per-turn scan scoping never covered ops/asset files; a standing repo-wide leak scan in every future ⑤ review would close that gap permanently — ⑤ will run one henceforth).
- **Status:** OPEN — **CRITICAL: HALTS the loop pending Owner ruling (Amendment 3 §A3.4).**

### QA-243 — Repo records assert repo-wide "zero Drive ids/links" — false at HEAD given QA-242
- **Severity:** S3 MINOR
- **Confidence:** HIGH
- **Type:** repository (record accuracy)
- **Evidence:** `CANON_REGISTRY.md` §7 :214 "zero image bytes and zero Drive file ids/links are stored in this public repository"; `REFERENCES/PMU_style/INDEX.md` :24 "The folder id and the complete per-file id manifest are on record in the private ops channel" (implying not in-repo); `HANDOFFS/CYCLE-0003-EP.md` standing-constraint line asserting containment as in force. All three are contradicted by the QA-242 occurrences. (The PMU INDEX's own file-scoped sentence — "No raw Drive file ids or share links appear in this public file" — remains TRUE.)
- **Governing source:** Repository law (records must be true); QA-242.
- **Consequence:** future departments relying on the registry's containment claim would repeat the scoping blind spot.
- **Owner role:** ④ (registry/PMU INDEX wording) and ① (plan-language) — AFTER the QA-242 ruling, since the truthful wording depends on the chosen remediation.
- **Recommended action:** on the first authorized pass after the Owner rules QA-242, re-scope the claims to whatever is then true (e.g., "…stored in this library's files; two legacy occurrences elsewhere remediated per DEC-0015 ruling <id>").
- **Status:** OPEN (blocked on QA-242 ruling).

### QA-244 — ② investigation DRAFT: three quote-convention/precision nits (zero semantic impact)
- **Severity:** S4 POLISH
- **Confidence:** HIGH
- **Type:** repository (record convention)
- **Evidence:** (1) E2 and E4 quote complete dialogue sentences byte-exactly but trim the surrounding narration of their long source lines without the bracketed ellipsis the table header promises ("bracketed ellipses mark trims") — e.g., Ch.1:161 continues "…Ha-eun turned a page of the folio…" after the quoted utterance. (2) §0's Q-19 quotation drops the row's trailing "→ REVIEWS/CYCLE-0002_GATE-REPO.md" pointer unmarked. (3) The census sentence "The word 'male' occurs in exactly one primary source (E13)" is literally falsifiable: story_bible:101 contains "male" inside a PMU reference-thumbnail descriptor ("vbu641zd (male close-up)") — unrelated to Im, so the intended claim (no other surface genders Im male) is TRUE, but the sentence as written is absolute.
- **Governing source:** the DRAFT's own stated conventions; primary sources at base `35f09648`.
- **Consequence:** negligible — a future byte-checker loses seconds; the Owner's ruling basis is unaffected (every quoted string IS byte-exact as a substring at its cited line).
- **Owner role:** ② (next touch of the DRAFT, e.g., when the Owner rules Q-19).
- **Recommended action:** add trailing "[…]" to E2/E4/§0 and scope the census sentence to Im-gendering surfaces. Ride-along; no dedicated turn.
- **Status:** OPEN (queued).

### QA-245 — A1.4's letter (every department updates STATUS+CHANGELOG each turn) vs the established conductor ops-lease practice; ②/④ CHANGELOG entries pending at ① close
- **Severity:** S4 POLISH
- **Confidence:** HIGH
- **Type:** build/process (handbook debt)
- **Evidence:** ② and ④ made no STATUS/CHANGELOG writes this cycle (both declared it; ①'s lease). ① recorded turn completions in STATUS (`04f08e82`, `21971bd4`), but CHANGELOG carries no CYCLE-0003 ②/④ turn entries yet — they sit on ①'s declared close-list (STATUS at HEAD). The practice is precedented and was accepted by prior gates as compliant-by-order, but Amendment 1 §A1.4 item 4 was never amended to describe it.
- **Governing source:** Handbook A1.4; OPS-0002/CYCLE-0002 precedent; STATUS close-list.
- **Consequence:** if ①'s close skipped the entries, cycle history would be incomplete; and each new department reads an A1.4 that does not match practice.
- **Owner role:** ① (write the entries at cycle close — already planned; queue a one-line A1.4 clarification for the next authorized Handbook touch).
- **Recommended action:** as above; ⑤ will verify the entries at the next cycle review.
- **Status:** OPEN (watch item).

### QA-246 — Handbook subtitle/version-note still "Amendments 1–2" though Amendment 3 is binding (①-lane; flag only)
- **Severity:** S4 POLISH
- **Confidence:** HIGH
- **Type:** repository (stale header)
- **Evidence:** `00_OPERATING_HANDBOOK.md` :2 "## v2.1 — Five-Department Studio Model (Amendments 1–2 + retained v1 body)"; :4 version note "**Amendments 1 and 2 below are binding…**". Both predate Amendment 3 and were correctly NOT touched by ②/④ (out of lane; ④ flagged it, deviation 7).
- **Governing source:** the Handbook's own Amendment 3.
- **Consequence:** cosmetic; a cold reader could briefly under-count the binding amendments.
- **Owner role:** ① (already on ①'s close-list per STATUS).
- **Recommended action:** mechanical subtitle/v-note fix "1–2" → "1–3" at ①'s cycle close.
- **Status:** ACKNOWLEDGED (queued with ①).

### QA-247 — Acknowledged ④-lane ride-alongs, correctly left untouched this cycle (flag only)
- **Severity:** S4 POLISH
- **Confidence:** HIGH
- **Type:** repository
- **Evidence:** (1) `CANON_REGISTRY.md` §1 Cha "Identity" row (:53) quotes the salts-broth sentence without the story_bible "Cast" pointer (outside QA-239's three named cells; declared in note 6 + deviation 3). (2) `REFERENCES/PMU_style/INDEX.md` §C (:105–106) still says "28 strips"/"the 28 rows" (QA-218's fix targeted §A; echo declared, deviation 5). (3) `CANON_REGISTRY.md` §7 (:214) "28 of them integrity-verified and visually reviewed" — literally true as a file count; framing echo declared, deviation 6. ⑤ concurs with ④'s judgment on all three: edit discipline beat completeness here; none is misleading in context.
- **Governing source:** QA-218/QA-239 scopes; ④'s declared deviations.
- **Consequence:** negligible.
- **Owner role:** ④ (next authorized registry/INDEX pass).
- **Recommended action:** fold all three into the next ④ mechanical pass. §C echo: ⑤ judges it worth taking then (it repeats the corrected count in headline form); §7 echo: optional.
- **Status:** ACKNOWLEDGED (queued).

---

## (g) Verdict block

- **Checklist results:** (a) chain/attribution CLEAN · (b) ① governance VERIFIED · (c) ② turn VERIFIED · (d) ④ turn VERIFIED · (e) cross-cutting CLEAN except QA-242 · (f) ledger hygiene CLEAN with flags.
- **Findings by severity:** S0 — 1 (QA-242) · S1 — 0 · S2 — 0 · S3 — 1 (QA-243) · S4 — 4 (QA-244, QA-245, QA-246, QA-247). All HIGH confidence.
- **Verdict: PASS-WITH-FINDINGS** — every one of the seven CYCLE-0003 commits verifies clean at the byte level: in-lane, night-legal, records-only, label-disciplined, truthfully manifested. No defect in this cycle's work rises above S4.
- **CRITICAL findings: YES** — QA-242 (S0). **Per Amendment 3 §A3.4 the loop HALTS pending an Owner ruling.** Note the deliberate split: the verdict grades the cycle's commits (which are sound and are NOT returned to ②/④); the CRITICAL finding is a pre-existing repo-state exposure that this review's mandated cycle-wide scan surfaced for the first time. Under §A3.4 nothing returns to any department unless and until the Owner rules; the ruling requested is DEC-0015 (a)/(b) plus the in-repo remediation path described in QA-242.
- **QA ledger:** ends at **QA-247**.

## Summary — recommended next steps for ① / Owner

1. **① cycle-close report must lead with QA-242** (S0 CRITICAL → loop HALTED for Owner ruling): put DEC-0015 in front of the Owner with the two occurrences (Asset_Registry:67, CHANGELOG:89), the immediate zero-cost mitigation (restrict folder link-sharing NOW), the repo-visibility question, and the forward-redaction-vs-history-rewrite choice for the in-repo occurrences. Recommend an INCIDENTS.md entry (scan-scoping gap) at close.
2. Complete the close-list already in STATUS: CHANGELOG entries for ②/④ turns + this review (QA-245); TASK-0023 → delivered/verified-by-this-review; TASK-0024 → delivered, awaiting Q-19 ruling; QA-240 → RESOLVED (verified here); Handbook subtitle fix (QA-246).
3. Owner queue otherwise unchanged (12 pending, Q-19 options report ready — the investigation DRAFT is verified byte-exact and decision-ready).
4. QA-243 rides on the QA-242 ruling; QA-244/QA-247 ride along on ②'s/④'s next authorized touches.

*⑤ Quality Assurance · CYCLE-0003 full-cycle review (first under Amendment 3) · base `ecd652b6…` → HEAD `21971bd4…` · this review touches only this file.*

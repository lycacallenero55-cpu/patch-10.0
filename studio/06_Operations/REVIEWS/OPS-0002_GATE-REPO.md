# QA Review — OPS-0002 GATE(④)

- **Date:** 2026-07-19 · **Author:** ⑤ Quality Assurance · **Task ID:** OPS-0002 (Owner-priority PMU reference import — gate review of ④'s turn, per DEC-0013)
- **Scope:** ONLY ④'s OPS-0002 turn — the three commits descending from base `ec4853db5047806fb3de751a6369dc576dfe725b`: `3e88cfc371899f907025595d7ecc762ec572c002` (new `studio/07_Repository/REFERENCES/PMU_style/INDEX.md`), `beac8a622513fb9358d7c07299a849cbac605900` (`studio/07_Repository/CANON_REGISTRY.md` §7 insertion), `3d58a9656f87ec0ae55c0e709d8d201c0c4c3f82` (new `studio/06_Operations/HANDOFFS/OPS-0002-REPO.md`, = HEAD at gate time). Verified: commit chain and hygiene, lane compliance, the pure-insertion claim (byte-level blob-sha restoration), INDEX content quality and its reconciliation against the live Drive manifest, Drive-id/link non-leakage, a 3-strip independent spot audit re-downloaded from Drive, handoff completeness, and Owner-protocol deviation handling. This gate evaluates **execution quality only**: ④'s licensing deviation was endorsed by ① before this gate, and the licensing/visibility ruling itself remains queued for the Owner — nothing in this review decides it. This review makes no edit to any ④ file or any file outside ⑤'s own lane (`REVIEWS/`); per the work order, ① owns the follow-on ops bookkeeping for OPS-0002, so the absence of STUDIO_STATUS/CHANGELOG/TASK_QUEUE updates in ④'s commits is compliant-by-order, not an omission.
- **Numbering note:** this review's findings start at **QA-210** because `CYCLE-0002_GATE-LORE.md` already used QA-201 through QA-209 (the conductor's running pointer of "last used = QA-202" is stale; flagged to ① in the gate report, not a ④ defect).
- **Method note:** every claim below was re-derived from primary sources — commit list and per-commit file stats via `github__list_commits`/`github__get_commit`; exact file bytes via GitHub's raw content API at pinned SHAs; git blob SHA-1s recomputed locally as `sha1("blob <len>\0" + bytes)`; the spot-audit strips re-downloaded from Drive by ⑤ (read-only) and re-hashed with `sha256sum`; the source folder's live permission list read via the Drive API. ④'s own working artifacts (sandbox manifest/hash files) were used only as a lookup aid and cross-check, never as evidence.

## Findings

### QA-210 — Commit chain and message hygiene confirmed
- **Severity:** N/A (positive confirmation, not a defect)
- **Confidence:** HIGH
- **Type:** repository
- **Evidence:** `github__list_commits` on `main` at gate time returns, newest-first: `3d58a965…` → `beac8a62…` → `3e88cfc3…` → `ec4853db…` (④'s declared base, ①'s block-lift commit) → older history. Exactly **three** commits exist between the declared base and HEAD — no more, no fewer, and nothing interleaved (base authored 07:42:57Z; ④'s three at 08:04:41Z / 08:04:57Z / 08:05:14Z, strictly increasing and matching the claimed 1→2→3 order: INDEX, then registry, then handoff). All three messages carry the `[④-REPO] ` prefix and are descriptive to the house standard — each states what was added, and the first two state the deviation substance (zero image bytes, zero Drive ids/links, licensing grounds) directly in the message rather than hiding it. HEAD at gate time **is** ④'s third commit; no post-turn commit intervened before this gate ran.
- **Governing source:** DEC-0013 / Amendment 2 §A2.3 (gate mechanics); Amendment 1 §A1.4 (commit hygiene); ①'s conductor record of the turn base.
- **Consequence:** None.
- **Owner role:** N/A.
- **Recommended action:** None required.
- **Status:** RESOLVED (verified this gate).

### QA-211 — Lane compliance confirmed: three commits, one in-scope file each, zero binaries
- **Severity:** N/A (positive confirmation)
- **Confidence:** HIGH
- **Type:** repository
- **Evidence:** `github__get_commit` per-commit changed-file lists: `3e88cfc3…` touches ONLY `studio/07_Repository/REFERENCES/PMU_style/INDEX.md` (added, +108); `beac8a62…` touches ONLY `studio/07_Repository/CANON_REGISTRY.md` (modified, +10/−0); `3d58a965…` touches ONLY `studio/06_Operations/HANDOFFS/OPS-0002-REPO.md` (added, +51). That is exactly the three-file manifest ④ declared, and nothing else. **Zero image or binary files appear anywhere in any of the three commits** — the deviation (no image bytes in the public repo) was actually honored, not just declared. A directory listing of `studio/07_Repository/REFERENCES/` at HEAD contains only `PMU_style/`, and `PMU_style/` contains only `INDEX.md`. None of the ops docs (`STUDIO_STATUS.md`, `CHANGELOG.md`, `TASK_QUEUE.md`, `DECISION_LOG.md`, `OPEN_QUESTIONS.md`) and nothing under `studio/02_Art/`, `manuscript/`, or `readers/` was touched. **Verdict: COMPLIANT.**
- **Governing source:** Amendment 1 §A1.2 (lane ownership); the OPS-0002 work order's lane carve-out (① owns follow-on bookkeeping).
- **Consequence:** None.
- **Owner role:** N/A.
- **Recommended action:** None required.
- **Status:** RESOLVED (verified this gate).

### QA-212 — CANON_REGISTRY pure-insertion claim verified at byte level (blob-sha restoration)
- **Severity:** N/A (positive confirmation)
- **Confidence:** HIGH
- **Type:** repository
- **Evidence:** Fetched exact bytes of `CANON_REGISTRY.md` at base `ec4853db…` (35,996 bytes) and at HEAD `3d58a965…` (38,417 bytes). The base copy's recomputed git blob SHA-1 is `9af95b76a829038d2c36f9086da39b8c5e19f9dc` — **identical to the pre-turn blob sha on record.** Byte-level common-prefix/common-suffix analysis shows the two versions differ by exactly **one contiguous 2,421-byte insertion** (prefix 34,139 bytes and suffix 1,857 bytes byte-identical; 35,996 + 2,421 = 38,417). Deleting the inserted span **byte-restores the prior file exactly**: the reconstruction hashes back to `9af95b76…`. The commit's own stats corroborate (+10/−0 — additions only). The inserted span is §7 "Reference Libraries": a records-only preamble ("A reference library is never canon, never a drawing source, and never overrides a LOCKED entry; this registry records that such a library exists and where its index lives, nothing more") plus one PMU table row whose constraints column is explicitly "(recorded, not ruled, by ④)", marks the entry `REFERENCE-ONLY — style/mood reference exclusively`, names `studio/02_Art/Art_Direction.md` (DEC-0003 flat-2D PMU, gpt-image-2; DEC-0004 strip model v5) as **remaining MASTER**, prohibits panel copying/tracing/direct derivation of compositions, and records the in-repo-vs-Drive question as "an open Owner ruling — queued … not decided here." HEAD blob SHA-1s for the record: registry `20612b3cf8d73ce5827be9dda325b159bcd32bab`; INDEX `349c36f104db0668137beb83d09a50765805f37d` (matches GitHub's own blob listing for the file, confirming download integrity); handoff `25f58005512094b86beb5770ccf7d49c14bb54e2`.
- **Governing source:** ④'s pure-insertion claim (commit message + handoff fact #5); Handbook §21 (registries record, never adjudicate).
- **Consequence:** None — every pre-existing registry line is byte-identical; no entry, status, pointer, or the QA cross-cutting notes block was modified.
- **Owner role:** N/A.
- **Recommended action:** None required.
- **Status:** RESOLVED (verified this gate).

### QA-213 — INDEX.md quality verified; every checkable inventory claim reconciles against the live Drive manifest
- **Severity:** N/A (positive confirmation)
- **Confidence:** HIGH
- **Type:** repository
- **Evidence:** (a) **Banner:** the REFERENCE-ONLY banner sits at the top of the file, above all content, and is correctly subordinated — Art_Direction.md's locked style law (DEC-0003/DEC-0004) is named MASTER; "No panel copying. No tracing. No direct derivation of compositions"; "Nothing in this library is canon." (b) **Licensing note:** present as its own top-level section; states the source is scanlation captures of the licensed *Pick Me Up: Infinite Gacha* (watermarks visible on the pages — independently confirmed, see QA-215), that the repo is public, and derives both deviations (zero bytes; ids withheld) from that; the in-repo-copies path is phrased as a recommend-only note with "④ did not take any of those actions." (c) **§A shortlist:** exactly 28 rows (4 × 7 chapters), each with a 64-hex SHA-256, a one-line visual description, and style elements. (d) **§B inventory reconciliation** — checked item-for-item against the Drive listing: 7 chapter subfolders; per-chapter strip lists match exactly, including the fiddly cases (ch.51 = 14 files with 004/006/009 split `_p1`/`_p2` and `_p2` remainders of ~1 KB–119 KB — actual 1,016 B / 1,182 B / 121,732 B; ch.144 = 11 files, `005` genuinely absent; ch.142's `001` correctly identified as a site-banner capture); 85 story strips total; 260 non-story chrome files (= 232 images + 7 css + 21 script/beacon blobs, exact); 5 top-level files with sizes accurate to the stated precision (282/226 KB HTML; 6.3/13.6/11.4 MB recordings); the ch.143 anomaly (HTML shell with **no** `_files` image folder) is real — no ch.143 subfolder exists in the listing — and is correctly flagged record-only to ①. Total item count reconciles: 350 files + 7 subfolders = **357 items** as stated. (e) **Curation rationale:** present (§C) with honest "Imported into the repo: 0" framing and a register-coverage argument that matches the actual shortlist composition.
- **Governing source:** the OPS-0002 work order (index requirements); the live Drive folder listing (⑤'s own read at gate time via file/metadata reads); ④'s manifest cross-checked as secondary.
- **Consequence:** None — the index is accurate enough to serve as ③'s working surface without the images in-repo.
- **Owner role:** N/A.
- **Recommended action:** None required.
- **Status:** RESOLVED (verified this gate).

### QA-214 — Zero Drive-id/link leakage in all three delivered files
- **Severity:** N/A (positive confirmation)
- **Confidence:** HIGH
- **Type:** repository
- **Evidence:** Scanned the exact HEAD bytes of `INDEX.md`, `CANON_REGISTRY.md`, and `OPS-0002-REPO.md` for: the source folder's id prefix (zero hits in all three), any `drive.google.com` string (zero hits), and any Drive-id-shaped token (all `[A-Za-z0-9_-]{25,}` matches extracted and reviewed one-by-one — every match is a SHA-256 table value, a git commit SHA, or a hyphenated filename; no base64url-style Drive id shapes exist in any of the three files). Files are cited by exact name only, matching the declared withholding policy; the id manifest lives in the private ops channel as stated. (This review likewise contains no Drive ids or links.)
- **Governing source:** ④'s declared second deviation (handoff fact #3); the licensing note's own policy.
- **Consequence:** None — the public repo neither contains the images nor points at them.
- **Owner role:** N/A.
- **Recommended action:** None required.
- **Status:** RESOLVED (verified this gate).

### QA-215 — Spot audit (3 of 28): independent Drive re-downloads hash-match the INDEX exactly; descriptions honest; licensing premise corroborated live
- **Severity:** N/A (positive confirmation)
- **Confidence:** HIGH
- **Type:** repository
- **Evidence:** ⑤ selected three §A rows across three chapters — **PMU-086-B** (ch.86/`006.webp`), **PMU-103-D** (ch.103/`011.webp`), **PMU-189-B** (ch.189/`005.webp`) — resolved their file ids from the private manifest by exact name, re-downloaded each from Drive (read-only), and recomputed SHA-256 with `sha256sum` on the received bytes: all three reproduce the INDEX table values **exactly** (`d463cb0e…`, `0687596b…`, `c9136565…`; sizes also match the manifest byte-for-byte). Visual honesty check on PMU-189-B (sliced and inspected segment-by-segment): the strip is precisely as described — an arena beat giving way to a black-page interior monologue of floating caption boxes ("I can't get stronger… the infinite loop of everyday life… which is the real one?") and a lone spearman amid **drifting unanswered letters** ("No matter how many letters I write, the memories I lost will not come back") — the INDEX's "time-loop doubts as floating captions, drifting unanswered letters" one-liner and "the library's strongest quiet-beat exemplar" note are accurate, not embellished. Supporting depth: all **28** reviewed strips' local working copies in ④'s sandbox re-hash to the INDEX values (28/28) and match manifest sizes (28/28) — recorded as corroboration only; the three Drive re-downloads above are the independent evidence. Licensing premise independently corroborated at gate time: the Asura Scans watermark is visible on the audited page itself, and the source folder's live permission list shows exactly one non-owner grant — `type: anyone` (link), `role: reader`, discovery off — i.e., the folder **is** link-public as ④'s deviation reasoning assumed. Drive-side read-only conduct corroborated by sample: audited file and subfolder metadata show modified/created times of 2026-07-18 (pre-dating ④'s 2026-07-19 turn); no evidence of any Drive write was found (exhaustive proof of absence across all 350 files is not feasible from artifacts and was not attempted).
- **Governing source:** handoff fact #4 (reproducibility claim, "re-downloading any listed file and hashing it should reproduce the table value" — confirmed 3/3); the work order's READ-ONLY Drive constraint.
- **Consequence:** None — provenance hashes are real, reproducible, and honestly described.
- **Owner role:** N/A.
- **Recommended action:** None required.
- **Status:** RESOLVED (verified this gate).

### QA-216 — Handoff completeness confirmed (③ brief + ⑤ gate manifest + honest deviations)
- **Severity:** N/A (positive confirmation)
- **Confidence:** HIGH
- **Type:** repository
- **Evidence:** `OPS-0002-REPO.md` is addressed to ③ Visual Production as primary addressee with: the library's exact location, what it is (7 chapters / 85 strips / 28 reviewed), where the images actually live (Drive; request access from the Owner or ①), the REFERENCE-ONLY constraints **quoted verbatim** from the order with Art_Direction.md named master, and practical pointers into the shortlist (registers, and the card-UI refs relevant to the undesigned registry-cards device — correctly tagged "as *sensibility* reference only"). The ⑤ gate section lists the exact three commits/files (matches QA-211's independently derived lists), states the base commit, and declares both deviations plainly — including the precise, honest framing that the order's binary-integrity blob-sha protocol is **NOT RUN / N-A** because no binary was ever committed (there is no test file to remove), rather than claiming it "passed." Open items for ①/Owner are queued at the bottom, explicitly "queued, not decided by ④."
- **Governing source:** DEC-0013 (gate manifest requirement); TURN_HANDOFF_TEMPLATE.md conventions.
- **Consequence:** None — ③ can act on this handoff without reading ④'s private report.
- **Owner role:** N/A.
- **Recommended action:** None required.
- **Status:** RESOLVED (verified this gate).

### QA-217 — Deviation handling followed Owner-protocol: queued, not decided; declared prominently, not buried
- **Severity:** N/A (positive confirmation)
- **Confidence:** HIGH
- **Type:** process
- **Evidence:** The licensing/visibility ruling is left genuinely open in every artifact: INDEX.md's licensing note marks the in-repo path "recommend-only … ④ did not take any of those actions"; CANON_REGISTRY §7 records it as "an open Owner ruling — queued in `HANDOFFS/OPS-0002-REPO.md`, not decided here"; the handoff's final section is titled "Open items left for ① / Owner (queued, not decided by ④)." Prominence: the deviation is stated in the **first line of substance** of all three commit messages, in the INDEX's top-of-file licensing section (immediately after the banner), in the registry row itself, and in a dedicated handoff facts list — nowhere is it buried in a footnote. ④ also did not perform any surrogate action that would moot the ruling (no sharing change, no repo-visibility change, no id publication). ①'s endorsement of the deviation is on the conductor record; this gate verified execution only, per its charge.
- **Governing source:** Owner-protocol (UNDECIDED items queued, never resolved by departments); DEC-0013 gate scope.
- **Consequence:** None — the Owner receives an intact decision with full context.
- **Owner role:** **The queued ruling is real and waiting:** (a) keep the library Drive-resident permanently, or (b) restrict folder sharing + make the repo private + issue a fresh import order. Ancillary fact for that ruling, from this gate: the folder's sharing is still "anyone with link" as of gate time.
- **Recommended action:** ① should carry the queued ruling (and the ch.143 gap note) to the Owner; no action for ④.
- **Status:** RESOLVED (process verified this gate; the ruling itself remains OPEN with the Owner).

### QA-218 — §A's "28 reviewed reference strips" includes one self-disavowed capture artifact; effective reference shortlist is 27
- **Severity:** S4 POLISH
- **Confidence:** HIGH
- **Type:** repository
- **Evidence:** Shortlist row **PMU-142-A** (ch.142/`001.webp`) is, per its own honest description, a "wide site-header banner from the page capture (mostly black web chrome) — not a story strip; indexed for provenance completeness only," with style elements "N/A — capture artifact, not an art reference." The row is truthful and its inclusion is defensible (it documents that ch.142's `001` is not usable, which saves ③ a wasted open), but the section heading "Curated shortlist — 28 reviewed reference strips" and the review-count claims ("visually reviewed 28 of the 85 story-page strips", "4 per chapter") count it as a reference strip. The *reference-usable* shortlist is 27; ch.142 effectively contributed 3 usable references, not 4.
- **Governing source:** INDEX.md §A/§C internal consistency.
- **Consequence:** Negligible — the row itself prevents any misuse, and ③'s practical pointer list in the handoff does not recommend 142-A. Purely a heading/count precision matter.
- **Owner role:** N/A.
- **Recommended action:** On any future ④ touch of INDEX.md (no dedicated turn warranted): reword §A's heading or add a half-line, e.g. "28 reviewed (27 usable as reference; 142-A is a capture artifact kept for provenance)." Non-blocking.
- **Status:** OPEN (queued, non-blocking).

### QA-219 — §B.2's "~180 hash-named" thumbnail count is loose against the raw file count
- **Severity:** S4 POLISH
- **Confidence:** HIGH
- **Type:** repository
- **Evidence:** §B.2 characterizes the recommendation-thumbnail group as "~180 hash-named `.webp`/`.jpeg`/`.png`/`.gif` files, 2–1,039 KB". ⑤'s count from the Drive listing: **211** such files raw (203 in strict `id.hash.ext` form + 8 odd-named), of which **172 are distinct names** (the same thumbnails recur across the 7 folder captures) — so "~180" is defensible as a distinct-asset estimate but reads as a file count and is ~15% low on that reading. The size range checks out (min ~1.8 KB, max ~1,039 KiB), and — decisively — the **exact** enclosing totals are all correct (260 non-story files; 345 subfolder files; 5 top-level; 85 strips; 357 items), so the imprecision is contained to one explicitly-approximate descriptor inside a group ④ itself marked "individually meaningless … Not recommended as style reference."
- **Governing source:** INDEX.md §B.2; the live Drive listing.
- **Consequence:** Negligible — no navigation or reference decision depends on this sub-count.
- **Owner role:** N/A.
- **Recommended action:** On any future ④ touch of INDEX.md: either drop the number ("hash-named thumbnails") or state both figures ("211 files, ~172 distinct"). Non-blocking.
- **Status:** OPEN (queued, non-blocking).

## Severity reference (verbatim from Handbook §8.5/§21)
- `S0 CRITICAL` — secret exposure, repository corruption, destructive history rewrite, or severe safety issue. Stop pipeline.
- `S1 BLOCKER` — canon contradiction, broken locked asset, failed production gate, or unusable output. No downstream work.
- `S2 MAJOR` — continuity or production defect that materially harms story/readability/consistency.
- `S3 MINOR` — localized issue with low downstream impact.
- `S4 POLISH` — optional clarity or style improvement.

## Confidence reference
`HIGH` / `MEDIUM` / `LOW`. Low-confidence findings must not trigger semantic edits without further review.

## Protected zones (do not silently fix — per Handbook §21)
Canon bibles · prose and dialogue · approved adaptation scripts · locked asset facts · creator approvals · private/sealed information. This review made no edit to any file in these zones, or to any ④ file, or to any file outside ⑤'s own lane (`REVIEWS/`). In keeping with the turn's own withholding policy, this review reproduces no Drive ids or links.

## Summary

- **Findings by severity:** S0 — 0 · S1 — 0 · S2 — 0 · S3 — 0 · S4 — 2 (QA-218, QA-219) · N/A (positive confirmations) — 8 (QA-210 through QA-217).
- **Findings by confidence:** HIGH — 10 (all findings). One disclosed partial-scope note inside QA-215: 3 of the 28 shortlist hashes were independently reproduced from Drive re-downloads (the audit's required sample); the remaining 25 were corroborated against ④'s sandbox working copies (28/28 match) but not re-downloaded from Drive this gate — corroborated, not independently reproduced. One disclosed limit: "no Drive writes" is corroborated by sampled metadata timestamps and the artifact record, not exhaustively provable.
- **Lane-compliance verdict:** all three commits — **COMPLIANT.** One file each, all inside ④'s lane (or `HANDOFFS/` carve-out); `[④-REPO] ` prefixes; descriptive messages; zero binaries; zero ops-doc touches (①'s bookkeeping carve-out honored).
- **Blob-sha verification result:** base `CANON_REGISTRY.md` recomputes to `9af95b76a829038d2c36f9086da39b8c5e19f9dc` (35,996 B) exactly; HEAD version = prior bytes + one contiguous 2,421 B insertion (§7); removal of the insertion byte-restores the prior blob sha. **Pure insertion: TRUE.**
- **Recommended next steps for ① / Owner:** (1) No blocking action; ③ may consume the library per the handoff, under the INDEX banner. (2) Carry the queued Owner ruling (Drive-resident permanently vs. restrict-sharing + private-repo + fresh import order) — noting the folder is still link-public as of gate time. (3) Record the ch.143 images-missing gap alongside TASK-0012. (4) Correct the conductor's QA-number pointer (last used is now QA-219, not QA-202). (5) QA-218/QA-219 ride along on any future ④ INDEX touch; no dedicated turn.

---

## VERDICT

# PASS

**Rationale:** No finding rises above S4 POLISH. The commit chain is exactly as declared (three `[④-REPO] ` commits, in order, base-to-HEAD, nothing else). Lane compliance is fully confirmed with the deviation *actually honored in the tree* — zero image/binary bytes anywhere, `REFERENCES/PMU_style/` holding only `INDEX.md`, and zero Drive ids/links in any delivered file (token-level scan). The pure-insertion claim is verified at the strongest available standard: the pre-turn registry blob sha recomputes exactly, and deleting the single contiguous inserted §7 block byte-restores it. The INDEX is accurate where it is checkable — every per-chapter file list, count, size, and anomaly (ch.51 splits, ch.144's missing `005`, ch.142's banner artifact, the ch.143 HTML-without-images gap) reconciles against the live Drive listing, and the 357-item arithmetic is exact. The spot audit reproduced 3 of 3 sampled SHA-256 values from fresh Drive downloads and found the sampled visual description honest to the pixel content; the licensing premise (scanlation watermark; link-public folder) was independently confirmed live. The handoff equips ③ and ⑤ fully and declares both deviations plainly, including the honest NOT-RUN framing of the binary-integrity protocol. The Owner ruling is genuinely queued, prominently, everywhere. The two S4 findings (a self-disavowed capture artifact counted inside "28 reviewed reference strips"; a loose "~180" sub-count) are cosmetic, self-limiting, and queued for a future INDEX touch.

**Non-blocking findings queued:** QA-218 (S4 — shortlist heading counts one non-reference capture artifact; effective reference set is 27) · QA-219 (S4 — "~180" thumbnail sub-count vs. 211 raw / 172 distinct).

**④ is cleared; OPS-0002's repo deliverables stand as committed. The conductor may proceed — the Owner ruling on library residency remains the open item.**

# Turn Handoff — OPS-0002-④ (Repository & Canon Management, Owner-priority operations turn)

**From:** ④ Repository & Canon Management
**To:** ③ Visual Production (primary addressee) · ⑤ QA (gate section at bottom, per DEC-0013) · ① Executive Producer (dispatching conductor)
**Date:** 2026-07-19 · **Type:** OWNER-PRIORITY work order (PMU reference library import) · **Base commit this turn started from:** `ec4853db5047806fb3de751a6369dc576dfe725b` (verified as HEAD via `github__list_commits` before any write)

---

## To ③ Visual Production — what you are receiving

**A PMU style reference library now exists at `studio/07_Repository/REFERENCES/PMU_style/` — but it is Drive-resident: the repo holds the index, not the images.**

1. **What it is.** An indexed reference corpus built from the Owner's private Drive folder "pick me up": 7 captured chapters of the *Pick Me Up: Infinite Gacha* webtoon (chapters 51, 85, 86, 103, 142, 144, 189) totaling **85 story-page strips**, of which ④ downloaded, integrity-verified, and visually reviewed **28** (4 per chapter, spread across each chapter's range) and wrote per-strip descriptions and style notes.
2. **Where it lives.** The images stay in the Owner's Drive folder (request the link from the Owner or ①). The in-repo deliverable is the index: **`studio/07_Repository/REFERENCES/PMU_style/INDEX.md`** — start with its §A shortlist table (28 reviewed strips with one-line descriptions and style elements), then §B for the full named inventory.
3. **In-repo vs Drive-resident count: 0 images in-repo · 85 story strips (of 357 total folder items) Drive-resident.** Zero image bytes were committed, deliberately. The source pages are third-party scanlation copies of a licensed commercial series, this repository is public, and committing them would publicly redistribute copyrighted artwork. For the same reason the public INDEX carries **no Drive file ids or share links** (the folder is currently link-public); the id manifest is on record in ①'s private dispatch thread. This is a licensing decision by ④, flagged to ① in the turn report — not a technical failure and not an empty-folder situation.

### The constraints, verbatim from the Owner-priority order

> style/mood reference ONLY — the locked style law in `studio/02_Art/Art_Direction.md` (DEC-0003 flat-2D PMU, gpt-image-2; DEC-0004 strip model v5) remains MASTER; no panel copying, no tracing, no direct derivation of compositions; these images inform mood/palette/line-weight/paneling sensibility only.

The same banner sits at the top of INDEX.md. Treat it as binding whenever the library is open next to production work.

### Practical pointers for your next turn

- The shortlist deliberately spans registers: action spectacle (85/86/144), quiet beats (51-B, 189-B — the black-page introspection strip is the strongest quiet exemplar), environment-forward staging (103-B/C), horror/tragedy lighting (103-A, 142-B/C/D), comedy timing (86-C, 189-A).
- Of likely interest to existing gaps: the series' diegetic **card-UI grammar** (INDEX refs 86-D, 103-D, 142-D, 144-C/D) is directly relevant to the undesigned "registry cards" device (CANON_REGISTRY §2) — as *sensibility* reference only, per the banner.

---

## To ⑤ QA — exact gate manifest for this turn

Everything this turn touched, in order:

| # | Commit | Files |
|---|---|---|
| 1 | `[④-REPO] REFERENCES: establish PMU_style reference library index …` | `studio/07_Repository/REFERENCES/PMU_style/INDEX.md` (new) |
| 2 | `[④-REPO] CANON_REGISTRY: add §7 Reference Libraries …` | `studio/07_Repository/CANON_REGISTRY.md` (single additive section inserted between §6 and the "Cross-cutting notes for ⑤ QA" block; every pre-existing line byte-identical) |
| 3 | `[④-REPO] HANDOFFS: add OPS-0002-REPO …` | `studio/06_Operations/HANDOFFS/OPS-0002-REPO.md` (new — this file) |

Gate-relevant facts, honestly stated:

1. **Lane compliance:** only the three files above were written. STUDIO_STATUS.md, CHANGELOG.md, TASK_QUEUE.md, DECISION_LOG.md, OPEN_QUESTIONS.md, all of `studio/02_Art/`, `manuscript/`, and `readers/` were not touched (the work order excluded them from ④'s lane this turn; ① owns the follow-on bookkeeping). Nothing was LOCKED, retconned, or restructured. No Drive writes of any kind were performed (folder was read-only for ④; verified: only list/metadata/permission reads and downloads).
2. **Deviation to verify, not a hidden one:** the order's steps 3–4 (commit ~30 images + binary-integrity blob-sha test) were **deliberately not executed** on licensing grounds (public repo × scanlation copies of a licensed series × link-public Drive folder). The order's own fallback end-state — fully Drive-resident library, INDEX carries the entries, no image bytes in repo — was delivered instead, with the trigger being licensing rather than binary corruption. The binary-integrity protocol is therefore **NOT RUN / N-A** (no binary was ever committed; there is no test file to remove). Flagged prominently here and in ④'s report to ①.
3. **Second deviation, same root cause:** INDEX.md §B withholds raw Drive file ids/webViewLinks (order step 5 asked for them) because the source folder is shared "anyone with link" and this repo is public — publishing ids would be equivalent to publishing the content. Names are exact, so entries remain locatable; the full id manifest is in ④'s private report to ①.
4. **Verifiable claims:** the 28 SHA-256 hashes in INDEX §A were computed from bytes downloaded via the Drive integration on 2026-07-19 after magic-byte verification (RIFF/WEBP) of every file; re-downloading any listed file and hashing it should reproduce the table value.
5. **CANON_REGISTRY edit shape:** pure insertion of one new section (§7, one table row plus preamble). No existing entry, status, pointer, or the cross-cutting notes block was modified. A diff against parent commit should show only added lines.

## Open items left for ① / Owner (queued, not decided by ④)

- Whether to (a) keep the library Drive-resident permanently, or (b) restrict the Drive folder's sharing + make the repo private and re-issue a fresh import order for in-repo copies. ④ recommends recording the ruling in DECISION_LOG either way (recommend-only).
- TASK-0012 relevance: the folder contains a **chapter-143 HTML page capture but no ch.143 page images** (no `_files` folder for 143). Reported to ① in the turn report; no action taken.

# Canon Review — TASK-0042 Day-Label + Countdown Reconciliation Census DRAFT (TASK-0043)

**Reviewer:** Canon Review Agent (DEPT-024) · **Date:** 2026-07-20 · **Work Order:** TASK-0043 (CYCLE-0008, EP dispatch).
**Subject:** `studio/06_Operations/WORK_IN_PROGRESS/day_label_reconciliation_DRAFT.md`, delivered by ② Lore at commit `c7915a86746e9ef56ad528e299cc148460e37169` (blob `a9cf936f2004c7a3b47d65cdece458500a437d17`, +300 lines, single new file, parent `94f1ca21b3fa09a343bacc3d2d1d5d3332a73931`).
**Trees examined (fresh clone; every check recomputed from repository bytes, nothing trusted from the census's prose):** HEAD at sync = `26f86708e4d4c941b373aad95451135cb111f914` (= the TASK-0043 dispatch base — no post-dispatch drift) · census commit `c7915a86…` · census base `94f1ca21…`. Between `94f1ca21…` and HEAD only three ops ledgers moved (`CHANGELOG.md`, `STUDIO_STATUS.md`, `TASK_QUEUE.md`) plus the census itself — every bearing surface is byte-identical to the census's pinned base; base-blob reads were used for the three moved ledgers.
**This file is the ONLY write of this review (review-records lane; no ledger edits — EP records the verdict). It decides nothing, resolves nothing, and re-flags nothing closed. CR-005 and CT-008 remain OPEN at their recorded severities; the ruling on them remains the Owner's alone.**

---

## VERDICT: **PASS-WITH-FINDINGS** (zero S0/S1/S2/S3 · two S4, both non-blocking precision items)

The census is **safe to rule on.** Every load-bearing claim was independently recomputed from repository bytes and verified, including the claim the Owner will lean on hardest: **restricted to LOCKED + PUBLISHED surfaces, exactly one self-consistent timeline survives (Chain A), and the census's statement of what is "mechanically forced" is true as stated and properly conditioned.** The two findings are census-precision items (three missed propagation rows in the §3.7 map; three wording/attribution nits); neither touches the arithmetic, the options, the fair-play audit, or the neutrality posture.

---

## Check 1 — Census accuracy, forward direction: **PASS**

Spot-verified **40+ of the S1–S87 evidence rows, covering every surface class**, each against the exact blob the census pins (all 23 blob SHAs in census §2 recomputed via `git ls-tree` at `94f1ca21…` — 23/23 exact):

- **Prologue (`a8f08943`):** S1–S8 — all 8 rows byte-exact (:4 six hours; :8/:12 well two-days; :18 pack nine days; :16/:36 tells; :30–:36 tonight/hour; :52; :66/:68 11:58/11:59; :84 banner).
- **Ch.1 (`1623d610`):** S9–S24 — all 16 rows byte-exact, including every CT-008-relevant line (:65, :105, :195, :197, :205, :207, :209, :211, :213, :215) with quotes and bearings accurate.
- **story_bible (`c444bd97`):** S25–S28 exact — including the load-bearing S28 absence claim: the Ch.2 drafting-log entry at :100 carries **no day number** (verified; this is the entry the outline cites for "Day −3").
- **MPB (`47665222`):** S29–S34 exact, including the §5–6 constants line :41–:42 (`present = Day −3 → Ch.2 Day −2/−1 → Ch.3 Day 0 (festival night, patch lands EARLY…)`), :21 mid-festival, :60 precedence, and the fair-play law at :11 the options section cites.
- **CANON_REGISTRY (`f8da9aa2`):** S35–S38c exact (:186, :187, :188, :29, :180, :202); the "Day −2/−1"/"Day 0, festival night" labels sit inside the LOCKED (beats) value at :188 — the UNDECIDED qualifier scopes to Q-01/Q-02 specifics only, as the census represents.
- **CONTINUITY_LEDGER (`ffe4fc62`):** S39–S41 exact; the rollover-semantics gap the census notes at S39 is real (the ledger does not define whether the "Day −3 night" label's day opens or closes at that midnight).
- **Published EP.1 script (`3448be33`) + readers (`17bce6ea` / `714dc7a1`):** S42–S56 all exact, including the published endcard S56 (readers p2 :223–:224): "Seventy-two hours. One bag to pack." — confirmed **untied** to any named event.
- **Variance record (`f526a278`):** S57–S60 exact (:48 rooftop 11:58→"Midnight" softening; :49 collapse preserved exactly; :50 final-image omission; :18–:19 doubt-line omission).
- **EP.2 outline (`0dbb13b9`):** S61–S68 exact, including the S62 attribution-gap claim (verified both ways: the outline attributes "Day −3" to a drafting-log entry that carries no day number — independently corroborated by both TASK-0005 reviews).
- **EP.2 script DRAFT (`e2ac6ad0`):** S69–S77 exact; recomputed day-number sweep confirms :16 is the file's **only** "Day −3" token (production header; zero on-panel day numbers), and :18's reader-facing register does tie 72 hours to festival night, as S71 states.
- **Ops/review propagation (S78–S87):** verified at cited lines, including base-blob reads for `TASK_QUEUE.md` :43/:47, `STUDIO_STATUS.md` :27, `CHANGELOG.md` :84/:222. `TASK-0005_CANON.md` :12/:65/:79 confirm the CR renumber history and the ":197 glance" provenance the census's §0 cites. One row imprecision found (S87 — see CR-008).

## Check 2 — Census completeness, reverse direction: **PASS-with-findings**

Independent repo-wide sweep (all tracked `.md` + `.html`) for day-label tokens, countdown words, and clock/festival anchors, every hit read in context and reconciled against the census's S-rows, §3.7 map, and §3.8 non-bearing list:

- **No bearing surface was missed.** Every canon, published, WIP-canon, and variance surface carrying a day label or countdown claim is in the census. The census's verified-absence claims hold: `DECISION_LOG.md` and `00_STUDIO_RULES.md` carry zero relevant tokens (recomputed: 0 hits each); no file titled "Manhwa Production Bible" exists anywhere at the base tree (recomputed); the retired v1 trailer's repo record (`Video_Workflow.md` :42 title-card list) carries no countdown claims (recomputed).
- **Three review-record surfaces carrying swept tokens are absent from the §3.7 propagation map** → **CR-007** (S4). All three are records-about-records, chain-neutral, and change nothing in §§4–7.
- Ops-register "skips" hits elsewhere (`HANDOFFS/OPS-0001-EP.md` :16, `HANDOFFS/TASK-0004-LORE.md` :32 — department/row skips) are not time surfaces; correctly outside the census's scope.

## Check 3 — Arithmetic verification (the heart): **VERIFIED, all four sub-claims**

Recomputed independently from LOCKED + PUBLISHED bytes only, then per-line against Ch.1:

**(a) Chain A is self-consistent and entailed.** All six §4.1 assertions verified as actual locked/published bytes (S32/S33/S37/S77; S36/S39; S25/S27/S30/S36/S38c/S55; S56; S36/S38a/S38b/S39; S32/S37). From "3 days before the Founding Festival" + "ETA collapsed 9→~3" + "patch lands ON festival night, Day 0": festival night ≈ M0+72h; under standard rollover the double-skip night belongs to Day −3, Ch.2's dramatized day is Day −2 (terminal midnight at the −2/−1 boundary), Ch.3 = Day 0. Satisfies every locked and published assertion simultaneously. The census's conditioning ("under standard rollover"; "≈"/"~3" precision) is stated, not smuggled.

**(b) The uniqueness claim is TRUE.** I independently constructed and tested the alternatives rather than trusting §4.2's exhaustive check: (i) midnight-rollover with M0 opening Day −3 → festival night ≈ M0+96h, violating the LOCKED "3 days before" + ETA ~3 + patch-on-festival-night rows; (ii) sunset-to-sunset days → the outline's actual span-usage ("Day −3 morning **through Day −3 midnight**", S63) fails (the terminal midnight falls in the next sunset-day; forcing the full span to one label requires a ~30h day and either festival at Day −1 or a skipped label), and Ch.2 = Day −3/−2 contradicts LOCKED :188 "Day −2/−1"; (iii) dawn-rollover → baseline night and Ch.2's day get different labels, breaking one end or the other; (iv) nights-remaining-inclusive counting → festival **day** lands at Day −1, exactly the far-end breakage §4.2 names. No committed record defines any non-standard convention. **Restricted to locked + published surfaces there is no conflict, and the committed chain −3 (baseline night) → −2 (Ch.2) /−1 → 0 (festival/patch) is the unique assignment. "Ch.2 = Day −3" exists only on WIP/ops surfaces — confirmed by the repo-wide sweep (outline :14/:16/:30/:32/:33; script header :16; handoff/queue/status rows; historical gate/review records).**

**(c) Chain B verified as characterized.** Recomputed: reading :197's "Six more skips to festival night" with the double-skip as the first of six → festival night = M0+5 nights (~120h); with END = M0+72h (:211), :213's "miss their last dinner by two days" recomputes **exact** (120−72 = 48h). Chain B contradicts LOCKED rows directly (S36/S39 "3 days before"; S25; S32/S33/S37/S77 patch-on/mid-festival; plus the EP.2 DRAFT's reader-facing tie at :18). It contradicts **zero published bytes** — full sweep of both readers confirms the published countdown corpus is exactly: the 8.0 tonight/six-hours frame, the well's "two more days," 11:58/11:59, the festival-night invitation, "NINE DAYS LEFT"→"THREE," and the untied endcard. No published day label, no 72h tie, no patch–festival tie. The census's per-line claims that B breaks :65 (either reading), :105, and :207's register also verify: Ch.1 :65's surrounding prose ("planned accordingly… where a man should stand when a world went under") pins the ledger's "Festival night" entry to the END (the dinner is not minted until :93), so under B the ledger's own entries (:65 end=festival-night, :105 nine-out, :197 six-skips) cannot cohere.

**(d) The irreducible wobble set is exactly :65 / :197 / :213.** Per-line recompute under Chain A matches census §4.4 verdict-for-verdict: :55/:63 elapsed ✓; :65 ✗ both readings (reading (a) puts festival at ~M0+9d against every chain; reading (b) makes the pre-collapse ledger already know ~3, collapsing the 9→3 collapse against :105/S25/S55); :105 ✓ records-coherent (pre-collapse ETA 9 = story_bible :45, registry :187, published S55); :197 ✗ (six skips vs ~3 nights); :207 ✓ (9→~3 hedged = the records' "~3"); :211 ✓ (END at M0+72h exact); :213 ✗ (under A the end lands ON festival night); :215 ✓. **No more, no fewer; :105 and :211 need no touch under Chain A — confirmed.**

## Check 4 — Option integrity: **PASS**

- **Change lists resolve.** Option 1's outline list (:16/:30/:32/:33 + :14) is **complete** — the sweep finds no other Day-label line in the outline; script :16 is the only header token; the handoff/queue/status/changelog rows all resolve at the cited lines (base blobs). Option 2a's lines (MPB :42; registry :188/:29/:180/:187; ledger :2) resolve; the MPB :2 upstream-export note it invokes exists as claimed. Option 2b's lines resolve (registry :187 "3 days before"; ledger :3; story_bible :45; MPB :42/:21; script :18); its MPB :33 entry is prudential over-inclusion (the "Founding Festival imminent" line needs review, not necessarily change — not an error). Option 3's list (Ch.1 :65/:197/:213 — nothing else) is exactly the verified wobble set.
- **2b's fair-play flag is CORRECT.** The published endcard (readers p2 :223–:224) asserts "Seventy-two hours." as the pivot into EP.2; under 2b (festival ≈ M0+96h, or patch detached) nothing occurs ~72h after the published cliffhanger, and the published "THE WORLD JUST ANSWERED: THREE." (p2 :217) degrades — a published tease made retroactively false, violating the fair-play law (MPB :11, law 4: withhold, never lie). Flag verified; it is the only option that touches a published byte's truth value. The census's companion posture — full Chain B stays *endcard-compatible* because "Seventy-two hours." is untied and true of the END under B — also verifies.
- **Option 3's never-published claim is CORRECT.** Direct search of the EP.1 script and both readers: none of :65's apposition, :197's "six more skips," or :213's two-day miss (nor :211's "to live" tie, nor :105, nor :205) exists on any published surface; variance :50 independently records that EP.1 ends before the prose's final beats. An erratum on those three lines cannot contradict any published reader.
- **Cited house precedent is real.** The "accepted Ch.1:161 erratum" (Options 1/3 ripple) verifies: DEC-0018 Owner ruling, TASK-0031 one-word correction, Canon+Continuity reviewed, ACCEPTED (CHANGELOG :177/:186/:196/:233).
- **Option W's subject verifies:** script :127 "THE FESTIVAL-EVE ADDRESS" matches neither chain (two days before festival day under Chain A; three under the WIP convention), while outline :42 and MPB :20 both say "festival speech." Reader-invisible; correctly a ride-along candidate, correctly not minted as a finding by the census.

## Check 5 — Neutrality audit: **PASS**

The pack states as forced only what recomputation confirms is forced, and conditions it correctly (standard rollover named as the hinge; 2a explicitly explores non-standard semantics with its endpoint problem stated). Options are presented symmetrically — minimal-change sets are given in **both** directions (1+3 for full Chain-A recompute; 2a+3′ for preserving every WIP byte); flags are mechanical consequences of the fair-play law or locked rows, not taste; the Chain-B option is recorded with its exact prose-side strengths and its locked-row costs, unleaned. §6 explicitly declines to recommend among 0/1/2a/3/3′/W and reserves locked-row amendment to the Owner; §9 states the census decides nothing. **No language pre-decides the Owner's ruling.**

## Check 6 — Undecided discipline: **PASS**

Q-01, Q-02, Q-16 and every other PENDING/WAITING_FOR_CREATOR/UNDECIDED item are mentioned only as remaining exactly as they were (§0 header, quoted registry text) — none is touched, leaned on, or shaded. No Q is minted. CR-005 and CT-008 remain OPEN at their recorded severities in the pack's own framing (§0, §9). The open Owner word gate is referenced (Option W) but not exercised.

## Check 7 — Hygiene (raw bytes of the census file + its commit message): **PASS**

- Zero URLs, zero Drive/Docs ids, zero external document ids in the census blob `a9cf936f…` and in the `c7915a86…` commit message (raw-byte grep; the only long tokens are git SHAs). Platform pointers in swept files (story_bible :202–:206; reader image tags) are referenced by path/line only, never reproduced — as §1 promises.
- Sealed twist bank: not sought, not referenced, not reconstructed; the census additionally abstains from assigning story meaning to the geometry (§8) — verified against the full text.
- QA-242: zero mentions anywhere in the census (not re-flagged; register :18 posture respected).
- Naming note verified: the census's "MPB = `studio/01_Lore/Master_Project_Bible.md`" resolution matches the FINDINGS_REGISTER CR-005 row's own citation (`FINDINGS_REGISTER.md` :42 cites the same path and line :42). No path misdirection.

---

## Findings (CR namespace — continues from CR-006 per `FINDINGS_REGISTER.md` :19/:23 and the TASK-0005_CANON renumber note; repo-wide collision check for CR-007 clean at HEAD)

| ID | Severity | Finding |
|---|---|---|
| CR-007 | **S4** (census completeness; records-about-records; zero effect on §§4–7 conclusions) | **§3.7 propagation map misses three review-record surfaces carrying the swept tokens:** (i) `studio/06_Operations/REVIEWS/CYCLE-0002_GATE-LORE.md` :38 — the TASK-0017 gate's "Day −3 countdown" spot-check row (side-B token; the CHANGELOG :84 summary of this gate IS mapped at S81, the gate file itself is not); (ii) `studio/06_Operations/REVIEWS/CYCLE-0002_GATE-VISUAL.md` :78 — verbatim registry citation "§5 'Day 0, festival night'" in the gate's evidence row (side-A-consistent, same class as S86); (iii) `studio/06_Operations/REVIEWS/CYCLE-0001_REVIEW.md` :66 — the 9→3 countdown consistency verification row (chain-neutral register). §3.7's "listed so the Owner can see **every** place each convention has spread" and §1's sweep claim overstate by exactly these three rows. All three are historical review records that quote or verify other surfaces; none bears on the conflict, the uniqueness claim, or any option. Fix: a three-row §3.7 addendum riding the census's next authorized touch (natural window: the post-ruling annotation pass). |
| CR-008 | **S4** (census precision; substance preserved in all three) | **Three wording/attribution nits:** (i) S87 attributes "'Day −3 night' baseline phrasing" to `studio/07_Repository/INDEX.md` :71, :121, :130 — only :71 carries the label; :121/:130 carry moon-skip-cliffhanger descriptions with no day token (they belong in a propagation map, but the stated bearing over-attributes). (ii) §3.8 lists "`Trailer_v2_Storyboard.md` moon-skip prompt references" — that file carries zero moon/skip tokens at the base tree (`Video_Workflow.md` does; the classification is right for the file that has them). (iii) §3.4's header grounds the readers-supersede-script relation in "(S34 precedence)" — MPB :60 orders records > bible > prose > readers and never mentions the script; the relation actually lives in `studio/06_Operations/SOURCE_OF_TRUTH.md` :29/:33 (and CT-007's own citation), which the census's §2 index row states correctly without citation. Fix: same ride-along annotation window as CR-007. |

**Referenced, not re-minted:** CR-005 and CT-008 (the census's subjects) remain OPEN, untouched by this review. The S74 "FESTIVAL-EVE" stray is the census's own disclosed observation with a ride-along path (Option W) — correctly not a minted finding there, and not re-minted here.

---

## Verdict detail & recommendations (records only — nothing here is an instruction to the Owner)

1. **The census is safe to rule on as delivered.** Both S4 findings are annotation-grade and can ride the census's next authorized touch after the ruling; neither needs to precede it.
2. **The specific sentence the Owner will rely on is verified:** from LOCKED + PUBLISHED surfaces exactly one timeline recomputes (Chain A: festival night = patch night = Day 0 ≈ 72h after the double-skip midnight; labels forced Day −3 baseline night → Ch.2 = Day −2 → Day 0 under standard rollover); the "Ch.2 = Day −3" convention lives only on WIP/ops surfaces; locked + published surfaces carry no conflict; the irreducible Ch.1 wobble is exactly :65/:197/:213 with :105/:211 records-coherent; Option 2b is the only option that would falsify a published byte; Option 3's three lines have no published counterpart.
3. For the EP's record: the dispatch-anticipated namespace is honored — findings here are CR-007/CR-008; `REVIEWS/TASK-0042_CANON.md` is this review's only write; no ledger was edited; QA-242 was not re-flagged; the sealed bank was not sought.

---

*Canon Review Agent · TASK-0043 · review records only: this file passes/fails and cites; it decides nothing. No canon touched, no lock, no retcon, no UNDECIDED item resolved, no Q minted, no URLs or external document ids, sealed bank untouched, QA-242 not re-flagged. `[AGENT:Canon Review]`*

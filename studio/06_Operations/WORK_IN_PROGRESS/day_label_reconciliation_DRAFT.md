# Day-Label + Countdown Reconciliation Census (TASK-0042) — DRAFT

**DRAFT — EVIDENCE CENSUS FOR THE OWNER. THIS DOCUMENT DECIDES NOTHING.**
The ruling on CR-005 (day-label convention) and CT-008 (Ch.1 countdown wobble) belongs to the Owner alone. No canon file, bible, registry, ledger, outline, script, review, or reader file is edited by this task; nothing below locks, retcons, or resolves any OPEN or UNDECIDED item (Q-01, Q-02, Q-16 and all others remain exactly as they were). Every quote below is transcribed byte-exact from the pinned tree (bracketed ellipses mark trims); every claim of absence was verified by search-and-absence against the same tree. This document is additive, records-only, night-rules DRAFT. Any actual fix is a future Owner-authorized Work Order.

- **Author:** ② Lore Department, CYCLE-0008 (TASK-0042, P2 — Owner-decision prep per the CYCLE-0006 close-out's recommended next increment).
- **Date:** 2026-07-20.
- **Base commit:** `94f1ca21b3fa09a343bacc3d2d1d5d3332a73931` (HEAD at sync = the dispatch base; no post-dispatch drift; all `file:line` locators and blob SHAs below are against this tree).
- **Provenance:** CR-005 (S4, `REVIEWS/TASK-0005_CANON.md`, Check 2 + findings table) and CT-008 (S4, `REVIEWS/TASK-0005_CONTINUITY.md`, C1 + findings table), both recorded in `studio/06_Operations/FINDINGS_REGISTER.md` :42 / :51. Canon Review asked that Ch.1:197 be glanced in the same pass (`TASK-0005_CANON.md` :65, :79); it is covered in §4.4 below. Both findings are pre-existing and S4; the delivered EP.2 script DRAFT is day-label neutral (zero on-panel day numbers, recomputed by both reviews and re-verified here) — **nothing in production blocks on this census.**
- **Naming note:** the dispatch's "Manhwa Production Bible §5–6" resolves to `studio/01_Lore/Master_Project_Bible.md` ("MPB") §5–6 — the "TIMELINE (constants)" section at :41–:43. No file titled "Manhwa Production Bible" exists at the base commit (verified by repo-wide search); the FINDINGS_REGISTER row for CR-005 cites the same MPB path and line.

**STATUS NOTE — RULED (added under TASK-0044, 2026-07-20, an authorized rider of DEC-0019).** The question this census was built for has been ruled by the Owner: **DEC-0019** (`studio/06_Operations/DECISION_LOG.md`, landed at commit `e9f6e688`) — **Chain A is canonical** (baseline night = Day −3 → Ch.2's dramatized day = Day −2 → festival/patch = Day 0); fix set = **Option 1 + Option 3** (§5 below), archive-don't-delete; CR-007/CR-008 S4 nits authorized to ride the same touch; **Option 2b explicitly rejected** (fair-play flag upheld). CR-005 and CT-008 are therefore **RULED** (their register rows are the ops lane's to update; this note changes no finding row). TASK-0044 execution (see `HANDOFFS/TASK-0044-LORE.md`): Option 1 applied to `ep2_outline_proposal.md` (:16/:30/:32/:33 relabeled; :14 reviewed — verbatim ledger citation, Chain-A-correct night label, no change); Option 3 applied to Ch.1 :65/:197/:213; the change list's `ep2_script_DRAFT.md` :16 row is DEFERRED to the pending word gate per the dispatch's hard limits (census Option W was not ruled). Riders applied in this file: CR-007 (rows S88–S90 added to §3.7) and CR-008 (S87 narrowed to :71; §3.8 moon-skip attribution corrected to `Video_Workflow.md` alone; §3.4 precedence gloss re-grounded in `SOURCE_OF_TRUTH.md` :29/:33). Everything below is otherwise preserved as delivered at `c7915a86` (Canon-verified at `6fb5f7bf`); statements below that CR-005/CT-008 "remain OPEN," or that the ruling is pending, describe the pre-ruling state and are retained as history.

## 0. The two findings, quoted (from `studio/06_Operations/FINDINGS_REGISTER.md`, blob `3c58f518…`)

> :42 | CR-005 | S4 | […] Ch.2 day-label conflict across the records layer: `studio/01_Lore/Master_Project_Bible.md` :42 + `CANON_REGISTRY.md` :188 label Ch.2 "Day −2/−1" vs the GATED-PASS outline + TASK-0005 dispatch "Day −3" (same calendar day, two label chains); the script is neutral — zero on-panel day numbers, recomputed. […]

> :51 | CT-008 | S4 | […] PRE-EXISTING prose-internal countdown wobble in Ch.1 (:65 "Nine days." · :197 "Six more skips" · :213 "two days") that does not recompute against :211 "seventy-two hours" or the records layer; EP.1's adaptation omitted all three lines; the EP.2 script imports none of it. […]

## 1. Method

Fresh `git clone` of `main`; HEAD verified equal to the dispatch base `94f1ca21…`. Blob SHAs recomputed via `git ls-tree` at HEAD. Pattern census over every tracked `.md` and `.html` file for: day-label tokens (`Day −N` / `Day -N` / `Day 0`), countdown words (nine days / three days / two days / seventy-two / 72-hour / six more / skips / ETA), clock times (11:58 / 11:59 / 3:07 / midnight / midday / dawn / dusk / nightfall / tonight / six hours), and festival anchors (festival night / Founding Festival). Every hit read in context; the manuscript Prologue and Chapter 1 were additionally read in full, line by line, so that no unpatterned time surface escaped. Adjacent time surfaces that carry no countdown weight were classified and listed (§3.8) rather than silently dropped. `DECISION_LOG.md` and `00_STUDIO_RULES.md` carry **zero** day-label or countdown tokens (verified absence). This file contains no URLs and no external document ids; assets and platform pointers in swept files are referenced by path and line only, never reproduced.

## 2. File & blob index (at `94f1ca21…`)

| File (repo-root-relative) | Blob SHA | Layer / status |
|---|---|---|
| `manuscript/chapters/00_prologue.md` | `a8f089438779c35befe27ca96c0f5e79c28f013a` | MANUSCRIPT_CANON (prose) |
| `manuscript/chapters/01_the_ninth_world.md` | `1623d610db98da205ef7a99477df36a97e7d06f5` | MANUSCRIPT_CANON (prose) |
| `manuscript/bible/story_bible.md` | `c444bd976c327feaa3b450c809f860adeb2bfec3` | Running lore canon |
| `studio/01_Lore/Master_Project_Bible.md` (MPB) | `4766522214c621d9266024dd8dd315c3d3969b99` | Franchise canon export |
| `studio/07_Repository/CANON_REGISTRY.md` | `f8da9aa2092d5fddeca5faae244f326b7e40fd1f` | Compiled registry (rows carry LOCKED status) |
| `studio/06_Operations/CONTINUITY_LEDGER.md` | `ffe4fc62e5244c8f3e23cd162f2eefaa471ba92a` | Authoritative state ledger (baseline charter) |
| `manuscript/manhwa/ep1_v3_script.md` | `3448be33631f1bdf75ff36bfed85c21fd67845bf` | Adaptation script (superseded by readers where they differ) |
| `readers/episode1_part1.html` | `17bce6ea6baceb0f0d6eda2fa2705760548d6fea` | **PUBLISHED** reader |
| `readers/episode1_part2.html` | `714dc7a15a89a31fce1449897e10ba94a9fba742` | **PUBLISHED** reader (incl. EP.2 endcard tease) |
| `manuscript/manhwa/ep1_adaptation_variance.md` | `f526a278895c51cf28825ecd90ae58b61ae9b76f` | Variance record (prose↔script↔readers) |
| `studio/06_Operations/WORK_IN_PROGRESS/ep2_outline_proposal.md` | `0dbb13b9844ffc304fad81f22d644d7bf57fbf58` | WIP proposal, GATED-PASS (TASK-0017) |
| `studio/06_Operations/WORK_IN_PROGRESS/ep2_script_DRAFT.md` | `e2ac6ad077016d66000bb4b0cafe2b56c9b33a93` | WIP DRAFT (TASK-0005, at word gate) |
| `studio/06_Operations/HANDOFFS/TASK-0005-LORE.md` | `90e7560c4ba4fbf408d724bd7029b759eb7e709f` | Ops handoff (delivered record) |
| `studio/06_Operations/FINDINGS_REGISTER.md` | `3c58f518a374ab47def8b1c8a44f95ceeeef1557` | Ops findings register |
| `studio/06_Operations/TASK_QUEUE.md` | `e315b60b5972d87a55706e509174d7cfc9161dc5` | Ops queue |
| `studio/06_Operations/STUDIO_STATUS.md` | `8005341d1f59923694cba110be0e7ac7b8c4cdeb` | Ops status |
| `studio/06_Operations/CHANGELOG.md` | `1e913d14568daefabf55167cf216a65c29dd8009` | Ops changelog (historical) |
| `studio/06_Operations/HANDOFFS/CYCLE-0006-CLOSE.md` | `b8476d04a49f850e377847a8bafd904a8128a55d` | Ops close-out (historical) |
| `studio/06_Operations/HANDOFFS/CYCLE-0002-LORE.md` | `b91353103722ba633ecb26095f311668ea8f8569` | Ops handoff (historical) |
| `studio/06_Operations/REVIEWS/TASK-0005_CANON.md` | `73b6784973dcd75ee1d4950783d43c79c6e31f3b` | Review record |
| `studio/06_Operations/REVIEWS/TASK-0005_CONTINUITY.md` | `6da976261f3677bc67826e8c345ea43ebcc2f3f5` | Review record |
| `studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md` | `1356127b39dae889f6559ffaacd4fe1c7e2f5356` | WIP visual spec |
| `studio/07_Repository/INDEX.md` | `250062811617a82e14a36f75f91ee9d0368bf22d` | Repository index |

Short blob prefixes in the tables below refer to this index.

## 3. Evidence census

Surfaces are numbered S1… continuously. **Bearing** states only what the surface asserts; classification of coherence is deferred to §4.

### 3.1 Prologue (8.0's last hours) — `00_prologue.md` (`a8f08943`)

| # | file:line | Byte-exact quote (trimmed) | Bearing |
|---|---|---|---|
| S1 | :4 | "The world had six hours left, and Sergeant Cha was worried about the well." | 8.0 end: six hours out at scene open. |
| S2 | :8 / :12 | "Two more days," […] / "But not the two days." | Well-completion estimate (mundane), not the patch clock — but the patch lands before the two days elapse. |
| S3 | :18 | "He had a pack on his shoulder. He'd had it on his shoulder for nine days." | 8.0's tells telegraphed ≈ **nine days** (pack carried since onset). |
| S4 | :16 / :36 | "Eighth time." / "The sun's been stuttering since Tuesday." | Tell duration texture for 8.0. |
| S5 | :30–:36 | "Tonight, then." / "Tonight." / "Down to the day?" / "Down to the hour, by the end." | End predictable to the day, then to the hour. |
| S6 | :52 | "[…] had six hours left, and only two people on the planet knew […]" | Restates S1. |
| S7 | :66 / :68 | "At 11:58 the wind quit." / "At 11:59 the stars shuffled […]" | Patch application sequence begins 11:58 PM; wave follows (≈ midnight). |
| S8 | :84 | "【VERSION 9.0 — APPLYING】" | The 8.0→9.0 patch instant. |

### 3.2 Chapter 1 (single day, ending at the double-skip midnight) — `01_the_ninth_world.md` (`1623d610`)

| # | file:line | Byte-exact quote (trimmed) | Bearing |
|---|---|---|---|
| S9 | :3 | "*Ten years later.*" | Prologue → Ch.1 gap = 10 years. |
| S10 | :55 | "Everything was not fine. He had known for nine days." | Tells running **nine days elapsed** as of Ch.1's day. |
| S11 | :63 | "Nine days of this, by his ledger. […] he'd timed it off the harbor clocktower three nights running." | Elapsed nine days restated; nightly moon-skip timing. |
| S12 | :65 | "**Festival night, said the ledger. Nine days.**" | **CT-008 line 1.** Ledger names festival night and "Nine days" in apposition — readable as (a) end = festival night, nine days remaining, or (b) end = festival night; nine days of tells elapsed. Neither reading recomputes cleanly (§4.4). |
| S13 | :67 | "[…] went to dinner early, because it was Tuesday." | Ch.1 is one day (Tuesday). |
| S14 | :93 | "Come by before closing on festival night. First bowl's on the house." | Cha's invitation pins a **festival-night dinner** in the future. |
| S15 | :105 | "Tonight was for checking the wrapping — nine days out, by the ledger —" | Evening, pre-collapse: ledger still reads **nine days remaining**. |
| S16 | :195 | "On the roof of the old hall, at 11:58, he checked the moon." | 11:58 rooftop check (numeric rhyme with S7). |
| S17 | :197 | "This was the routine of the last nine days: […] One skip a night, half a second, regular as rent. **Six more skips to festival night.**" | **CT-008 line 2 (Canon Review's requested glance).** Night-count: festival night = **six more nightly skips** from the double-skip night. |
| S18 | :205 | "[…] every bird went silent at midnight, which was seven hours off schedule, and did not resume." | Off-schedule tell at midnight (daily tell otherwise at 3:07 PM, S19). |
| S19 | :61 | "At 3:07 exactly, the birds stopped — […] four seconds, five […] what she had said to him on Saturday" | Daily 3:07 tell; vendor sampling repeat (Saturday anchor). |
| S20 | :207 | "The count was not the count. The tells were compounding. **Nine days had become** — […] — **three. Perhaps two, if the acceleration held.**" | The collapse: remaining count 9 → ~3 (hedged toward 2). |
| S21 | :209 | "For the first time in ninety years, the world was running early." | The patch is **early** relative to its own telegraphed count. |
| S22 | :211 | "[…] two hundred years of history, ten years old, **seventy-two hours to live**. […] First bowl's on the house, she'd said. Festival night." | **The 72-hour register** (remaining-to-END), juxtaposed with the festival-night dinner. |
| S23 | :213 | "**She was going to miss their last dinner by two days**, and there was no one in any world he could tell." | **CT-008 line 3.** The END precedes the festival-night dinner by ≈ two days. |
| S24 | :215 | "'Early,' […] 'You couldn't give me the nine days.'" | Restates: the original count was nine days; it was cut short. |

### 3.3 Records layer — story_bible / MPB / CANON_REGISTRY / CONTINUITY_LEDGER

| # | file:line | Byte-exact quote (trimmed) | Status / bearing |
|---|---|---|---|
| S25 | `story_bible.md` :45 (`c444bd97`) | "**Founding Festival** in ~3 days at Ch.1's end (patch arrives early — his ledger said 9 days; tells accelerated)." | Records chain: festival ≈ 3 days out at Ch.1 end; original ledger figure 9 days. |
| S26 | `story_bible.md` :46 | "Patch tells: birds silent at 3:07 PM; moonrise "skip" stutter; […] at the end, doubled moon-skips." | Tell canon (3:07 = PM fixed here). |
| S27 | `story_bible.md` :99 | "cliff: moon skips twice — **three days, not nine**" | Ch.1 drafting-log summary: collapse 9 → 3. |
| S28 | `story_bible.md` :100 | "- [ ] Ch.2 — "Last Day" (compressed: goodbyes, […] midnight tear + banner "Are you still there?")" | **Ch.2 drafting-log entry carries NO day number** (verified — this is the entry the outline cites for its "Day −3"; see S38). |
| S29 | MPB :15 (`47665222`) | "The story opens 3 days before patch nine […]" | Round register: story open ≈ 3 days before the 9.0→10.0 patch. |
| S30 | MPB :18 | "Night: the moon skips TWICE; countdown collapses 9 days → 3." | Same collapse register. |
| S31 | MPB :20 | "**CH.2 — Last Day:** compressed goodbyes; […] midnight banner addresses him: "Are you still there?"" | Locked Ch.2 beats — **no day number in the beat text**; the label lives at S32. |
| S32 | MPB :41–:42 — **§5–6 "TIMELINE (constants)"** | "## 5–6 · TIMELINE (constants)" / "[…] present = **Day −3** → Ch.2 **Day −2/−1** → Ch.3 **Day 0** (festival night, patch lands EARLY — plot, not error)." | **CR-005 side A.** The constants chain: present(=Ch.1 baseline) Day −3 → Ch.2 Day −2/−1 → Ch.3 Day 0 = festival night = patch. |
| S33 | MPB :21 | "**CH.3 — I'll Be Quick:** patch lands mid-festival; […]" | Patch lands **mid-festival** (Day 0 night). |
| S34 | MPB :60 | "Precedence: studio/00_STUDIO_RULES.md + Asset_Registry > this bible > prose chapters > readers." | Precedence law: records outrank prose; prose outranks readers. |
| S35 | `CANON_REGISTRY.md` :186 (`f8da9aa2`) | "Prologue timing | 8.0 → 9.0 rewrite, 10 years before present-day story start. Sky tear at 11:58 PM (wind quits) / 11:59 PM (stars shuffle). | […] | LOCKED" | LOCKED clock anchor for patch application. |
| S36 | `CANON_REGISTRY.md` :187 | "Present-day baseline (Day −3 night, end of Ch.1/EP.1) | **3 days before the Founding Festival**; patch ETA collapsed from 9 days to ~3 (moon skipped twice this night). […] | LOCKED" | **LOCKED**: baseline night = "Day −3 night" AND = 3 days before festival AND ETA ~3. |
| S37 | `CANON_REGISTRY.md` :188 | "Forward plan (unwritten, locked beats) | Ch.2 "Last Day" (**Day −2/−1**): […] Ch.3 "I'll Be Quick" (**Day 0, festival night**): patch lands EARLY (plot, not error); […] | LOCKED (beats) / UNDECIDED (Q-01, Q-02 specifics)" | **CR-005 side A (registry).** LOCKED forward plan carries the same chain as S32. |
| S38a | `CANON_REGISTRY.md` :29 | "Baseline state (Day −3 night, end of EP.1/Ch.1) | […] | LOCKED | ②" | Same baseline label, character-state row. |
| S38b | `CANON_REGISTRY.md` :180 | "**Baseline = end of EP.1 / end of Ch.1 prose, Day −3 night**, per `studio/06_Operations/CONTINUITY_LEDGER.md` […]" | §5 header restates the ledger label. |
| S38c | `CANON_REGISTRY.md` :202 | "Nightly moon-skip stutters (half-second, regular as rent) accelerate […]; doubled skip = countdown compression event (9 days → 3, confirmed baseline). Other patch tells: birds silent at 3:07 PM […] | LOCKED | ②" | LOCKED tell mechanics + collapse register. |
| S39 | `CONTINUITY_LEDGER.md` :2–:3 (`ffe4fc62`) | "## Baseline state — end of EP.1 (= end of Ch.1 prose), **Day −3 night**" / "- Chronology: **3 days before Founding Festival**; patch ETA collapsed from 9 days to ~3 (moon skipped twice this night)." | The authoritative baseline: the double-skip night is labeled "Day −3 night," 3 days before festival. **The label's rollover semantics (night ENDS Day −3 vs night OPENS Day −3) are not defined here — this ambiguity is the seed of CR-005 (both reviews note it).** |
| S40 | `CONTINUITY_LEDGER.md` :8 / :11 | "no visible sky damage yet in 9.0 (first crack appears end of Ch.2)" / "banner will speak at Ch.2 midnight." | Ch.2's terminal midnight = first crack + banner (both chains agree on the physical night). |
| S41 | `CONTINUITY_LEDGER.md` :9 | "Weather/light: clear festival-season nights; moon anomalies visible only to observers timing it." | Context only. |

### 3.4 Published EP.1 — script (`3448be33`) and readers (`17bce6ea` / `714dc7a1`)

The readers are the **published** surface; the script is the derived planning layer beneath them (per `SOURCE_OF_TRUTH.md` :29/:33 — the script's dialogue is "superseded by readers' wording" and the readers carry the "current published wording"; gloss corrected under TASK-0044 per CR-008: previously "(S34 precedence)," but S34/MPB :60 ranks records > prose > readers and does not itself rank script vs readers).

| # | file:line | Byte-exact quote (trimmed) | Bearing |
|---|---|---|---|
| S42 | script :6 | "P1. Pitch-black panel. 📦 "The world ends tonight."" | Published-layer cold open: end = **tonight** (8.0 frame). |
| S43 | script :12–:13 | "## SIX HOURS EARLIER — THE RED DESERT" / "P6. Caption: SIX HOURS EARLIER." | Six-hour register for the prologue (matches S1). |
| S44 | script :15 | "P8. […] 💬 CHA: "Two more days and the well is done. […]"" | S2 adapted. |
| S45 | script :21 / :31 / :32 | "The wind dies at 11:58. Then the stars move." / "P22. Pocket watch: 11:58. […] 📦 "11:58. The wind quit."" / "P23. […] 📦 "11:59."" | S7 adapted, on-panel. |
| S46 | script :51 | "P39. 💬 CHA: "Come on festival night. First bowl's free."" | Festival-night dinner invitation, adapted. |
| S47 | script :72 | "P56. Rooftop. […] 📦 "**Midnight.** The old dorm roof. I check the moon every night."" | Script labels the rooftop check "Midnight" where prose says 11:58 (S16) — variance record flags this softening (S57). |
| S48 | script :74 | "P58. FINAL SPLASH: […] 💭 "**My count said nine days left. The world just said three.**" · 💭 "For the first time in ninety years — the world is running early." → [NEXT: LAST DAY]" | The 9→3 collapse as published-layer copy; note "**my count**" (estimate framing), and no festival tie. |
| S49 | script :76 | "## EP2 PREVIEW (for planning): Last Day — […] **midnight:** the sky tears and the banner asks a question it's never asked." | Planning note: Ch.2 midnight beat. No day number. |
| S50 | readers p1 :104 / :157 / :160 / :195 | "TONIGHT." (cold open) / "TONIGHT." ×2 (dialogue) / "TONIGHT... DON'T TELL HER ABOUT THIS PLACE." | Published: 8.0 ends tonight. |
| S51 | readers p1 :125–:128 | "SIX HOURS EARLIER" (section + caption) | Published six-hour register. |
| S52 | readers p1 :149 | "TWO MORE DAYS AND THIS WELL IS FINISHED. […]" | Published well estimate. |
| S53 | readers p1 :174 / :209 / :214 | "THE WIND WILL STOP AT 11:58. […]" / "11:58. THE WIND STOPPED." / "11:59. THE STARS BEGAN TO MOVE." | Published clock anchors. |
| S54 | readers p2 :108 | "COME BY ON FESTIVAL NIGHT. FIRST BOWL'S ON ME." | Published festival-night dinner invitation. |
| S55 | readers p2 :206 / :215 / :217 / :219 | "EVERY NIGHT, I CHECK THE MOON." / "**MY COUNT SAID NINE DAYS LEFT.**" / "**THE WORLD JUST ANSWERED: THREE.**" / "FOR THE FIRST TIME IN NINETY YEARS...<br>IT'S RUNNING EARLY." | **Published collapse register: 9 → 3, framed as Han's count.** No festival tie; no day label; no explicit time-of-check. |
| S56 | readers p2 :223–:224 | "NEXT: LAST DAY" / "**Seventy-two hours. One bag to pack.** And a transfer student who hums a song from a world that never existed." | **The published endcard.** "Seventy-two hours" is asserted **untied** — not "to festival night," not "to live," not to any named event. |
| S57 | `ep1_adaptation_variance.md` :48 (`f526a278`) | "[…] prose specifies the check happens "at 11:58" […]; script instead labels this beat "Midnight" […] readers drop the specific time entirely. This is not a contradiction (11:58 rounds colloquially to "midnight") […]" | Variance record already tracks the 11:58→"Midnight" softening. |
| S58 | `ep1_adaptation_variance.md` :49 | "Load-bearing plot fact (9 days → 3) preserved exactly and consistently across prose, script, and readers — matches `CONTINUITY_LEDGER.md` baseline exactly […] Prose's hedge ("perhaps two, if the acceleration held") is dropped from adaptation […]" | The collapse register is the one countdown fact published **exactly**. |
| S59 | `ep1_adaptation_variance.md` :50 | "[…] the birds' off-schedule silence […] and the melancholy "no one... he could tell" close — does not appear in the manhwa. […]" | **Ch.1 :205 and :213 never published.** (Row also confirms EP.1 ends before the :211/:213 region's final beats.) |
| S60 | `ep1_adaptation_variance.md` :18–:19 | rows for the well-brace opening and Han's dropped "But not the two days" doubt line | :12 (S2's doubt half) never published. |

**Published-absence summary (verified against S57–S60 and by direct search of both readers):** Ch.1 :65 ("Nine days" apposition), :105 ("nine days out"), :197 ("Six more skips"), :205 (birds/midnight), :211 ("seventy-two hours **to live**"), :213 ("miss their last dinner by two days") — **none of these lines exists on any published surface.** The published countdown consists, in its entirety, of: "nine days left"→"three" (S55), "Seventy-two hours." untied (S56), the 8.0 "tonight/six hours" frame (S50–S53), and the festival-night invitation (S54).

### 3.5 EP.2 outline (GATED-PASS, WIP) — `ep2_outline_proposal.md` (`0dbb13b9`)

| # | file:line | Byte-exact quote (trimmed) | Bearing |
|---|---|---|---|
| S61 | :14 | "Per `studio/06_Operations/CONTINUITY_LEDGER.md`'s "Baseline state — end of EP.1 (= end of Ch.1 prose), Day −3 night" section:" | Outline anchors to the ledger label (S39). |
| S62 | :16 | "EP.1 ends having just recalculated the patch ETA from 9 days down to ~3 […]; Chapter 2 is titled "Last Day" and opens on **Day −3**, per `manuscript/bible/story_bible.md`'s Drafting Log entry for Ch.2 ("compressed: goodbyes... midnight tear")." | **CR-005 side B, origin point.** The outline pins Ch.2 = Day −3 and attributes the label to the story_bible drafting log — **which carries no day number** (S28). Both reviews independently verified this attribution gap. |
| S63 | :30 | "Thirteen beats, sequenced to cover Chapter 2's full compressed span (**Day −3 morning through Day −3 midnight**) in a single episode […]" | Side B: Ch.2 = one calendar day labeled Day −3. |
| S64 | :32 | "**Cold open — "72 hours, one bag."** […] establishes the **Day −3 countdown** visually before any dialogue. *Source: […] endcard framing ("seventy-two hours, one bag to pack") adopted as the episode's own cold-open register […]*" | Beat 1 register = the published endcard's 72 hours; label = Day −3. |
| S65 | :33 | "Han moving through ordinary **Day −3** academy life […]" | Side B repeated (Beat 2). |
| S66 | :24 | "`readers/episode1_part2.html`'s published endcard reads: "NEXT: LAST DAY — Seventy-two hours. One bag to pack. […]" This gives EP.2 a ready-made cold-open hook […] without treating the readers' promotional copy itself as new canon […]" | The outline itself marks the endcard as promotional register, not new canon. |
| S67 | :38 | "*Source: […] `story_bible.md` 9.0 World quick canon (Founding Festival ~3 days at Ch.1 end).*" | Outline simultaneously cites the ~3-days-to-festival record (S25). |
| S68 | :44 | "**Midnight — the sky tears; the banner speaks.** […]" | Beat 13 = Ch.2 terminal midnight (agrees with S40). |

### 3.6 EP.2 script DRAFT (WIP, at word gate) — `ep2_script_DRAFT.md` (`e2ac6ad0`)

| # | file:line | Byte-exact quote (trimmed) | Bearing |
|---|---|---|---|
| S69 | :9 | "**Timeline register:** reader-facing countdown uses the outline's Beat-1 register ("seventy-two hours"); day-number labels appear in production headers only, per the outline's own citation practice." | The script's own D3 discipline statement. |
| S70 | :16 | "## DAWN — SEVENTY-TWO HOURS (white bg) — [outline Beat 1 · **production label: Day −3, dawn**]" | **The file's only "Day −3" token** (recomputed: zero on-panel day numbers anywhere). Production header, reader-invisible. |
| S71 | :18 | "P1. […] 📦 "**Seventy-two hours to festival night.**"" | Reader-facing register — note the script **ties** 72 hours to festival night (the published endcard, S56, leaves it untied; prose :211 ties it to "to live"). |
| S72 | :73 / :77 / :78 | "## MIDDAY — THE CITY PRACTICES ITS SMILE" / "P42. **3:07.** The plane trees go silent […] "Four seconds of silence. Five. […]"" / "P43. […] 💭 "On schedule. It's the off-schedule tells that worry me now."" | Clock tells at canon values; inherits Ch.1's true final beat (S18) without a number. |
| S73 | :83 | "P45. […] 📦 "He was the only graveyard eight worlds had. **Tonight**, he held the service."" | Same-day register only. |
| S74 | :127 | "## NIGHTFALL — **THE FESTIVAL-EVE ADDRESS** (white bg) — [outline Beat 11: one planted sentence]" | **Census-noted stray (production-header layer, reader-invisible; not a minted finding):** "FESTIVAL-EVE" is a day-relative token that matches **neither** label chain — under the records chain (§4.2) the address evening is two days before festival day; under the outline's Day −3 it is three. The outline's own Beat 11 title (:42) says "festival speech," not festival-eve; MPB :20 says "festival speech." One-word smoothing is available inside the already-open word gate if the Owner wishes (§5, Option W). |
| S75 | :136–:140 | "## THE ROOF OF THE OLD HALL […]" / "P71. […] 📦 "**11:58.** The routine, one more night."" / "P72. […] 💭 "**The count is not the count anymore.** Watch anyway."" / "P73. […] The watch ticks toward midnight […]" | Restores the prose 11:58 (S16) that EP.1 had softened (S47/S57); countdown handled qualitatively (echo of S20), no number. |
| S76 | :142 | "## MIDNIGHT — THE FIRST CRACK (black bg) — [outline Beat 13 […]]" | Terminal midnight (agrees S40/S68). |
| S77 | :150 | "## EP3 PREVIEW (for planning): I'll Be Quick — the patch lands **mid-festival**; […]" | Agrees S33 (patch = festival night). |

### 3.7 Ops/review propagation map (context — these are records **about** the labels, not canon surfaces; listed so the Owner can see every place each convention has spread)

| # | file:line (blob) | Carries |
|---|---|---|
| S78 | `HANDOFFS/TASK-0005-LORE.md` :23, :56, :66, :68 (`90e7560c`) | Side B "Day −3" in the beat table and D-declarations; **D3 at :66** is the delivered flag that routed CR-005: "the same calendar day under two labeling conventions […] no new Q minted and nothing resolved by this draft." |
| S79 | `TASK_QUEUE.md` :43, :47 (`e315b60b`) | TASK-0038 row: "timeline anchors (Day -3 countdown, […])"; TASK-0042 row (this WO). |
| S80 | `STUDIO_STATUS.md` :27 (`8005341d`) | CYCLE-0008 status line quoting both sides ("Day -2/-1" vs "Day -3"). |
| S81 | `CHANGELOG.md` :84, :222 (`1e913d14`) | Historical: TASK-0017 gate spot-check ("Day −3 countdown […] resolve exactly" — the gate verified the *citation resolves*, i.e. the outline says what it says; the day-number attribution gap was found later by TASK-0037/0038); CYCLE-0006 findings summary. |
| S82 | `HANDOFFS/CYCLE-0006-CLOSE.md` :71 (`b8476d04`) | The recommended-next-increment text this WO executes. |
| S83 | `HANDOFFS/CYCLE-0002-LORE.md` :30–:31 (`b9135310`) | Historical: outline-delivery handoff naming "Day −3/countdown acceleration" among anchors. |
| S84 | `REVIEWS/TASK-0005_CANON.md` :31, :65, :79 (`73b67849`) · `REVIEWS/TASK-0005_CONTINUITY.md` :18–:24, :84 (`6da97626`) | The findings' own analysis (quoted in §0). |
| S85 | `FINDINGS_REGISTER.md` :42, :51 (`3c58f518`) | The consolidated rows. |
| S86 | `Trailer_v2_Gap_Specs_DRAFT.md` :96 (`1356127b`) | ""Day 0, festival night" — CANON_REGISTRY §5 forward plan" — Day 0 usage consistent with S37 (no side-B propagation into visual specs). |
| S87 | `INDEX.md` :71 (`25006281`) | Index description carrying "Day −3 night" baseline phrasing (side A). *(Corrected under TASK-0044 per CR-008: :121/:130, previously co-listed here, carry no day-label phrasing — moon-skip-cliffhanger descriptions only.)* |
| S88 | `REVIEWS/CYCLE-0002_GATE-LORE.md` :38 (`e7a6a195`) | Historical: the CYCLE-0002 ② gate (TASK-0008/0017 review) spot-check item 4 — "**"Day −3 countdown"** — outline cites `CONTINUITY_LEDGER.md`'s baseline heading ("Baseline state — end of EP.1..., Day −3 night") and `story_bible.md`'s Ch.2 drafting-log entry. Confirmed verbatim in both live files." Chain-neutral: the gate verified the citations resolve, not the day-number attribution (same posture as S81's CHANGELOG :84 note). *(Row added under TASK-0044 per CR-007.)* |
| S89 | `REVIEWS/CYCLE-0002_GATE-VISUAL.md` :78 (`36f0d959`) | Historical: the CYCLE-0002 ③ gate (TASK-0018 review) evidence sweep carries the verbatim registry cite "§5 "Day 0, festival night"" among its ALL-verbatim citation checks — Day 0 usage consistent with S37 (as S86; no side-B propagation into the visual lane's review). *(Row added under TASK-0044 per CR-007.)* |
| S90 | `REVIEWS/CYCLE-0001_REVIEW.md` :66 (`986e42ef`) | Historical: the CYCLE-0001 cycle audit (TASK-0016) verification row — "**9 days → 3 days countdown**: verified consistent across prose, script P57-58, and reader Part 2's "MY COUNT SAID NINE DAYS LEFT" / "THE WORLD JUST ANSWERED: THREE" — matches `CONTINUITY_LEDGER.md` baseline exactly, as the record claims." Chain-neutral (collapse register only; no day label). *(Row added under TASK-0044 per CR-007.)* |

### 3.8 Adjacent time surfaces considered and classified non-bearing

Swept, read in context, and excluded from the reconciliation question (listed for census completeness): Ch.1 :59/:67 Tuesday rounds (single-day structure anchor) · Ch.1 :83 "Festival week." (season register) · Ch.1 :87 "eleven minutes" (scene duration) · Ch.1 :95 ledger "page ninety-one" (not time) · Ch.1 :101 "dead for seventy years" (master's era) · prologue :64 sundown (scene beat) · readers/script "TONIGHT" tokens beyond S42/S50 (same-night registers) · EP.2 script :24/:80 "MORNING ROUNDS"/"DUSK" headers and :132 P68 "tonight" (time-of-day only, no day claim) · `story_bible.md` :204 trailer production note (clip titles only; no day/countdown claim) · `Video_Workflow.md` moon-skip prompt references (visual register only; attribution corrected under TASK-0044 per CR-008 — `Trailer_v2_Storyboard.md`, previously co-cited here, carries no moon-skip token). `DECISION_LOG.md` and `00_STUDIO_RULES.md`: zero relevant tokens (verified absence). Ch.1 :205's "seven hours off schedule" (S18) bears on the 3:07-tell schedule, not the day count; it is census-recorded and needs no reconciliation under any option below.

## 4. Arithmetic reconstruction

**Definitions.** Let **M0** = the double-skip midnight that ends Ch.1 (the 11:58→midnight window of S16–S22; the ledger's "Day −3 night," S39). Let **F** = festival night (the night of the festival day; Cha's dinner, S14/S54, happens on it "before closing"). "Standard rollover" = calendar days change at midnight and "Day −N" names the calendar day N days before Day 0.

### 4.1 What the LOCKED + PUBLISHED surfaces assert

1. Day 0 = festival night, and the patch lands ON it, early, mid-festival — S32, S33, S37, S77 (LOCKED rows + MPB constants).
2. The baseline (M0) is "3 days before the Founding Festival" — S36, S39 (LOCKED row + authoritative ledger).
3. The patch ETA collapsed from 9 days to ~3 at M0 — S25, S27, S30, S36, S38c, and **published** S55 ("MY COUNT SAID NINE DAYS LEFT." / "THE WORLD JUST ANSWERED: THREE.").
4. "Seventy-two hours." is the published pivot into EP.2 — S56 — asserted **untied** to any named event.
5. The baseline night itself is labeled "Day −3 night" — S36, S38a, S38b, S39.
6. Ch.2 is labeled "Day −2/−1" and Ch.3 "Day 0" — S32, S37 (both LOCKED-status surfaces).

### 4.2 Derivation (records chain, "Chain A")

From (1)+(2)+(3): F ≈ patch ≈ M0 + 3 days ≈ M0 + 72h. From (4): the 72-hour figure matches M0 + 72h exactly. Under standard rollover, with Day 0 := festival day (1): the night ending at M0 belongs to the calendar day three days before festival day — **Day −3** ✓ consistent with (5). The single daylight day Ch.2 dramatizes (dawn after M0 → the following midnight) is then **Day −2**, and its terminal midnight (first crack + banner, S40/S68/S76) is the Day −2/Day −1 boundary — after which **Day −1 passes largely undramatized** before Ch.3 = Day 0. This chain satisfies (1)–(6) simultaneously. Two readings of "Ch.2 Day −2/−1" (S32/S37) both fit inside it, and the census cannot distinguish them from committed bytes:
- **A-i (day + terminal midnight):** Ch.2 = Day −2, with "/−1" naming the midnight rollover its cliffhanger lands on.
- **A-ii (original two-day plan):** the MPB constants predate the GATED outline, which compressed Ch.2 to one day (S63); "−2/−1" may simply be the earlier two-day plan for Ch.2, of which the outline dramatizes the first day.

**Chain A is the unique assignment.** Exhaustive check of the alternatives against (1)–(6):
- Treating M0 as the *first* instant of Day −3 (so Ch.2's daylight day = Day −3, the outline's label, S62/S63/S70): then Day 0 = festival day sits 4 rollovers after M0 → F-night ≈ M0 + 96h, violating (2), (3) and the exact fit of (4); alternatively F must be pulled back to M0+72h while keeping the label, which breaks standard rollover (the same physical day would need two labels). No uniform rollover convention keeps **both** "Ch.2 = Day −3" **and** "Day 0 = festival at M0+72h." A night-anchored labeling convention (days counted sunset-to-sunset, or labels naming "nights remaining") can be *constructed* to make Ch.2 = "Day −3" locally, but every construction checked breaks at the far end (festival day would land at Day −1 or the label chain must skip a number); no committed record defines such a convention.
- Conclusion: **restricted to LOCKED and PUBLISHED surfaces, there is no conflict at all.** The committed label chain −3 (baseline night) → −2 (Ch.2's day) /−1 → 0 (festival/patch) is arithmetically self-consistent and unique. The "Day −3 = Ch.2" convention exists only on WIP/ops surfaces (outline S62–S65, script production header S70, handoff S78, queue/status rows S79–S80), where it originated as the outline's extension of the ledger's "Day −3 *night*" label across the midnight boundary into the next morning, attributed to a drafting-log entry that carries no day number (S28/S62).

### 4.3 The one other self-consistent timeline ("Chain B," prose-local)

Read purely inside Ch.1's rooftop scene, a second timeline is constructible: **F = M0 + 5 nights (~120h)** and **END = M0 + 72h**. Then S17 ("Six more skips to festival night," counting the double-skip as the first), S22 ("seventy-two hours to live"), and S23 ("miss their last dinner by two days": 120h − 72h = 48h) become **mutually exact** — three prose lines cohering to the hour. But Chain B contradicts LOCKED/records surfaces directly: S36/S39 ("3 days before the Founding Festival"), S25, S32/S37/S33/S77 (patch lands ON festival night; under Chain B the patch lands two days *before* the festival and the entire Ch.3 "mid-festival" premise moves), and S71 (the EP.2 DRAFT's reader-facing "Seventy-two hours **to festival night**"). It contradicts **zero published bytes** — the endcard's "Seventy-two hours." is untied (S56) and no published surface ties patch to festival or carries a day label (§3.4 absence summary). Census posture: Chain B is *not derivable* from locked surfaces; it is what two of the three CT-008 lines locally imply. Adopting it would be a deliberate Owner amendment of locked rows, not a reconciliation.

### 4.4 Chapter 1 line-by-line recompute under Chain A (the CT-008 wobble, made exact)

| Line | Under Chain A (F = END = M0+72h) | Verdict |
|---|---|---|
| :55 / :63 (nine days *elapsed*) | Tells began 9 days before Ch.1's day. No remaining-time claim. | ✓ coherent |
| :65 "Festival night, said the ledger. Nine days." | Reading (a) "festival night is nine days away" → festival at ≈ M0+9d ✗; reading (b) "the end lands on festival night; nine days of tells so far" → makes the *pre-collapse* ledger already place the end ~3 days out, collapsing the collapse ✗. The apposition survives only as a loose journal register. | ✗ **wobble (CT-008 line 1)** |
| :105 "nine days out, by the ledger" (evening, pre-collapse) | The ledger's pre-collapse ETA was 9 days (S25/S55); the collapse happens hours later at M0. | ✓ coherent — **note: :105 needs no correction under Chain A** |
| :197 "Six more skips to festival night" | Festival is ~3 nights out at M0, not six. | ✗ **wobble (CT-008 line 2; Canon Review's :197-vs-:211 glance resolves as: :211 is the records-coherent line, :197 is not)** |
| :207 "Nine days had become — three. Perhaps two" | Exactly the records register (9 → ~3, hedged). | ✓ coherent (the hedge is why records say "~3") |
| :211 "seventy-two hours to live" | END at M0+72h. | ✓ coherent |
| :213 "miss their last dinner by two days" | Under Chain A the end falls ON festival night — the dinner is missed by hours (or by the patch mid-festival), not by two days. Exact only under Chain B (§4.3). | ✗ **wobble (CT-008 line 3)** |
| :215 "You couldn't give me the nine days." | The telegraphed 9 days were cut to ~3. | ✓ coherent |

**Result: the irreducible wobble set is exactly CT-008's three lines (:65, :197, :213) — no more, no fewer.** No single timeline reconciles all Ch.1 lines: Chain A clears everything except those three; Chain B clears :197/:211/:213 but breaks :65 (either reading), :105, :207's register, and the locked records. The wobble is mechanically irreducible *within the prose as written*.

**Pattern note (context, no adjudication):** the Prologue gives 8.0 a ~nine-day telegraph (S3); Ch.1 gives 9.0 nine days *elapsed* at Ch.1's day plus a pre-collapse ETA of nine *remaining* (S15/S25) — a deliberate-looking "nine days" rhyme whose two halves cannot both be exact. Whether the rhyme or the arithmetic wins is a voice/texture call, which is one reason §5 leaves the prose options to the Owner.

## 5. Reconciliation options (neutral; combinable; none actioned here)

Fair-play law (MPB :11, creator law 4): published surfaces may withhold, never lie. Per §3.4, **no published byte carries a day label, ties "Seventy-two hours" to any event, or ties the patch to the festival** — so *every* option below is fair-play-clean at the published layer **except where flagged**. "Change lists" name the bytes an option would touch if the Owner orders it; this census touches none of them.

**Option 0 — Mint the convention record; change no existing bytes.**
Add a terminology/canon record (registry §5 note or lore brief) defining "Day −N" semantics (standard rollover; Day 0 = festival day; baseline night = Day −3 night; Ch.2's dramatized day = Day −2) and recording that WIP/ops surfaces written before the ruling may carry the older "Day −3" production label, to be read as the same physical day.
- Files: one new/annotated record only (placement = ④/Information Architecture's call).
- Ripple: none to existing bytes; future scripts/outlines label from the record; the S70 production header and S62–S65 outline labels stand as historical WIP with a defined reading.
- Fair-play: none (no reader-facing surface involved).

**Option 1 — Conform the WIP/production layer to the locked chain (relabel "Day −3" → "Day −2" where it names Ch.2's day).**
- Files/lines: `ep2_outline_proposal.md` :16, :30, :32, :33 (+ :14 context sentence); `ep2_script_DRAFT.md` :16 production header (word gate is already open — zero reader-facing impact since the label is a header); optionally annotate (not rewrite) the delivered handoff `TASK-0005-LORE.md` :23/:56/:66/:68 and ops rows `TASK_QUEUE.md` :43, `STUDIO_STATUS.md` :27 per EP's historical-record policy (CHANGELOG :84/:222 and review files stay untouched as history).
- Ripple: the outline is GATED-PASS — relabeling a gated artifact needs an EP-recorded amendment note (the accepted Ch.1:161 erratum is the house precedent for correcting a delivered surface with a visible record). Reviews/findings remain accurate as written (they describe the tension, which the amendment then closes).
- Fair-play: none (all touched surfaces are internal).

**Option 2a — Adopt "Ch.2 = Day −3" into the records by DEFINING night-anchored label semantics (physical timeline unchanged).**
Rewrite the constants so labels count nights-to-festival-night rather than calendar days (making the ledger's "Day −3 night" and the outline's "Day −3 morning-through-midnight" the same labeled span).
- Files/lines: MPB :42 (LOCKED constants — Owner-gated; the MPB export's upstream master document must be updated in the same ruling per the export note at MPB :2, or the export and its source will diverge); `CANON_REGISTRY.md` :188 (LOCKED row: "Day −2/−1" → "Day −3") and consistency wording at :29/:180/:187; `CONTINUITY_LEDGER.md` :2 clarifying parenthetical; plus the Option 0 record (mandatory here — a non-standard convention *must* be written down or it will drift again).
- Ripple: every future Ch.3+ label derives from the new semantics; §4.2 shows every checked night-anchored construction breaks at the Day 0 endpoint (festival day would need relabeling or a skipped number) — **if the Owner wants this option, the semantics text must solve that endpoint explicitly before anything is committed.** `Trailer_v2_Gap_Specs_DRAFT.md` :96 ("Day 0, festival night") and INDEX rows follow whatever the registry says.
- Fair-play: none at the published layer (labels were never published) — the risk is internal-consistency, not reader-facing.

**Option 2b — Adopt "Ch.2 = Day −3" with standard rollover (physical timeline MOVES: festival ≈ M0+96h, patch no longer mid-festival — or patch detaches from festival).**
- Files/lines: MPB :42, :21, :33; `CANON_REGISTRY.md` :187 ("3 days before" → "4"), :188; `CONTINUITY_LEDGER.md` :3; `story_bible.md` :45; `ep2_script_DRAFT.md` :18 (P1's "Seventy-two hours to festival night" becomes false as written); downstream: the entire Ch.3 "patch lands mid-festival" premise (S33/S37/S77) and EP.3 planning.
- Ripple: largest of any option — it re-derives the Volume-1 climax geometry.
- **Fair-play: FLAGGED.** The published endcard's "Seventy-two hours." (S56) was published as the pivot into EP.2; under 2b, seventy-two hours after the published cliffhanger nothing occurs (end and festival both sit ≈96h+ out) — the published tease becomes retroactively false rather than merely withholding. The published "THE WORLD JUST ANSWERED: THREE." (S55) similarly degrades to "four-ish." **This option contradicts published surfaces and is recorded for completeness only.**
- (The full Chain-B adoption of §4.3 — festival at +120h — carries the same structure with a larger locked-row amendment set: S25/S27/S30/S32/S33/S36/S37/S39 all change. Same fair-play posture as 2b at the endcard: "Seventy-two hours." stays literally true of the END under Chain B (S22 ties it "to live"), so Chain B is *endcard-compatible*; its cost is the locked records and the mid-festival premise, not the published bytes. Recorded, not leaned.)

**Option 3 — Owner-authorized prose erratum for the CT-008 lines (Ch.1 :65, :197, :213 only).**
Bring the three wobble lines into Chain-A arithmetic (e.g., :197 "Six more skips" → "Three more skips"; :65 apposition smoothed so festival-night and the nine-day ETA stop reading as one date; :213 "by two days" → an hours-scale or unquantified miss). Exact wording is the Owner's (word-level canon is Owner-gated; CT-001's prose-pass lane).
- Files/lines: `manuscript/chapters/01_the_ninth_world.md` :65, :197, :213 — nothing else. (:105 and :211 need no touch, per §4.4.)
- Ripple: `ep1_adaptation_variance.md` :48–:50 quote the affected region — an erratum note there keeps the variance record true (house precedent: the Ch.1:161 erratum). story_bible/MPB/registry/ledger already carry Chain A and are untouched. EP.1 published bytes untouched.
- **Fair-play: CLEAN by construction** — all three lines were omitted from the published adaptation (S59 + absence summary), so no published reader has ever seen the wobble. Note for the Owner: the prose manuscript is the future webnovel layer; an erratum *before* prose publication is free, the same edit *after* would not be.

**Option 3′ — Leave the prose as-is; canonize the wobble as voice.**
Record (lore brief / registry note) that Ch.1's countdown lines are Han's in-the-moment journal register — hedged, revisable, deliberately imprecise ("The count was not the count," S20; "perhaps two," S20; Canon Review already reads :211 as "Han's canonically unstable estimate") — and that the records layer, not the prose's local numbers, is arithmetically binding (consistent with the precedence law, S34).
- Files: one new/annotated record only; plus a standing guard note for adapters (the EP.2 draft already models the correct practice: import the register, not the numbers — S69/S75).
- Ripple: none to bytes; the wobble remains for future prose readers if the webnovel publishes unchanged (flagged, not judged).
- Fair-play: none today.

**Option W — word-gate ride-along (independent micro-item):** if the Owner is already inside the EP.2 word gate for CT-005/006/007/010 and CR-006(iii), the S74 "FESTIVAL-EVE" header word is available for one-word smoothing in the same sitting (e.g., "THE FESTIVAL ADDRESS"), under whichever label ruling is chosen. Reader-invisible either way.

**Compatibility matrix:** Option 0 combines with any. 1+3 is the minimal-change set that makes *every* surface recompute under Chain A. 2a+3′ is the minimal set that preserves every existing WIP byte. 2b (and full Chain B) stand alone and move locked canon. 3 and 3′ are mutually exclusive; everything else is orthogonal.

## 6. Recommendation posture (per the WO: only if mechanically forced)

**Mechanically forced (shown in §4.2, not a judgment):**
- The physical timeline is uniquely derivable from LOCKED + PUBLISHED surfaces: festival night = patch night = Day 0 ≈ 72h after the double-skip midnight, ETA 9→~3 at that midnight.
- Under that timeline **plus standard rollover**, the day-label set is forced: baseline night = Day −3, Ch.2's dramatized day = Day −2 (terminal midnight at the −2/−1 boundary), Ch.3 = Day 0. Any option that leaves the LOCKED rows (S32/S36/S37/S39) unamended therefore entails the Chain-A labels; "Ch.2 = Day −3" cannot be made to recompute against them under any uniform convention checked (§4.2), and Option 2b additionally contradicts a published surface (§5).
- The irreducible Ch.1 wobble is exactly :65/:197/:213 (§4.4): :105 and :211 are records-coherent and need no touch under Chain A.

**Owner judgment (explicitly NOT leaned on here):**
- WHICH reconciliation to order — 0, 1, 2a, 3, 3′, W, or a combination — is a taste, scope, and process call: whether to amend a GATED-PASS artifact vs define a convention record; whether the prose wobble is a defect (Option 3) or Han's voice (Option 3′); whether the "nine days" prologue rhyme outweighs exact arithmetic; whether label semantics should ever be night-anchored (2a). Locked canon does not force any one of these, so this census makes **no recommendation** among them.
- Amending locked rows (2a/2b/Chain B) is constitutionally the Owner's alone; nothing here shades that choice.

## 7. Fair-play audit (summary)

Published surfaces at the base commit: `readers/episode1_part1.html`, `readers/episode1_part2.html` (and the retired v1 trailer, which carries no countdown claims). Their complete countdown content is S42-analog cold-open "tonight," "SIX HOURS EARLIER," "TWO MORE DAYS" (well), 11:58/11:59, the festival-night invitation, "MY COUNT SAID NINE DAYS LEFT. / THE WORLD JUST ANSWERED: THREE.", "IT'S RUNNING EARLY.", and the untied endcard "Seventy-two hours. One bag to pack." **No published byte asserts a day label, a 72-hours-to-festival tie, a patch-festival tie, or any of the three wobble lines.** Consequences: Options 0/1/2a/3/3′/W cannot contradict a published reader under any wording; Option 2b would (flagged in place); full Chain-B adoption would contradict locked records but not published bytes (recorded in §4.3/§5 without lean). The published layer currently *withholds* the exact geometry — which is exactly what fair-play permits it to do — and every option above except 2b keeps it that way.

## 8. Sealed-territory note

The creator's twist bank was not sought, read, referenced, or reconstructed by this census. All reasoning above runs on committed repo bytes only. The census deliberately avoids assigning story *meaning* to the countdown geometry (why the patch runs early, what the festival timing signifies) — those belong to sealed or future canon; every option in §5 is constructed so any sealed reveal about the timeline's meaning can land without contradiction under whichever labels the Owner chooses.

## 9. What this census does not do

This DRAFT **decides nothing and changes no canon bytes.** It edits no manuscript line, no bible, no registry row, no ledger, no outline, no script, no review, and no reader; it resolves no finding (CR-005 and CT-008 remain OPEN at their recorded severities), mints no Q, resolves no PENDING/WAITING_FOR_CREATOR/UNDECIDED item (Q-01, Q-02, Q-16 and all others untouched), and re-flags nothing that is closed. It is an evidence census and options pack for the Owner, in the pattern of the Q-19 investigation: the ruling, its wording, and its timing belong to the Owner alone; any implementing change is a future Owner-authorized Work Order.

*Status note (TASK-0044, 2026-07-20): the paragraph above is preserved as delivered. The ruling has since occurred — DEC-0019: Chain A canonical; fix set Option 1+3; Option 2b rejected; CR-005/CT-008 RULED. See the STATUS NOTE at the top of this file and `studio/06_Operations/HANDOFFS/TASK-0044-LORE.md`.*

---

*② Lore — TASK-0042 delivered. Census only; no canon was created, moved, or fixed by this document. `[AGENT:Lore]`*

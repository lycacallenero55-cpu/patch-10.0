# Changelog
## RUN-0001 — 2026-07-19 — Studio Operations Initialization
- Adopted studio/00_OPERATING_HANDBOOK.md (creator-supplied, verbatim) as studio constitution.
- Created studio/06_Operations control layer: STATUS, SOURCE_OF_TRUTH (PROPOSED), TASK_QUEUE, DECISION_LOG, OPEN_QUESTIONS, CHANGELOG, CONTINUITY_LEDGER, VALIDATION_PROFILE (VALIDATION_UNDEFINED), INCIDENTS, HANDOFFS/, REVIEWS/, WORK_IN_PROGRESS/.
- Recorded I-0001 (reference durability) and I-0002 (mixed historical doc) incidents.
- README navigation updated to match tree (non-semantic).
- No canon, art, adaptation, or asset-lock content was modified.
## Pre-history (before ops layer)
- 2026-07-19: repo bootstrapped at commit 8d4620f (17 files: studio bibles, lore export, chapters, EP1 script, readers).
- 2026-07-18: EP.1 Parts 1–2 produced (strip model v5); trailer v1 (calm teaser) produced; art v3 + engine locked; cast masters + environment plates locked.
- 2026-07-17/18: novel Prologue + Chapter 1 drafted; concept/bible/twist-seal established.
## [ARCHIVE] — 2026-07-19 — Final knowledge drain from novel thread
- Appended (never rewrote): Art_Direction Appendix A (style provenance/discoveries); Image_Workflow_QA appendix (verbatim proven prompts + hazards); Video_Workflow appendix (verbatim Veo exemplars, Pillow card recipe, trailer-v1 clip inventory); Asset_Registry appendix (Library display-title lookup, deprecated-title blacklist, PMU provenance); OPEN_QUESTIONS Q-11–Q-14; TASK_QUEUE TASK-0011–0014; DEC-0011; HANDOFFS/THREAD_RETIREMENT.md.
- NOT preserved into repo, by design: sealed twist bank (creator's spoiler seal — workspace-only, custody question = Q-12); PMU copyrighted reference pages; platform-hosted binaries (masters/readers/trailer — see I-0001/TASK-0003); Master Project Bible platform doc (referenced by ID).
## CYCLE-0001 ① — 2026-07-19 — Five-department restructure (Conductor Mode)
- Handbook Amendment 1 adopted: five-department model (① EP · ② Lore · ③ Visual Production · ④ Repository & Canon Management · ⑤ Quality Assurance), ownership map incl. ④ → studio/07_Repository/ and ⑤ → QA files in 06_Operations, cycle order, turn mechanics, v1→v2 interpretation map. v1 body retained verbatim.
- DEC-0012 recorded (implements DEC-0011). Commit prefixes now [①-EP] [②-LORE] [③-VISUAL] [④-REPO] [⑤-QA].
- TASK_QUEUE: added TASK-0015 (④ 07_Repository layer) and TASK-0016 (⑤ Cycle-1 audit); activated TASK-0004/0008 (②) and TASK-0007 spec-draft phase (③).
- STUDIO_STATUS → CYCLE-0001 Conductor Mode; README constitution note + 01_Lore navigation line synced.
- No canon, art, adaptation, or asset-lock content was modified.
## CYCLE-0001 ② — 2026-07-19 — Lore records
- **TASK-0004** (section-tag story_bible.md): produced `studio/06_Operations/WORK_IN_PROGRESS/story_bible_tagging_proposal.md` — a heading-by-heading classification proposal (FRANCHISE_CANON / HISTORICAL_RECORD / SUPERSEDED / PRODUCTION_NOTE) for all ~28 sections of `manuscript/bible/story_bible.md`, with rationale per section. `story_bible.md` itself is byte-for-byte UNCHANGED — this is a proposal only, gated on creator approval per DEC-0008. No contradictions found between story_bible.md's FRANCHISE_CANON-tagged sections and prose/Master_Project_Bible.md; the file's mixed-content problem is confirmed to be a labeling problem, not a factual-conflict problem.
- **TASK-0008** (adaptation-variance record): produced `manuscript/manhwa/ep1_adaptation_variance.md` — a beat-by-beat comparison table (Event/Beat | Prose location | EP.1 location | Variance class | Notes) covering `00_prologue.md` + `01_the_ninth_world.md` against `ep1_v3_script.md` + both published readers. Confirms SOURCE_OF_TRUTH.md's precedence rule in practice: readers' dialogue wording supersedes the script's wording in roughly a dozen lines (documented with side-by-side examples). No load-bearing plot fact found contradicted between prose and adaptation. Largest documented omission: Yoo Ha-eun's entire Ch.1 library scene is deferred to EP.2 (confirmed intentional per CONTINUITY_LEDGER.md, but now recorded explicitly as an adaptation variance for the first time). Several minor texture/continuity notes logged for ⑤ QA and future ③ Visual attention (left-hand callus detail no longer stated in adaptation dialogue; "Attendance: perfect" detail dropped; a setup/payoff asymmetry around the "for the well" callback line; 11:58→"Midnight" numeric softening).
- No edits were made to `manuscript/bible/story_bible.md`, any chapter, `manuscript/manhwa/ep1_v3_script.md`, or `studio/01_Lore/Master_Project_Bible.md` — both deliverables are new files only, per DEC-0008 block and this turn's write-lane constraint.
- No new OPEN_QUESTIONS entries were required; existing UNDECIDED items referenced (Q-01, Q-04) were left unresolved.
- TASK_QUEUE: TASK-0004 and TASK-0008 status cells updated to IN_REVIEW (proposal/record awaiting ⑤ QA verification and eventual creator approval).
- STUDIO_STATUS moved current_department to "②-LORE done → ③-VISUAL next"; base_remote_commit/last_verified_commit advanced to d5c66125.

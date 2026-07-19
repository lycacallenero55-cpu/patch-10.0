# Source-of-Truth Register — **PROPOSED (awaiting creator approval, DEC-0008)**
Until approved: substantive canon rewrites, adaptation reclassification, asset-lock changes, and release tasks are BLOCKED (Handbook §5).

## Precedence (conservative, per Handbook §5)
1. Explicit current creator instruction (in-thread)
2. studio/00_OPERATING_HANDBOOK.md + studio/00_STUDIO_RULES.md — production law
3. studio/03_Assets/Asset_Registry.md — LOCKED visual facts
4. studio/01_Lore/Master_Project_Bible.md — on-repo franchise canon
5. manuscript/chapters/*.md — canonical narrative expression
6. studio/02_Art/*.md — visual specifications
7. manuscript/manhwa/ep1_v3_script.md + studio/04_Storyboards/* — adaptation/production specs
8. readers/*.html — derivative outputs
9. Historical/superseded records (tagged sections)

## Classification of every tracked file
| Path | Type | Notes |
|---|---|---|
| studio/00_OPERATING_HANDBOOK.md | PRODUCTION_SPEC | studio constitution (adopted RUN-0001) |
| studio/00_STUDIO_RULES.md | PRODUCTION_SPEC | compact law; where it conflicts with Handbook, Handbook wins |
| studio/01_Lore/Master_Project_Bible.md | FRANCHISE_CANON | lore-complete export; uncut master = platform doc cmrr0f9vr0bg907ade7vvxsnd (off-repo supplement, optional) |
| manuscript/chapters/00_prologue.md | MANUSCRIPT_CANON | exact text canon |
| manuscript/chapters/01_the_ninth_world.md | MANUSCRIPT_CANON | exact text canon |
| manuscript/bible/story_bible.md | MIXED: FRANCHISE_CANON sections + HISTORICAL_RECORD/SUPERSEDED production notes | section tagging = TASK-0004; do not treat wholesale as active |
| studio/02_Art/Art_Direction.md | VISUAL_SPEC | current law v3 |
| studio/02_Art/Character_Bible.md | VISUAL_SPEC | includes continuity micro-rules |
| studio/02_Art/Environment_Bible.md | VISUAL_SPEC | |
| studio/02_Art/Effects_Bible.md | VISUAL_SPEC | |
| studio/03_Assets/Asset_Registry.md | LOCKED_ASSET_RECORD | provenance fields incomplete → TASK-0003 |
| manuscript/manhwa/ep1_v3_script.md | ADAPTATION_CANON (beats) | dialogue superseded by readers' wording — variance record = TASK-0008 |
| studio/04_Storyboards/Trailer_v2_Storyboard.md | PRODUCTION_SPEC / PROPOSAL | keyframes not yet generated |
| studio/05_Production/Video_Workflow.md | PRODUCTION_SPEC | shot-length rule harmonized: 4–8s standard, shorter cuts = editorial inserts (RUN-0001, DEC-0009 pending) |
| studio/05_Production/Image_Workflow_QA.md | PRODUCTION_SPEC | |
| readers/episode1_part1.html · part2.html | DERIVATIVE OUTPUT | current published wording lives here |
| README.md | PRODUCTION_SPEC (navigation) | |
| studio/06_Operations/* | OPERATIONS RECORDS | this layer |
| manuscript/bible/twist_bank_PRIVATE.md | PRIVATE_SEALED — **NOT IN REPO by design** | workspace-only; never surface contents |

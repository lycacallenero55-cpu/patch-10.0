# PATCH 10.0 — AI Anime Studio

**PATCH 10.0** is an original dark-fantasy webnovel → Korean-webtoon manhwa → anime-trailer franchise, produced through an AI studio pipeline with hard consistency rules.

> Premise: Reality "patches" itself every ten years — a full version update that rewrites geography, history, and every living memory. One man persists. Nine worlds buried. The final patch just announced itself.

## Repository layout
```
studio/
  00_STUDIO_RULES.md            ← the operating brain (identity, asset locking, pipeline gates)
  02_Art/
    Art_Direction.md            ← locked style law, color script, strip metrics, lettering
    Character_Bible.md          ← locked designs + animation notes + continuity micro-rules
    Environment_Bible.md        ← canonical plates + variants checklist
    Effects_Bible.md            ← per-power VFX specs (glow, particles, motion grammar)
  03_Assets/
    Asset_Registry.md           ← every LOCKED asset with IDs; approval workflow
  04_Storyboards/
    Trailer_v2_Storyboard.md    ← the cinematic trailer: 17 shots, keyframe list, music map
  05_Production/
    Video_Workflow.md           ← keyframe-first Veo pipeline, choreography templates, ffmpeg
    Image_Workflow_QA.md        ← generation recipes + QA checklists
  00_OPERATING_HANDBOOK.md        <- studio constitution (single live agent + specialist subagents)
  06_Operations/                  <- STATUS, SOURCE_OF_TRUTH, TASK_QUEUE, DECISION_LOG, OPEN_QUESTIONS,
                                     CHANGELOG, CONTINUITY_LEDGER, VALIDATION_PROFILE, INCIDENTS, HANDOFFS/
manuscript/
  bible/story_bible.md          ← running lore canon
  chapters/                     ← novel prose (Prologue, Chapter 1)
  manhwa/                       ← episode scripts + published reader HTML
```
The consolidated **Master Project Bible** (22-section franchise document) lives as a platform document; a successor AI loads it by ID (see `studio/00_STUDIO_RULES.md` §7).

## Core laws (short version)
1. Nothing is generated before its assets exist and are LOCKED.
2. Every generation references locked assets; drift is re-rolled, never "redesigned around."
3. Keyframes before motion; shots are 4–8s of concrete choreography; cinema happens in the edit.
4. Flat-2D webtoon law: ink lines, flat fills, hard cel shadows — no 3D, no realism, no blur.
5. Fair-play storytelling: narration may withhold, never lie. (Some twists are sealed off-repo by the creator's own request.)

*Note: `twist_bank_PRIVATE.md` is intentionally NOT in this repository — the creator is keeping spoilers sealed from themselves.*

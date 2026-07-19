# PATCH 10.0 — REPOSITORY INDEX

> **RECORD — maintained by ④ Repository & Canon Management.** Complete navigation of every tracked file in this repository as of HEAD commit `31b36ee39044c8d545a588443add7137c6d404d9` (base of the CYCLE-0002 ④ refresh, TASK-0019), grouped by area, with one-line purpose, owning department (per `studio/00_OPERATING_HANDBOOK.md` Amendment 1 §A1.2 write-lane map), and SOURCE_OF_TRUTH classification where that file is registered in `studio/06_Operations/SOURCE_OF_TRUTH.md`. This is a navigation record, not a canon source — where it disagrees with `SOURCE_OF_TRUTH.md` or any file it describes, those files win.
>
> Files added earlier in **CYCLE-0001** are marked **"(new, CYCLE-0001)"**; files added by the CYCLE-0001 ④ turn are marked **"(new, CYCLE-0001 ④)"**. Files added since then carry their run and department — **"(new, OPS-0001 ①)"**, **"(new, OPS-0002 ④)"**, **"(new, CYCLE-0002 ②/③/⑤)"** — and this refresh's own additions are marked **"(new, CYCLE-0002 ④ — this turn)"**.

**Legend — Owning department:** ① EP · ② Lore · ③ Visual Production · ④ Repository & Canon Management · ⑤ Quality Assurance. **SOURCE_OF_TRUTH classification** (where registered): see `SOURCE_OF_TRUTH.md` for the full type list and precedence order; "—" means not yet classified there (most files added this cycle are records/proposals, not classified sources).

---

## Root

| Path | Purpose | Owner | SOURCE_OF_TRUTH class |
|---|---|---|---|
| `README.md` | Top-level orientation: premise, repository layout tree, five-department model summary, core laws short-form. | ① | `PRODUCTION_SPEC` (navigation) |

## `studio/` — root-level studio files

| Path | Purpose | Owner | SOURCE_OF_TRUTH class |
|---|---|---|---|
| `studio/00_STUDIO_RULES.md` | Compact operating law: identity, asset-locking law, the 8-gate pipeline, generation constraints, continuity micro-rules (§5 — the exact scar-side/sword-hand/hairpin/callus rules cited throughout this registry), department sign-off checklist, file map. Where it conflicts with the Handbook, the Handbook wins. | ① | `PRODUCTION_SPEC` |
| `studio/00_OPERATING_HANDBOOK.md` | Studio constitution (v2.1): **AMENDMENT 1** (binding — five-department model, write-lane ownership map, production cycle, turn mechanics, v1→v2 interpretation map) + **AMENDMENT 2** (QA gates, DEC-0013; Night Shift standing order + night rules §A2.4, DEC-0014) followed by the retained v1 body (permanent studio laws §3, authority/approval §4, source-of-truth model §5, task system §10, safe git workflow §12, domain workflows §13–19, continuity ledger §20, QA §21, handoff/run-record templates §22, live-mode protocol §11/§24). | ① | `PRODUCTION_SPEC` |

## `studio/01_Lore/` — franchise canon export (owner: ②; ④ holds custodial/registry authority only)

| Path | Purpose | Owner | SOURCE_OF_TRUTH class |
|---|---|---|---|
| `studio/01_Lore/Master_Project_Bible.md` | On-repo franchise canon export (22-section production bible, condensed): project overview, complete story so far + locked future beats, world/cosmology, timeline constants, character dossiers, systems summary, canon rules + abandoned-concept graveyard. Full uncut version is an off-repo platform document (id `cmrr0f9vr0bg907ade7vvxsnd`). Sealed twists are explicitly NOT in this file. | ② (content) / ④ (custodial/registry) | `FRANCHISE_CANON` |

## `studio/02_Art/` — visual specifications (owner: ③)

| Path | Purpose | Owner | SOURCE_OF_TRUTH class |
|---|---|---|---|
| `studio/02_Art/Art_Direction.md` | LOCKED v3 style law: flat-2D visual doctrine, color script (per-arc palette + per-character accent glow system), canonical sky-crack visual, strip/panel-layout doctrine (measured from real PMU reference), lettering rules, cinematic identity. Appendix A: style-provenance/discovery history (archived from origin thread). | ③ | `VISUAL_SPEC` |
| `studio/02_Art/Character_Bible.md` | LOCKED visual + animation canon for every designed character (CHAR-001 Seo Han through CHAR-006 Moderator spec-only): master asset IDs, design description, expression sets, animation notes, continuity micro-rules. "Pending designs" list names every character still needing a visual design. | ③ | `VISUAL_SPEC` |
| `studio/02_Art/Environment_Bible.md` | LOCKED environment plates (ENV-001–004) with canon contents + existing variants; "Locations still needing plates" gap list; per-plate variant checklist; environmental design language per era. | ③ | `VISUAL_SPEC` |
| `studio/02_Art/Effects_Bible.md` | LOCKED per-power VFX grammar: the ten FX-ID table (source/look/particles/glow/motion notes), impact-and-motion grammar for video, SFX calligraphy pack. AI must never invent an effect not specified here. | ③ | `VISUAL_SPEC` |
| `studio/02_Art/Kit_Specs_DRAFT.md` **(new, CYCLE-0001)** | DRAFT (NOT LOCKED) asset specifications for the four character-kit gaps Character_Bible.md flags as TODO: Yoo Ha-eun master pack, Yoon Si-woo master pack, Cha Mi-ran v3 master pack, full ground-up Moderator design. Headmaster Baek Do-yun recorded as an explicit deferred STUB. Every canon fact cites its source; every canon-silent detail is marked PROPOSAL. Flags one possible existing-spec inconsistency (Cha Mi-ran CM-01, see `CANON_REGISTRY.md` §1) for ⑤ QA. Produced by TASK-0007 (spec-draft phase). | ③ | — (DRAFT proposal, not yet a classified source) |
| `studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md` **(new, CYCLE-0002 ③)** | DRAFT PROPOSAL (NOT LOCKED, NOT CANON; nothing in it authorizes generation): specs for the six Trailer-v2 keyframe gaps the KF plan surfaced — three environment plates (KF-03 matched pair, KF-04 env halves, KF-12 first+last-frame centerpiece pair), monster/"extinction content" silhouette-level design language (KF-07/KF-08 attacker half), registry-card UI (KF-15). Canon-silent choices marked PROPOSAL and queued as file-local OQ-VIS-1…12 (official Q-numbers deliberately not minted by ③). Produced by TASK-0018; gate-passed (`REVIEWS/CYCLE-0002_GATE-VISUAL.md`). | ③ | — (DRAFT proposal, not yet a classified source) |

## `studio/03_Assets/` — locked-asset registry (owner: ③)

| Path | Purpose | Owner | SOURCE_OF_TRUTH class |
|---|---|---|---|
| `studio/03_Assets/Asset_Registry.md` | Single source of truth for every LOCKED asset (character masters/kits, environment plates, style anchors, published-work pointers) with image IDs; DEPRECATED section (never-use-as-refs list); approval workflow. Appendix: platform-Library display-title lookup table (cross-references registry IDs to searchable Library titles) + deprecated-title blacklist + PMU reference provenance note. | ③ | `LOCKED_ASSET_RECORD` (provenance fields incomplete → TASK-0003) |

## `studio/04_Storyboards/` — shot plans and production plans (owner: ③)

| Path | Purpose | Owner | SOURCE_OF_TRUTH class |
|---|---|---|---|
| `studio/04_Storyboards/Trailer_v2_Storyboard.md` | The cinematic Trailer v2 shot list ("THE NINTH WORLD" hype cut): 16-keyframe pre-production batch requirement, 5-act/17-shot list with narrative function/duration/composition per shot, music & pacing map, assembly specs. Keyframes not yet generated. | ③ | `PRODUCTION_SPEC` / `PROPOSAL` |
| `studio/04_Storyboards/Trailer_v2_KF_Production_Plan.md` **(new, CYCLE-0001)** | Paper-only per-keyframe production table for all 16 KFs above: named LOCKED-asset dependencies, missing/blocked dependencies (I-0001 durability, missing kits from `Kit_Specs_DRAFT.md`, and newly-surfaced gaps: monster design, registry-card UI, three missing environment plates), generation-packet checklist status, per-KF approval gate. Ends with a six-tier "Ready order." No keyframes generated. Produced under TASK-0006. | ③ | — (PLAN, IN_REVIEW — not yet a classified source) |

## `studio/05_Production/` — generation workflows (owner: ③)

| Path | Purpose | Owner | SOURCE_OF_TRUTH class |
|---|---|---|---|
| `studio/05_Production/Image_Workflow_QA.md` | Image-generation recipe (ref selection, prompt skeleton, engine/aspect settings), panel QA checklist, reader-assembly QA, escalation rule. Appendix: verbatim proven prompt exemplars + operational hazards learned (archived from origin thread). | ③ | `PRODUCTION_SPEC` |
| `studio/05_Production/Video_Workflow.md` | Keyframe-first video law, choreography prompt template, shot recipes by type, ffmpeg assembly pipeline (with environment quirks — drawtext absence, S3 fetch workaround), per-shot QA. Appendix: verbatim proven Veo exemplars + Pillow title-card recipe + Trailer v1 clip inventory (archived). | ③ | `PRODUCTION_SPEC` |

## `studio/06_Operations/` — operations control layer (owner: ①, except the ⑤-owned files noted)

| Path | Purpose | Owner | SOURCE_OF_TRUTH class |
|---|---|---|---|
| `studio/06_Operations/STUDIO_STATUS.md` | Live machine-readable + prose studio state: schema front-matter (run id/status, current department, base/last-verified commit, active tasks, blocking decisions), prose summary of current state and milestones. Updated every turn by the acting department. | ① (mechanics) / every department (own turn's fields, per A1.4) | `OPERATIONS RECORDS` |
| `studio/06_Operations/SOURCE_OF_TRUTH.md` | The PROPOSED precedence register (**DEC-0008 pending**) — precedence order for the whole repository plus a classification table for every active source file. This INDEX documents and cross-references this register; it does not replace it. | ① | `OPERATIONS RECORDS` (the register itself; PROPOSED status) |
| `studio/06_Operations/TASK_QUEUE.md` | Every tracked task with ID/title/status/priority/owner/dependencies/approval-needed/notes. Rows TASK-0001 through TASK-0020 as of this index. | Shared — any department may append rows during its own turn (A1.2) | `OPERATIONS RECORDS` |
| `studio/06_Operations/DECISION_LOG.md` | Every creator decision (DEC-0001 through DEC-0015 as of this index), with date/decision/decided-by/evidence. DEC-0008/0009/0015 remain PENDING. | ① | `OPERATIONS RECORDS` |
| `studio/06_Operations/OPEN_QUESTIONS.md` | The UNDECIDED ledger, Q-01 through Q-18 as of this index (includes Q-12, the sealed-twist-custody question; Q-13/Q-14 completeness items; and Q-15–Q-18, the QA-09 cross-link pointer rows appended by CYCLE-0002 ④ under TASK-0019). | Shared — any department may append during its own turn (A1.2) | `OPERATIONS RECORDS` |
| `studio/06_Operations/CHANGELOG.md` | Append-only history of every run/cycle/department turn, newest-relevant entries at top per run, oldest pre-history at bottom, with a special `[ARCHIVE]` entry recording the origin-thread knowledge drain. | Shared — every department appends its own turn's entry (A1.4) | `OPERATIONS RECORDS` |
| `studio/06_Operations/CONTINUITY_LEDGER.md` | The durable state ledger: baseline state at end of EP.1/Ch.1 (Day −3 night) — chronology, per-character physical/knowledge state, environment state, open threads. This is the authoritative continuity snapshot `CANON_REGISTRY.md` §5 points to rather than duplicates. | ⑤ | `OPERATIONS RECORDS` |
| `studio/06_Operations/VALIDATION_PROFILE.md` | Records `VALIDATION_UNDEFINED` status honestly — no build/test/lint/link-check tooling exists in this repo; documents what manual/agent checks exist instead. | ⑤ | `OPERATIONS RECORDS` |
| `studio/06_Operations/INCIDENTS.md` | Open incidents: I-0001 (reference-durability risk — LOCKED masters are thread-scoped, unchecksummed platform URLs) and I-0002 (story_bible.md mixes active canon with superseded production history). | ⑤ | `OPERATIONS RECORDS` |
| `studio/06_Operations/HANDOFFS/RUN-0001.md` | Handoff record for the pre-Amendment-1 initialization run (single-agent model, before the five-department restructure). | ① | `OPERATIONS RECORDS` (historical) |
| `studio/06_Operations/HANDOFFS/THREAD_RETIREMENT.md` | Orientation map for the incoming department agents at the moment the origin novel-production thread retired (DEC-0011): what's in-repo vs. off-repo-by-ID, including the sealed twist bank's custody note. | ① | `OPERATIONS RECORDS` (historical) |
| `studio/06_Operations/HANDOFFS/CYCLE-0001-EP.md` **(new, CYCLE-0001)** | ①'s Conductor Mode dispatch record for CYCLE-0001: Amendment 1 adoption, DEC-0012, task activation, dispatch order/objectives for ②③④⑤, risks flagged. | ① | `OPERATIONS RECORDS` |
| `studio/06_Operations/HANDOFFS/CYCLE-0001-LORE.md` **(new, CYCLE-0001)** | ②'s turn handoff: TASK-0004 (story_bible.md tagging proposal) and TASK-0008 (adaptation-variance record) summary, decisions needed from creator, risks flagged for ⑤/future departments. | ② | `OPERATIONS RECORDS` |
| `studio/06_Operations/HANDOFFS/CYCLE-0001-VISUAL.md` **(new, CYCLE-0001)** | ③'s turn handoff: TASK-0007 spec-draft phase + Trailer-v2 KF plan summary, why no generation happened, what the creator must approve (grouped by document), risks/findings for ⑤ and future departments (including CM-01). | ③ | `OPERATIONS RECORDS` |
| `studio/06_Operations/HANDOFFS/CYCLE-0001-REPO.md` **(new, CYCLE-0001 ④)** | The CYCLE-0001 ④ turn's handoff (TASK-0015): what was built, CONFLICT-FOR-QA items found, mechanical-fix candidates noticed but not fixed, next department ⑤. | ④ | `OPERATIONS RECORDS` |
| `studio/06_Operations/HANDOFFS/CYCLE-0001-QA.md` **(new, CYCLE-0001)** | ⑤'s CYCLE-0001 closing-audit handoff: TASK-0016 summary, VALIDATION_PROFILE refresh, CONTINUITY_LEDGER/INCIDENTS left untouched (with reasons), turn mechanics per its own QA-12 convention. | ⑤ | `OPERATIONS RECORDS` |
| `studio/06_Operations/HANDOFFS/OPS-0001-EP.md` **(new, OPS-0001 ①)** | ①'s operations-turn record: Handbook Amendment 2 (QA gates, DEC-0013) + Night Shift standing order (DEC-0014); pending rulings and queued follow-ups for CYCLE-0002 (incl. this turn's QA-09 cross-links). | ① | `OPERATIONS RECORDS` |
| `studio/06_Operations/HANDOFFS/OPS-0002-REPO.md` **(new, OPS-0002 ④)** | ④'s Owner-priority PMU-import handoff to ③: what/where/counts (85 Drive-resident story strips of 357 folder items, 28 reviewed w/ SHA-256; ZERO image bytes and zero Drive ids/links in-repo, by licensing decision), REFERENCE-ONLY constraints verbatim, ⑤ gate manifest, deviations declared, residency ruling queued (DEC-0015). | ④ | `OPERATIONS RECORDS` |
| `studio/06_Operations/HANDOFFS/CYCLE-0002-EP.md` **(new, CYCLE-0002 ①)** | ①'s CYCLE-0002 dispatch record: gated cycle under Night Rules; assignments ② (QA-04 correction + TASK-0017 outline), ③ (TASK-0018 gap specs DRAFT), ④ (TASK-0019 — this refresh), gate order per DEC-0013. | ① | `OPERATIONS RECORDS` |
| `studio/06_Operations/HANDOFFS/CYCLE-0002-LORE.md` **(new, CYCLE-0002 ②)** | ②'s turn handoff: QA-04 correction (well callback present in script P40, dropped at readers layer) + EP.2 "Last Day" outline proposal summary (Q-02/Q-04/Q-14 queued, none resolved). | ② | `OPERATIONS RECORDS` |
| `studio/06_Operations/HANDOFFS/CYCLE-0002-VISUAL.md` **(new, CYCLE-0002 ③)** | ③'s turn handoff: TASK-0018 gap-specs summary, OQ-VIS-1…12 owner-decision queue (file-local numbering; official Q-numbers deliberately not minted — ④ appends from Q-15 under TASK-0019), 401-abort re-dispatch record, PMU REFERENCE-ONLY use disclosure. | ③ | `OPERATIONS RECORDS` |
| `studio/06_Operations/HANDOFFS/CYCLE-0002-REPO.md` **(new, CYCLE-0002 ④ — this turn)** | This ④ turn's handoff (TASK-0019): §3/§4 stub-completion summary (filled vs gap-marked), Q-15–Q-18 minting + collision check, the OPEN_QUESTIONS lane exception declaration, ⑤ gate manifest (files/commits/blobs), deviations declared. | ④ | `OPERATIONS RECORDS` |
| `studio/06_Operations/REVIEWS/` | ⑤'s QA findings directory (individual reviews listed below). | ⑤ | `OPERATIONS RECORDS` (directory) |
| `studio/06_Operations/REVIEWS/CYCLE-0001_REVIEW.md` **(new, CYCLE-0001)** | ⑤'s TASK-0016 cycle audit: lane compliance of all four CYCLE-0001 commits (all COMPLIANT); TASK-0008 verification (VERIFIED-WITH-CORRECTIONS — the QA-04 wording fix ② applied in CYCLE-0002); CM-01/SW-01 adjudication evidence; continuity spot-audit (zero violations); doc-quality/process findings QA-06…QA-12 (incl. QA-09, the OPEN_QUESTIONS cross-link gap closed by Q-15–Q-18, and QA-12, the STATUS commit-pointer drift). Verdict: PASS-WITH-FINDINGS. | ⑤ | `OPERATIONS RECORDS` |
| `studio/06_Operations/REVIEWS/OPS-0002_GATE-REPO.md` **(new, OPS-0002 ⑤)** | DEC-0013 gate review of ④'s Owner-priority PMU-import turn: commit chain, pure-insertion blob verification, Drive-id/link non-leak scan, 3-strip re-download spot audit, deviation handling. Verdict: PASS (findings QA-210–QA-219). | ⑤ | `OPERATIONS RECORDS` |
| `studio/06_Operations/REVIEWS/CYCLE-0002_GATE-LORE.md` **(new, CYCLE-0002 ⑤)** | DEC-0013 gate review of ②'s CYCLE-0002 turn (QA-04 correction + EP.2 outline proposal): correction verified against sources; proposal-only discipline confirmed. Verdict: PASS (findings from QA-201). | ⑤ | `OPERATIONS RECORDS` |
| `studio/06_Operations/REVIEWS/CYCLE-0002_GATE-VISUAL.md` **(new, CYCLE-0002 ⑤)** | DEC-0013 gate review of ③'s CYCLE-0002 turn (TASK-0018 gap specs DRAFT): citation accuracy, DRAFT/PROPOSAL + night-rules discipline, REFERENCE-ONLY compliance + Drive-leak scan, byte-level blob verification. Verdict: PASS (findings from QA-220). | ⑤ | `OPERATIONS RECORDS` |
| `studio/06_Operations/WORK_IN_PROGRESS/story_bible_tagging_proposal.md` **(new, CYCLE-0001)** | ②'s TASK-0004 deliverable: heading-by-heading classification proposal (FRANCHISE_CANON/HISTORICAL_RECORD/SUPERSEDED/PRODUCTION_NOTE tags + rationale) for all ~28 sections of `manuscript/bible/story_bible.md`. Proposal only — the target file is untouched; gated on creator approval (DEC-0008 context). | ② | — (DRAFT proposal, not yet a classified source) |
| `studio/06_Operations/WORK_IN_PROGRESS/ep2_outline_proposal.md` **(new, CYCLE-0002 ②)** | ②'s TASK-0017 deliverable: EP.2 "Last Day" beat-map/outline proposal (DRAFT PROPOSAL — not a script, not canon; the TASK-0005 script stays gated on DEC-0008 + Owner word-approval). UNDECIDED items presented as Owner options (Q-02 keepsake choice etc.), none resolved; sealed material untouched. | ② | — (DRAFT proposal, not yet a classified source) |

## `studio/07_Repository/` — canon registry, index, templates, prompt library, references, archive (owner: ④) **(area established CYCLE-0001 ④)**

| Path | Purpose | Owner | SOURCE_OF_TRUTH class |
|---|---|---|---|
| `studio/07_Repository/CANON_REGISTRY.md` | Item-level canon record register, seven sections: Characters, Key Objects, Locations/Environments, Powers/Effects, Timeline anchors, Story-visible laws, Reference Libraries (§7 added by OPS-0002) — each entry with a source pointer, status label, and owning department. §3/§4 STUBs completed CYCLE-0002 ④ (TASK-0019). Records disagreements as CONFLICT-FOR-QA rather than resolving them. Recommend-only; never overrides `SOURCE_OF_TRUTH.md`. | ④ | — (RECORD, indexes canon, is not itself a canon source) |
| `studio/07_Repository/INDEX.md` | This file. | ④ | — (RECORD) |
| `studio/07_Repository/TEMPLATES/WORK_ORDER_TEMPLATE.md` | Reusable work-order template mirroring Amendment 1 conductor practice (cycle/department/objective/read-first/deliverables/constraints/done-means/report-back). | ④ | — (TEMPLATE) |
| `studio/07_Repository/TEMPLATES/TURN_HANDOFF_TEMPLATE.md` | Reusable turn-handoff template aligned with Handbook v1 §22 run-record fields plus Amendment 1's `CYCLE-<n>-<dept>.md` naming convention. | ④ | — (TEMPLATE) |
| `studio/07_Repository/TEMPLATES/QA_REVIEW_TEMPLATE.md` | Reusable QA finding template aligned with Handbook v1 §21 (`QA-[ID]`, severity, confidence, evidence, governing source, consequence, owner role, recommended action, status). | ④ | — (TEMPLATE) |
| `studio/07_Repository/TEMPLATES/DECISION_ENTRY_TEMPLATE.md` | Reusable decision-log entry template matching `DECISION_LOG.md`'s exact table columns. | ④ | — (TEMPLATE) |
| `studio/07_Repository/PROMPT_LIBRARY.md` | Pointer index (not a copy) locating every proven-prompt/recipe appendix already in the repo, with anchors, contents summary, and usage rules. States the single-source/no-duplication rule explicitly. | ④ | — (POINTER INDEX) |
| `studio/07_Repository/ARCHIVE/README.md` | Archive policy: what gets archived, archive-don't-delete law, required metadata for archived items, current state (empty at creation). | ④ | — (POLICY RECORD) |
| `studio/07_Repository/REFERENCES/PMU_style/INDEX.md` **(new, OPS-0002 ④)** | PMU Style Reference Library index — REFERENCE-ONLY banner (`Art_Direction.md` DEC-0003/DEC-0004 remains MASTER; no panel copying/tracing); library is Drive-resident (zero image bytes, zero Drive ids/links in-repo by licensing decision — residency ruling queued as DEC-0015); §A 28-strip reviewed shortlist w/ SHA-256 provenance + §B full named inventory (85 story strips of 357 folder items). | ④ | — (REFERENCE-ONLY pointer index; never canon) |

## `manuscript/` — narrative canon (owner: ②)

| Path | Purpose | Owner | SOURCE_OF_TRUTH class |
|---|---|---|---|
| `manuscript/bible/story_bible.md` | Running lore canon file — MIXED content per `SOURCE_OF_TRUTH.md`: FRANCHISE_CANON sections (logline, chronology, core rules, 10.0 system, 9.0 world, cast, keepsakes, fight doctrine, tone/guardrails, Volume 1 arc) interleaved with HISTORICAL_RECORD/SUPERSEDED production notes (art-era iteration chain, strip-doctrine measurements, publication logs). Section-level classification proposed (not yet applied in-file) in `story_bible_tagging_proposal.md` above — do not treat this file wholesale as active canon until that proposal is approved. | ② | `MIXED: FRANCHISE_CANON + HISTORICAL_RECORD/SUPERSEDED` (per SOURCE_OF_TRUTH.md; section tagging = TASK-0004) |
| `manuscript/chapters/00_prologue.md` | "The Red Desert" — the 8.0→9.0 patch prologue, exact canonical prose text. | ② | `MANUSCRIPT_CANON` |
| `manuscript/chapters/01_the_ninth_world.md` | Chapter 1 — the present-day (9.0) opening chapter, exact canonical prose text: sparring hall, Si-woo's dream leak, Cha's noodle shop, the keepsake case, Ha-eun's library scene, the doubled moon-skip cliffhanger. | ② | `MANUSCRIPT_CANON` |
| `manuscript/manhwa/ep1_v3_script.md` | EP.1 v3 manhwa script — 58-panel beat breakdown with narration/thought/speech/system-text markup. Per `SOURCE_OF_TRUTH.md`, dialogue wording here is **superseded by the published readers'** wording wherever they disagree (confirmed in ~a dozen lines by the variance record below). | ② | `ADAPTATION_CANON` (beats — dialogue superseded by readers' wording) |
| `manuscript/manhwa/ep1_adaptation_variance.md` **(new, CYCLE-0001)** | Beat-by-beat comparison table: prose canon (Prologue + Ch.1) vs. EP.1 manhwa adaptation (script + both published readers), using the six-class variance vocabulary (SAME_EVENT/COMPRESSED/REORDERED/ADDED_IN_ADAPTATION/OMITTED_FROM_ADAPTATION/DIALOGUE_REWORDED). Confirms the readers-supersede-script precedence rule in practice; documents Ha-eun's Ch.1 thread deferral to EP.2 as the largest single omission; surfaces several texture/continuity flags (callus-hand mention, "Attendance: perfect," a well-callback asymmetry, an 11:58→"Midnight" numeric softening) for ⑤/③ attention. Produced by TASK-0008; QA-04 wording correction applied CYCLE-0002 (②, gate-verified). | ② | — (RECORD/comparison, ACCEPTED — not itself a canon source, describes two canon sources) |

## `readers/` — published derivative outputs (owner: ③)

| Path | Purpose | Owner | SOURCE_OF_TRUTH class |
|---|---|---|---|
| `readers/episode1_part1.html` | Published EP.1 Part 1 reader (cold open through the 8.0→9.0 rewrite and Han's arrival in Haeseong). Current published wording for this half of EP.1 lives here — this is the highest-precedence text source for EP.1 Part 1 dialogue per `SOURCE_OF_TRUTH.md`'s precedence rule. | ③ | `DERIVATIVE OUTPUT` |
| `readers/episode1_part2.html` | Published EP.1 Part 2 reader (noodle shop through the academy sparring scene, Si-woo's dream, and the rooftop moon-skip cliffhanger). Same precedence note as Part 1. | ③ | `DERIVATIVE OUTPUT` |

---

## Notes on this index

- **Not indexed here (by design):** `studio/06_Operations/REVIEWS/.gitkeep` and `studio/06_Operations/WORK_IN_PROGRESS/.gitkeep` are empty git placeholder files with no content to summarize; their parent directories are listed above instead.
- **Off-repo dependencies** (not indexed above because they are not tracked files in this repository, but relevant to complete navigation): the uncut 22-section Master Project Bible (platform document `cmrr0f9vr0bg907ade7vvxsnd`), the sealed twist bank (`manuscript/bible/twist_bank_PRIVATE.md`, intentionally off-repo per DEC-0002/Q-12), platform-hosted LOCKED asset images and published-reader binaries (see I-0001), and creator's Drive-hosted PMU reference pages (copyrighted, analysis-only, never to be committed — now text-indexed in-repo at `studio/07_Repository/REFERENCES/PMU_style/INDEX.md`, library itself Drive-resident, residency ruling queued as DEC-0015). Full off-repo orientation: `studio/06_Operations/HANDOFFS/THREAD_RETIREMENT.md`.
- **This index will drift** the moment any new file is added or any file is renamed/moved. Per Handbook Amendment 1 §A1.2, ④ may make meaning-safe mechanical fixes to this index (and other repo-wide navigation) anywhere in the repository at any time. Last refresh: CYCLE-0002 ④ (TASK-0019), which confined its writes to `studio/07_Repository/**` + `OPEN_QUESTIONS.md` (task-authorized Q-15–Q-18 exception) + its own handoff note; mechanical-fix candidates outside that lane remain logged, not fixed, in `HANDOFFS/CYCLE-0001-REPO.md` and `HANDOFFS/CYCLE-0002-REPO.md`.

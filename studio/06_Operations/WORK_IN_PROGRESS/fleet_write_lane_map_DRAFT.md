# Fleet Write-Lane Map — 27-Department Proposal for patch-10.0

> ## ⚠️ DRAFT PROPOSAL — THIS DOCUMENT DECIDES NOTHING
> This is a **proposal only**. It grants no lane, moves no custody, resolves no open item, and changes no enforcement. Until the Owner adopts a 27-lane map **via a future Handbook amendment**, the binding rule remains Handbook **§A4.5** (interim carry-over of the §A1.2 five-role lanes by closest-role equivalence). Every open item below (OQ-IA-1 … OQ-IA-8) is the **Owner's** to rule on. Nothing in this file may be cited as authority for a write.

- **Status:** DRAFT PROPOSAL (night-safe additive) · **Task:** TASK-0029 (P2, CYCLE-0005) · **Author:** Information Architecture Agent (DEPT-003) · **Date:** 2026-07-20 (UTC+8)
- **Origin:** Handbook Amendment 4 §A4.5 requires a formal 27-lane map "proposed by the Information Architecture Agent and Owner-approved." QA finding **QA-248** (S4, `REVIEWS/FLEET-CYCLE-0001_REVIEW.md` §(h)) flagged that no task tracked that follow-through; the EP minted TASK-0029 (`TASK_QUEUE.md`, TASK-0029 row). This file is that deliverable.
- **Write lane of this dispatch:** this one new file (plus a handoff note in `HANDOFFS/`). No ledger edits; the EP records completion.

---

## 1. Sources and derivation method

**Sources (all read in full for this proposal; none derived from memory):**

| Key | Source |
|---|---|
| `HB` | `studio/00_OPERATING_HANDBOOK.md` at base commit — cited by section (A1.1, A1.2, A1.3, A1.4, A2.4, A3.5, A4.3, A4.4, A4.5; v1 body §3.1, §5, §6, §12) |
| `A1.2-①…⑤` | The five legacy lane grants in HB §A1.2, per role |
| `D-0NN` | Department contract `studio/departments/DEPT-0NN-<name>.md` in `lycacallenero55-cpu/Patch-10.0-Production-Operating-System` at ref `7aa331f071952de80d0a7d2e5354cafddcc87201` (all 27 read; DEPT-001..DEPT-027, no gaps) |
| `TREE` | The patch-10.0 tree as it exists at base commit `c17c78c10e25116a68c8f05ed0d7ce42242fae74` (walked in full) |
| `TQ` | `studio/06_Operations/TASK_QUEUE.md` (row-level citations) |
| `DL` | `studio/06_Operations/DECISION_LOG.md` (DEC-level citations) |
| `FR` | `studio/06_Operations/REVIEWS/FLEET-CYCLE-0001_REVIEW.md` (section-level citations) |
| `SOT` | `studio/06_Operations/SOURCE_OF_TRUTH.md` (PROPOSED register; DEC-0008 pending) |

**Derivation rule (per the Work Order and §A4.5):** each department's proposed lane = the legacy five-role grant (§A1.2) that its contracted ownership most closely continues, narrowed to the artifacts its contract actually owns, and mapped onto paths that exist at the base commit. **Where two contracts continue the same legacy grant, or no contract clearly continues it, the row is CONTESTED or UNASSIGNED and carries an OQ-IA item — not a resolution.**

**Load-bearing observation:** none of the 27 contracts names a literal patch-10.0 path (verified across all 27; repository language in the contracts is generic — "repository updates," "repository-visible," "archive procedure"). Equivalence below is therefore **functional** (what the contract owns) rather than textual (a path the contract names). This is why several files with split function (content vs. custody) produce open items rather than clean rows.

**Precedent for split authority:** §A1.2 itself splits `studio/01_Lore/Master_Project_Bible.md` — "② holds content authority; ④ holds custodial/registry authority." The map below reuses that content/custody distinction wherever one file serves two functions.

---

## 2. The map — proposed standing write lanes, DEPT-001 … DEPT-027

**Reading the table:**
- **STANDING** = a proposed standing write lane over named paths. **SHARED-ONLY** = no standing production lane; the department writes only through the shared/custodial lanes of §3 (its own `HANDOFFS/` note; `WORK_IN_PROGRESS/` DRAFT deliverables when a Work Order assigns them). "No production write lane" is a valid, expected answer — most support and source-design roles deliver through review-gated handoffs, not standing file custody.
- **CONTESTED / UNASSIGNED → OQ-IA-n** = the legacy grant has no single clear successor; the interim §A4.5 reading governs day-to-day (EP dispatches must name such files explicitly) until the Owner rules.
- A lane grant is **never** an edit authorization by itself — see Rule R9 (§4).

| Dept | Fleet agent | Proposed standing write lane (patch-10.0) | Ancestry → rationale | Sources |
|---|---|---|---|---|
| DEPT-001 | Executive Producer | Root `README.md`; `studio/00_OPERATING_HANDBOOK.md` + `studio/00_STUDIO_RULES.md` (governance recordings **only under explicit Owner authorization per commit** — see R5 precedent); ops ledgers jointly with DEPT-002 (§3.1) | A1.2-① carried over; A4.5 names EP for ops-ledger custody; EP "writes no canon, no art, performs no QA" (A1.1) and its contract owns direction/approvals, not content | A1.2-①; A4.5; A1.1; D-001; TQ:TASK-0025; FR §(a) |
| DEPT-002 | Production Operations | Ops ledgers jointly with DEPT-001 (§3.1): `TASK_QUEUE.md`, `STUDIO_STATUS.md`, `DECISION_LOG.md`, `OPEN_QUESTIONS.md`, `CHANGELOG.md` (+ operational registers it owns by contract: queues, blocker/dependency registers, all inside `studio/06_Operations/`) | A1.2-① (06_Operations) via A4.5, which names Production Operations alongside EP; contract owns "Work Order operations; Production queues; Status tracking; Blocker registers; Dependency registers" | A1.2-①; A4.5; D-002; TREE: `studio/06_Operations/` |
| DEPT-003 | Information Architecture | `studio/07_Repository/INDEX.md` · `studio/07_Repository/TEMPLATES/` · `studio/07_Repository/ARCHIVE/` (structure, templates, archive rules — records, never specialist substance) | A1.2-④ structural instruments; contract owns "Repository structure standards … Archive rules; Structural integrity reviews; Single-source-of-truth placement rules"; ④'s roving mechanical-fix license is **not** claimed here — parked in OQ-IA-8 (self-interest disclosed: this author) | A1.2-④; D-003; TREE: `studio/07_Repository/` |
| DEPT-004 | Quality Assurance | `studio/06_Operations/REVIEWS/` (own review files, one per review — §3.2) · `studio/06_Operations/INCIDENTS.md` | A1.2-⑤; contract owns "Review outcomes; Review records; Defect reports"; INCIDENTS was a named ⑤ file | A1.2-⑤; D-004; TREE; FR (as practice) |
| DEPT-005 | Release Certification | **No standing lane at base commit.** Certification/readiness records have no existing home; interim: per-WO placement. → **OQ-IA-6** | No legacy release lane exists (no releases yet); contract owns "Release certification records; Milestone closure certification" — review-family records with nowhere standing to live | D-005; TREE (no release path); OQ-IA-6 |
| DEPT-006 | Lore | `manuscript/bible/story_bible.md` (content custody; mixed file — see SOT row; TASK-0004 tagging remains gated) · `studio/01_Lore/Master_Project_Bible.md` (**content authority half** of the A1.2 split; custodial half → OQ-IA-3). **All semantic canon edits remain blocked pending DEC-0008** | A1.2-② (bible-level canon) + A1.2's MPB content/custody split; contract owns "Canon facts; Lore records; Timeline truth; Universe rules; Terminology authority" | A1.2-②; A1.2-MPB bullet; D-006; SOT; DL:DEC-0008 |
| DEPT-007 | Narrative Design | **No standing lane.** Outlines/beat sheets/scene briefs are WO-scoped DRAFT deliverables (`WORK_IN_PROGRESS/`, precedent `ep2_outline_proposal.md`); no canonical home exists for narrative-design artifacts. → **OQ-IA-7** | A1.2-② covered narrative work product implicitly; contract owns "Story structure; Narrative arcs; Beat outlines" — none has a standing file at base commit | D-007; TREE: `studio/06_Operations/WORK_IN_PROGRESS/ep2_outline_proposal.md`; TQ:TASK-0017; OQ-IA-7 |
| DEPT-008 | Character | **No standing lane.** Character identity records live inside Lore-custody files (MPB; `CANON_REGISTRY.md` §1; story_bible Cast) → **OQ-IA-7** | Contract owns "Character identity records; Relationship records" but those records are sections of files custodied elsewhere | D-008; TREE; OQ-IA-7 |
| DEPT-009 | Worldbuilding | **No standing lane.** Location/culture/institution records live inside Lore-custody files → **OQ-IA-7** | Contract owns "Location records; Culture records; Institution records"; same placement condition as DEPT-008 | D-009; TREE; OQ-IA-7 |
| DEPT-010 | Power System | **No standing lane.** Power rules live inside Lore-custody canon files; the VFX **expression** of power rules lives in `studio/02_Art/Effects_Bible.md` (custody contested → OQ-IA-4, DEPT-010 is a named stakeholder) → **OQ-IA-7**, OQ-IA-4 | Contract owns "Power rules; Ability records; Limitations; Costs" (canon), and explicitly does **not** own "Visual effects rendering" | D-010; TREE; OQ-IA-4; OQ-IA-7 |
| DEPT-011 | Novel Production | `manuscript/chapters/` (chapter/scene prose, revision packages) | A1.2-② (chapters) by direct continuation; contract owns "Novel drafts; Chapter manuscripts; Scene prose" | A1.2-②; D-011; TREE: `manuscript/chapters/` |
| DEPT-012 | Manhwa Production | `manuscript/manhwa/` (episode scripts, adaptation records — see row note N-012) · `readers/` (published episode readers as manhwa production packages) | A1.2-② (manhwa scripts) + A1.2-③ (readers) split by contracted function; contract owns "Manhwa episode plans; Panel sequences; Page-flow decisions; Manhwa production packages" | A1.2-②; A1.2-③; D-012; TREE; SOT (readers = derivative outputs) |
| DEPT-013 | Anime Production | **No standing lane at base commit.** No anime artifact exists in the tree; deliverables are WO-scoped until a home is assigned at adoption | Contract owns "Anime episode plans; Animation production packages" — no current path continues ③ for anime specifically | D-013; TREE (no anime path) |
| DEPT-014 | Storyboard | `studio/04_Storyboards/` — **primary claimant under closest-role equivalence** (folder-function match), but custody is CONTESTED with DEPT-012 and DEPT-017 → **OQ-IA-1** | A1.2-③ (storyboards); contract owns "Storyboard boards; Shot plans; Camera intent records" | A1.2-③; D-014; D-012; D-017; TREE; OQ-IA-1 |
| DEPT-015 | Character Art | `studio/02_Art/Character_Bible.md` · `studio/02_Art/Kit_Specs_DRAFT.md` (character visual references, model sheets, kit specs) | A1.2-③ narrowed to character-visual files; contract owns "Character visual references; Model sheets; Costume design records"; Kit_Specs is character-kit content (TASK-0007) | A1.2-③; D-015; TREE; TQ:TASK-0007 |
| DEPT-016 | Environment Art | `studio/02_Art/Environment_Bible.md` (environment references, background standards) | A1.2-③ narrowed to environment-visual files; contract owns "Environment visual references; Location concept sheets; Background standards" | A1.2-③; D-016; TREE |
| DEPT-017 | Cinematic Production | **No standing lane pending OQ-IA-1.** Strong contract claim on the two trailer files in `04_Storyboards/` ("Cinematic shot packages; Trailer sequence plans") and on `05_Production/Video_Workflow.md` (→ OQ-IA-5) | ③'s trailer work product is genuinely split between the Storyboard and Cinematic contracts | D-017; TREE: `studio/04_Storyboards/Trailer_v2_*`; OQ-IA-1; OQ-IA-5 |
| DEPT-018 | Marketing | **No standing lane.** No marketing artifact or folder exists at base commit; outputs are WO-scoped DRAFTs pending an assigned home at adoption | Contract owns audience-facing copy/briefs; no legacy lane or current path corresponds | D-018; TREE (no marketing path) |
| DEPT-019 | Research | **No standing lane** (pure-advisory). Research briefs/reference packs are WO-scoped; contract routes placement through Information Architecture ("reference placement") | Advisory support role; no legacy lane analogue | D-019 |
| DEPT-020 | Prompt Engineering | `studio/07_Repository/PROMPT_LIBRARY.md` (prompt assets, instruction templates) | A1.2-④ held the file; the **contracted function** ("Prompt assets; Instruction templates; Reusable execution patterns") continues in DEPT-020 — the cleanest single-file equivalence in the map | A1.2-④; D-020; TREE |
| DEPT-021 | Asset Management | **No standing lane pending OQ-IA-2.** Strong contract claim on `studio/03_Assets/Asset_Registry.md` ("Asset inventory records; Asset metadata; Version tracking") and `studio/07_Repository/REFERENCES/` ("Reference package organization … managed libraries") — both custody questions are CONTESTED with legacy-③/④ successors | The Work Order itself names this conflict; resolving it is the Owner's | D-021; A1.2-③; A1.2-④; TREE; OQ-IA-2 |
| DEPT-022 | Automation | **No standing lane.** No scripts/tooling path exists in patch-10.0 at base commit; validation outputs support reviews but Automation is not a review agent | Contract owns "Automation scripts; Validation routines" — no corresponding path; repo-side tooling home is an adoption-time question, not claimed here | D-022; TREE (no tooling path) |
| DEPT-023 | Knowledge Management | **No standing lane pending OQ-IA-3.** Strong contract claim on the custodial/registry function (`CANON_REGISTRY.md`; MPB custodial half): "Knowledge records; Dependency maps; Derived-output relationship records" — contested with DEPT-006 (canon substance) and DEPT-003 (structure) | ④'s "manages canon RECORDS … never authors canon CONTENT" function has three partial successors | D-023; D-006; D-003; A1.2-④; A1.2-MPB bullet; OQ-IA-3 |
| DEPT-024 | Canon Review | `studio/06_Operations/REVIEWS/` — own review files, one per review (§3.2) | A1.2-⑤ review family; contract owns "Canon review reports; Canon pass and fail decisions" | A1.2-⑤; D-024 |
| DEPT-025 | Visual Review | `studio/06_Operations/REVIEWS/` — own review files, one per review (§3.2) | A1.2-⑤ review family; contract owns "Visual review reports; Visual pass and fail decisions" | A1.2-⑤; D-025 |
| DEPT-026 | Technical QA | `studio/06_Operations/REVIEWS/` (own review files, §3.2) · `studio/06_Operations/VALIDATION_PROFILE.md` | A1.2-⑤; VALIDATION_PROFILE was a named ⑤ file and the contract owns "Validation checklists; Automation validation notes"; precedent: TQA already writes REVIEWS/ (`FLEET-CYCLE-0001_TECH.md`) | A1.2-⑤; D-026; TREE; TQ:TASK-0028 |
| DEPT-027 | Continuity Review | `studio/06_Operations/REVIEWS/` (own review files, §3.2) · `studio/06_Operations/CONTINUITY_LEDGER.md` | A1.2-⑤; CONTINUITY_LEDGER was a named ⑤ file; contract owns "Continuity review reports; … Cross-output comparison notes" | A1.2-⑤; D-027; TREE |

**Row notes:**

- **N-001 (Handbook/RULES custody):** Handbook text changes are Owner-ruled amendments; the EP lane here is the *recording* function only, exercised per explicit authorization each time — exactly the TASK-0025 pattern ("Lane: ops ledgers + Handbook governance only", TQ:TASK-0025; verified FR §(a), §(b) check 8). This proposal does not widen it.
- **N-006/N-012 (content vs. file custody):** `manuscript/manhwa/ep1_adaptation_variance.md` was authored under legacy ② as a Lore-verified variance record (TQ:TASK-0008). Proposed reading: DEPT-012 holds file custody with `manuscript/manhwa/`; canon-variance *statements* inside it remain Lore-department substance under the adaptation-label law (HB §3.2). The MPB content/custody split (A1.2) is the precedent for this kind of split; it does not need a new mechanism.
- **N-review (one file per review):** review agents write **new** review files under `REVIEWS/` and never edit ledgers; the EP records verdicts (TQ:TASK-0027 and TASK-0028 rows: "no ledger edits (EP records verdict)"; FR write-lane recital).
- **Coverage check:** every path in the base-commit tree appears exactly once in this map as STANDING (table above), SHARED/CUSTODIAL (§3), or CONTESTED/UNASSIGNED (§5). No path is left silent.

**Shape summary:** 15 departments carry a proposed standing write lane (001, 002, 003, 004, 006, 011, 012, 014, 015, 016, 020, 024, 025, 026, 027); 12 carry none at base commit (005, 007, 008, 009, 010, 013, 017, 018, 019, 021, 022, 023 — several with active claims parked in OQ-IA items). All 27 retain the shared lanes of §3 when dispatched.

---

## 3. Shared and custodial lanes (`studio/06_Operations/`)

### 3.1 Ops ledgers — custody: Executive Producer + Production Operations

`TASK_QUEUE.md` · `STUDIO_STATUS.md` · `DECISION_LOG.md` · `OPEN_QUESTIONS.md` · `CHANGELOG.md` — held jointly by DEPT-001/DEPT-002 per §A4.5 ("the operations ledgers (`studio/06_Operations/**`) are held by the Executive Producer Agent / Production Operations Agent"). **Change from the legacy shared model:** §A1.2 let any department append to `TASK_QUEUE.md`/`OPEN_QUESTIONS.md` during its own turn; under §A4.5 and current fleet practice, other agents do **not** edit ledgers — requests, completions, and cross-department questions travel via the agent's handoff and Work Order report, and the EP/Ops record them (TQ:TASK-0027/0028/0029 rows: "no ledger edits (EP records)"). Q-numbers are minted only in `OPEN_QUESTIONS.md` by its custodians — which is why this file uses file-local OQ-IA numbering.
Also under EP/Ops custody as 06_Operations residents (A1.2-① residue): `SOURCE_OF_TRUTH.md` (register **content** approval is the Owner's — DEC-0008 PENDING, DL) and `INCIDENTS.md`/`CONTINUITY_LEDGER.md`/`VALIDATION_PROFILE.md` **excepted** to their §A1.2-⑤ successor rows above (004/027/026).

### 3.2 `REVIEWS/` — the review agents

Writers: Quality Assurance (004), Canon Review (024), Continuity Review (027), Visual Review (025), Technical QA (026). Discipline: **one file per review**, named for the reviewed unit (`CYCLE-NNNN_REVIEW.md`, `FLEET-CYCLE-NNNN_REVIEW.md`, `FLEET-CYCLE-NNNN_TECH.md`, `CYCLE-NNNN_GATE-<dept>.md` patterns in TREE); review files double as the turn's record; **no ledger edits** (verdicts recorded by EP). Sources: A1.2-⑤; A3.3 (output path); TQ:TASK-0027/0028; FR §(a). Whether Release Certification (005) becomes a sixth `REVIEWS/` writer or gets its own home is **OQ-IA-6**.

### 3.3 `HANDOFFS/` — the writing department's own handoffs

Any dispatched agent writes **its own** handoff note here, named for the task or cycle (`CYCLE-<n>-<dept>.md` per A1.4.4; fleet-era task pattern `TASK-NNNN-<abbr>.md`, e.g. `TASK-0026-OPS.md` in TREE), using `studio/07_Repository/TEMPLATES/TURN_HANDOFF_TEMPLATE.md`. A handoff is a record of the writer's own turn — never an edit to another agent's note.

### 3.4 `WORK_IN_PROGRESS/` — DRAFT deliverables per Work Order

The department that owns a Work Order writes its DRAFT deliverable(s) here, banner-labeled, decision-free. Precedents in TREE: `story_bible_tagging_proposal.md` (②, TQ:TASK-0004), `ep2_outline_proposal.md` (②, TQ:TASK-0017), `professor_im_investigation_DRAFT.md` (②, TQ:TASK-0024), `owner_decision_portfolio_DRAFT.md` (Ops, TQ:TASK-0026) — and this file (TQ:TASK-0029). WIP placement is per-WO and implies no standing custody of the folder.

---

## 4. Rules of the road (carry-forward, restated for 27 lanes)

- **R1 — Single writer per file per turn.** One agent's dispatch writes a given file at a time; fleet commits chain linearly (A1.3 "One department writes to the repository per turn"; v1 §6 "One writer prevents Git merge conflicts"; verified fleet practice FR §(a) — strictly linear, sole-parented chain).
- **R2 — Read at HEAD before write.** Sync first: `STUDIO_STATUS.md`, `CHANGELOG.md`, `TASK_QUEUE.md`, `OPEN_QUESTIONS.md`, newest `HANDOFFS/` note, and every file the task touches; "Trust commits, never memory" (A1.4.1; v1 §3.1, §12). Status records cite the base HEAD the turn built against, never the turn's own commits (QA-12 discipline, FR §(b) check 5). A push rejection means concurrent activity: stop, re-fetch, reconcile as a new bounded task (v1 §12).
- **R3 — `CHANGELOG.md` is pure-append.** Each revision is a byte-exact prefix of the next; past entries are never edited, superseded expectations are noted in *new* entries (append-only law: FR §(b) check 2 — verified byte-exact prefix property; FR §(h) QA-248 "No edit to the past entry (append-only law)").
- **R4 — Night Rules ride on top of every lane.** During unattended runs: additive DRAFT only — no LOCKs, no canon retcons, no repository restructures; anything needing Owner approval is QUEUED, never decided (A2.4, carried forward by A3.5 and A4.4). At night a standing lane narrows to *additive DRAFT within the lane*; a lane grant never overrides a night rule.
- **R5 — Lane exceptions are explicit, per Work Order, and declared.** An out-of-lane write is legal only when the Work Order names the exact file(s), and the writer declares the touch in its handoff/manifest and commit message. **House precedent:** TASK-0025 — queue row granted "Lane: ops ledgers + Handbook governance only" (TQ:TASK-0025); the Handbook touch outside the ops-ledger lane was dispatch-authorized, declared in the manifest (`HANDOFFS/TASK-0026-OPS.md`), and QA-verified as in-lane-by-authorization with deviations adjudicated (FR §(a), §(b) check 8, §(f)).
- **R6 — Attribution.** Every commit is tagged `[AGENT:<Name>]` (A4.3) and closes with a touches-only line listing exactly the files written (house practice verified FR §(a): "closing touches-only line that matches the actual per-commit file footprint").
- **R7 — Labels and approval.** DRAFT → IN REVIEW → APPROVED → LOCKED (+ DEPRECATED, UNDECIDED); **only the Owner approves or LOCKs**; UNDECIDED items live in `OPEN_QUESTIONS.md` under its custodians (A1.4.5).
- **R8 — Outside your lane is read-only.** Cross-lane needs travel via your handoff and the EP/Ops dispatch loop — never direct edits (A1.2 closing bullet; A1.4.2, as modified by §A4.5 ledger custody — see §3.1).
- **R9 — A lane is not an edit authorization.** Standing blocks ride on top of every lane: DEC-0008 gates all semantic canon edits (DL; SOT banner); asset-lock law (HB §3.3) gates locked-asset changes; per-item Owner approvals gate what their rows say they gate (TQ); v1 §12 branch policy defaults substantive multi-file/semantic work to a branch + PR. A lane says *where* an agent may write when authorized — the Work Order and standing law say *whether*.

---

## 5. Conflicts and gaps — file-local open items (Owner's to rule; **no resolutions proposed; no Q-numbers minted**)

> Numbering note: items below are file-local `OQ-IA-n` identifiers, exactly as the TASK-0029 dispatch requires ("open items as file-local OQ-IA-n (no Q-numbers)"). They collide with nothing in `OPEN_QUESTIONS.md`; if the Owner wants any of them tracked as official questions, the EP/Ops mint Q-numbers in that ledger.

### OQ-IA-1 — `studio/04_Storyboards/` custody: three overlapping claims
- **Conflict:** DEPT-014 Storyboard ("Storyboard boards; Shot plans; Blocking notes; Camera intent records"), DEPT-017 Cinematic Production ("Cinematic shot packages; Trailer sequence plans" — both current files in the folder are trailer artifacts: `Trailer_v2_Storyboard.md`, `Trailer_v2_KF_Production_Plan.md`), and DEPT-012 Manhwa Production ("Panel sequences; Page-flow decisions") each contractually continue part of the ③ storyboard function. (D-014; D-017; D-012; A1.2-③; TREE.)
- **Options:** (a) DEPT-014 holds the folder; 012/017 contribute through it per WO. (b) Per-artifact custody: boards → 014, trailer/cinematic packages → 017, manhwa panel plans → 012's own lane (`manuscript/manhwa/`), leaving 04_Storyboards to 014+017 by file. (c) 014 as sole writer with 012/017 as required consulted reviewers per WO.

### OQ-IA-2 — Asset registry and reference libraries: DEPT-021 vs. legacy-③/④ successors
- **Conflict:** `studio/03_Assets/Asset_Registry.md` sat in the ③ lane (A1.2-③) whose successors here are the art departments (015/016), but DEPT-021's contract owns exactly the registry function ("Asset inventory records; Asset metadata; Asset status records; Version tracking"). Likewise `studio/07_Repository/REFERENCES/` sat in ④'s layer but matches DEPT-021's "Reference package organization … managed libraries." Locks themselves are Owner acts either way (HB §3.3). (D-021; D-015; D-016; A1.2-③; A1.2-④; TREE; TQ:TASK-0020.)
- **Options:** (a) DEPT-021 custodies both (registry mechanics + reference indexes); art departments propose entries via WO. (b) Art departments keep §A1.2-③ equivalence for `Asset_Registry.md` (each for its asset classes) and 021 custodies only `REFERENCES/`. (c) Status quo interim: both files ride explicit WO naming until adoption.

### OQ-IA-3 — Canon records custody: `CANON_REGISTRY.md` and the MPB custodial half
- **Gap:** legacy ④ "manages canon RECORDS and their labels; never authors canon CONTENT" (A1.1) and held `CANON_REGISTRY.md` plus the MPB custodial half (A1.2-④; A1.2-MPB bullet). No single fleet contract continues that custodial function: DEPT-023 owns record-keeping ("Knowledge records; Dependency maps; Derived-output relationship records") but "does not own … Folder taxonomy" and may not "Declare new canon"; DEPT-006 owns canon substance but not registry custody as such; DEPT-003 owns structure/metadata standards but must not own specialist content. (D-023; D-006; D-003; A1.2-④.)
- **Options:** (a) DEPT-023 custodies registry mechanics; DEPT-006 remains substance authority (MPB-style split, A1.2 precedent). (b) DEPT-006 takes both halves (single canon lane). (c) Registry custody stays EP-dispatched per WO until the registry's own completeness debt is worked off.

### OQ-IA-4 — Unowned visual-law files in `studio/02_Art/`
- **Gap:** `Art_Direction.md` (cross-cutting visual law) and `Effects_Bible.md` (VFX grammar) have no single contract successor: DEPT-015/016 own character/environment references respectively; DEPT-010 owns power **rules** but explicitly not "Visual effects rendering"; no "art direction" department exists among the 27. `Trailer_v2_Gap_Specs_DRAFT.md` compounds this: its parts span environment plates (016), monster/extinction design (015/canon-adjacent), and registry-card UI (no clear owner). (D-015; D-016; D-010; TREE; TQ:TASK-0018/0021/0022.)
- **Options:** (a) Joint 015+016 custody of `02_Art/` with per-file split and named-stakeholder consultation (010 for Effects_Bible). (b) Owner designates one art department as visual-law custodian. (c) Visual-law files ride explicit WO naming only, until an adoption-time assignment.

### OQ-IA-5 — `studio/05_Production/` workflow specs custody
- **Gap:** `Image_Workflow_QA.md` and `Video_Workflow.md` are production-workflow law from the ③ lane; candidate successors each hold only a slice: DEPT-017 (video/cinematic execution), DEPT-015/016 (image generation standards), DEPT-020 (reusable execution patterns), DEPT-026 (validation checks embedded in the QA workflow doc). (A1.2-③; D-017; D-015; D-016; D-020; D-026; TREE.)
- **Options:** (a) Split by medium: `Video_Workflow.md` → 017; `Image_Workflow_QA.md` → 015+016 jointly. (b) Treat both as production law under EP custody (governance recordings, like 00_-level docs). (c) WO-named custody until adoption.

### OQ-IA-6 — Release Certification records have no home
- **Gap:** DEPT-005 produces "Release certification records; Milestone closure records; Release readiness reports" — no such path exists at base commit, and the §3.2 custodial spec names five review agents for `REVIEWS/`, not six. (D-005; TREE.)
- **Options:** (a) Admit 005 to `REVIEWS/` as a sixth review-family writer (one file per certification). (b) Create a dedicated home at adoption (e.g., a certification folder under `studio/06_Operations/`) — a restructure, so Owner-gated and never a night action. (c) Certification records land in `WORK_IN_PROGRESS/` per WO and are filed by EP/Ops.

### OQ-IA-7 — Source-designer records (DEPT-007/008/009/010) live inside files custodied elsewhere
- **Gap:** narrative outlines, character identity records, world records, and power rules — the contracted property of 007/008/009/010 — currently exist only as sections of Lore-custody files (MPB, `story_bible.md`, `CANON_REGISTRY.md` §§) or as WO-scoped WIP drafts. These departments therefore hold **no standing lane** while owning the substance of records they cannot write standing. All semantic canon edits are DEC-0008-gated regardless. (D-007; D-008; D-009; D-010; TREE; SOT; DL:DEC-0008.)
- **Options:** (a) Keep substance-through-Lore: 007–010 deliver via WO drafts; 006 (or the OQ-IA-3 custodian) integrates. (b) At adoption, assign per-domain record files/sections with named sectional custody (a structural change; Owner-gated). (c) Sectional custody inside existing files without new files (MPB-split precedent applied per section).

### OQ-IA-8 — Successor of ④'s roving "meaning-safe mechanical fixes anywhere" license
- **Gap:** A1.2-④ granted repo-wide mechanical fixes ("links, formatting, index rows … cannot change meaning"). No fleet contract inherits a roving cross-lane write license, and this author (DEPT-003) **declines to claim it unilaterally in its own proposal** — self-interest disclosed; current practice already leaves such fixes to the next authorized touch of the owning lane (FR §(h) QA-249 disposition). (A1.2-④; D-003; D-026; FR.)
- **Options:** (a) Retire the roving license; mechanical fixes ride the owning lane's next authorized WO (current de-facto practice). (b) Assign a narrow structure-only version (links/index rows/cross-references, never wording) to DEPT-003, each use declared per R6. (c) Assign detection to DEPT-026 (flags) with fixes always returned to the owning lane.

---

## 6. Follow-on notes (non-normative; nothing here is actioned by this file)

- `studio/07_Repository/INDEX.md` ownership labels predate the governance transfer (all fleet-era commits to date touch only `studio/06_Operations/**` and the Handbook — FR §(a)); a mechanical label refresh naturally rides the adoption Work Order.
- Per QA-248's own recommendation (FR §(h)), the CHANGELOG line forecasting that Amendment 4 would "formalize" the map is superseded by the TASK-0029 route; recording that supersession in a new CHANGELOG entry is EP-lane work, not this file's.
- Adoption path (for the Owner's convenience, not a decision): review this proposal → rule on OQ-IA-1…8 (in any order; each is independent) → adopt via Handbook amendment (Owner-gated, out of this Work Order's scope) → EP schedules the INDEX/label refresh and any structural follow-ons. Until then, §A4.5 interim carry-over remains the binding rule.

---

*Information Architecture Agent (DEPT-003) · TASK-0029 · proposal records only: no lane granted, no custody moved, no canon touched, no lock, no retcon, no UNDECIDED item resolved, no Q-number minted, no ledger edited, no off-repository identifiers reproduced. Touches ONLY `studio/06_Operations/WORK_IN_PROGRESS/fleet_write_lane_map_DRAFT.md`.*

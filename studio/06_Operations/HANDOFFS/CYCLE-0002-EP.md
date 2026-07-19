# Turn Handoff — CYCLE-0002-① (Executive Producer)
- **Date:** 2026-07-19 · **Mode:** Conductor Mode with QA gates (Amendment 2), Owner-ordered · **Night rules in force** (§A2.4) · **Base commit:** 8c397dd

## Cycle plan
Order: ① (this turn) → ② → ⑤ GATE(②) → ③ → ⑤ GATE(③) → ④ → ⑤ GATE(④) → ① report → Owner.
Scoping rationale: DEC-0008 still PENDING and night rules apply, so every assignment is additive DRAFT/record work — no canon edits, no locks, no generation, no restructures. Decisions surfaced by the work are QUEUED for the Owner (TASK_QUEUE/DECISION_LOG/OPEN_QUESTIONS), never made.

## Assignments
- **② Lore (one commit):** (a) TASK-0008 correction per QA-04 — fix the "well callback" row in `manuscript/manhwa/ep1_adaptation_variance.md` ("For the well" IS in script P40; dropped only at the readers layer); (b) TASK-0017 — EP.2 "Last Day" script OUTLINE proposal (beat map only, NOT the script) to `studio/06_Operations/WORK_IN_PROGRESS/ep2_outline_proposal.md`; Q-02 (Han's keepsake choice) must be presented as UNDECIDED options for the Owner, never resolved.
- **⑤ GATE(②):** verify the correction against sources, outline is proposal-only, lane + night compliance → `REVIEWS/CYCLE-0002_GATE-LORE.md`, PASS/FAIL.
- **③ Visual (one commit):** TASK-0018 — `studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md`: DRAFT specs for the three missing environment plates (KF-03, KF-04, KF-12 centerpiece), the monster/"extinction content" design (KF-07/08), and the registry-card UI (KF-15). Spec format per Handbook v1 §15; canon-silent details marked PROPOSAL; no locks, no generation.
- **⑤ GATE(③):** verify source-citation discipline, flat-2D law, PROPOSAL marking, lane + night compliance → `REVIEWS/CYCLE-0002_GATE-VISUAL.md`.
- **④ Repo & Canon (one commit):** TASK-0019 — complete CANON_REGISTRY Locations/Environments + Powers/Effects stubs; append OPEN_QUESTIONS cross-link entries for the recorded conflicts/gaps (QA-09; next free numbers Q-15+); refresh INDEX with CYCLE-0002 files. Records only.
- **⑤ GATE(④):** verify registry entries against sources (no canon invention), Q-numbering correctness, INDEX accuracy, lane + night compliance → `REVIEWS/CYCLE-0002_GATE-REPO.md`.

## Gate protocol (Amendment 2 §A2.3)
Gate scope = that department's cycle commit(s) only. PASS → conductor continues (non-blocking findings queued). FAIL → conductor returns work to the same department with findings; same gate re-runs. Two FAILs at the same gate → HALT, Owner report. Severity scale: S0–S4 per QA_REVIEW_TEMPLATE (QA-11 adopted studio-wide from this cycle).

## Risks
- Narrow legal envelope while DEC-0008 pending; departments must queue rather than resolve anything semantic.
- Q-numbering collision risk in OPEN_QUESTIONS appends — GATE(④) explicitly checks.

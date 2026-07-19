# QA REVIEW TEMPLATE

> **Maintained by ④ Repository & Canon Management.** Aligned verbatim with `studio/00_OPERATING_HANDBOOK.md` v1 §21 "Quality Assurance" finding template and severity/confidence scale, and with the §8.5 Continuity & Production QA Specialist brief (which Amendment 1 §A1.5 maps to ⑤). Intended location for instances of this template: `studio/06_Operations/REVIEWS/<review-name>.md`, owned by ⑤. Delete this notice line when instantiating a real review.

---

# QA Review — <review name / scope, e.g. "CYCLE-0001 Cycle Audit">
- **Date:** <YYYY-MM-DD> · **Author:** ⑤ Quality Assurance · **Task ID:** <TASK-ID>
- **Scope:** <files/assets/shots/commits under review — be exact; QA authority is to report and recommend, never to silently fix semantic canon or approve its own disputed interpretation (Handbook §8.5 "Authority").>

## Findings

### QA-[ID] — [short title]
- **Severity:** S0 CRITICAL / S1 BLOCKER / S2 MAJOR / S3 MINOR / S4 POLISH
- **Confidence:** HIGH / MEDIUM / LOW
- **Type:** canon / adaptation / continuity / asset / art / motion / repository / build
- **Evidence:** <exact file/section or asset/shot ID, quoted or closely paraphrased>
- **Governing source:** <the file/rule this finding is checked against>
- **Consequence:** <what breaks or is at risk if this finding is not addressed>
- **Owner role:** <which department would need to act — ⑤ never resolves canon/asset content itself>
- **Recommended action:** <concrete next step, phrased as a recommendation, not an edit ⑤ performed>
- **Status:** OPEN / ACKNOWLEDGED / RESOLVED / WONT_FIX <cross-reference the resolving commit or creator decision once applicable>

<Repeat one QA-[ID] block per finding. Number sequentially within this review; do not reuse IDs across reviews without a clear cross-reference.>

## Severity reference (verbatim from Handbook §8.5/§21)
- `S0 CRITICAL` — secret exposure, repository corruption, destructive history rewrite, or severe safety issue. Stop pipeline.
- `S1 BLOCKER` — canon contradiction, broken locked asset, failed production gate, or unusable output. No downstream work.
- `S2 MAJOR` — continuity or production defect that materially harms story/readability/consistency.
- `S3 MINOR` — localized issue with low downstream impact.
- `S4 POLISH` — optional clarity or style improvement.

## Confidence reference
`HIGH` / `MEDIUM` / `LOW`. Low-confidence findings must not trigger semantic edits without further review.

## Protected zones (do not silently fix — per Handbook §21)
Canon bibles · prose and dialogue · approved adaptation scripts · locked asset facts · creator approvals · private/sealed information. Safe non-semantic fixes are limited to broken links, index entries, obvious spelling, malformed Markdown, and metadata formatting — only when meaning is unchanged and the edit is logged.

## Summary

- Findings by severity: <counts>
- Findings by confidence: <counts>
- Lane-compliance verdict (if this review covers commit/turn compliance): <pass/fail per commit, with the specific lane-boundary check performed>
- Recommended next steps for ① / Creator: <short list>

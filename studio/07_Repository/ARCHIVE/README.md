# PATCH 10.0 — ARCHIVE POLICY

> **Maintained by ④ Repository & Canon Management.** This directory holds superseded repository content that is retired from active use but preserved for provenance. It is a policy record, not itself a canon source.

## Current state

**Empty at creation (CYCLE-0001).** No item has been moved into `studio/07_Repository/ARCHIVE/` as of this file's creation. This directory exists so that when the first archival need arises, there is already an agreed process and metadata schema to follow — nothing is being retired *by* the act of creating this policy.

## The archive-don't-delete law (per `studio/00_OPERATING_HANDBOOK.md` v1 §3.1 "Repository law" and the retcon procedure at §13)

- **Superseded content is archived, never deleted.** The Handbook's retcon procedure (§13, step 7) states explicitly: "Update authoritative sources and mark superseded text rather than erasing provenance." This directory is the location for content that has been fully superseded and removed from its original active location — it is not a location for content that is merely marked `SUPERSEDED` in place (see "What does NOT get archived" below).
- **Deleting, archiving, or broadly restructuring repository content requires creator approval** (Handbook §4, "Require creator approval before" list). No department — including ④ — may move a file into this archive unilaterally as part of routine maintenance. A move into `ARCHIVE/` is itself a repository-restructuring action and needs the same approval gate as any other broad restructuring, unless the Creator has pre-authorized the exact scope (Handbook §3.2, canon law's general pre-authorization exception, applied here by extension).
- **Git history is never rewritten to simulate archival.** The Handbook's Safe Git Workflow (§12) forbids force-push, destructive reset, and rewriting published history. Archiving in this repository means moving current content to a new path in a normal commit — it never means altering or squashing the commits that originally introduced the now-superseded content. Anyone who needs the exact prior state can always recover it from git history regardless of what this directory contains.

## What gets archived

- **Superseded documents:** a file (or a clearly-bounded section of a file) that has been fully replaced by a newer, creator-approved version, where keeping the old version in its original active-lane location would create confusion about which one is current.
- **Deprecated versions:** an asset record, spec, or production doctrine that a later, explicitly-superseding document has replaced (the Handbook's model for this is `studio/03_Assets/Asset_Registry.md`'s own in-place "DEPRECATED (never use as refs)" section and the "DEPRECATED-ERA TITLES" list in that file's appendix — but note those stay in place as a section *within* the live registry, they are not moved to this ARCHIVE/ directory; see the boundary note below).

## What does NOT get archived (stays in place, per existing repository practice)

This repository already has a working pattern for marking content superseded *without* moving it: `Asset_Registry.md`'s in-file `DEPRECATED` section, `SOURCE_OF_TRUTH.md`'s `SUPERSEDED`/`HISTORICAL_RECORD` classification types applied to whole files or sections in place, and `story_bible_tagging_proposal.md`'s per-section `SUPERSEDED`/`HISTORICAL_RECORD` tagging proposal for `manuscript/bible/story_bible.md`. **This ARCHIVE/ directory is for content that is being relocated out of its original file entirely** (e.g., an entire file replaced wholesale, or a large excised block that would otherwise clutter an active document) — it is not a substitute for the existing in-place classification/tagging convention, and ④ should not move content here merely because it is tagged `SUPERSEDED` in place. When in doubt, leave content where it is with an in-place tag; only use this directory when a creator-approved decision specifically calls for physical relocation.

## Required metadata for archived items

Every item moved into `studio/07_Repository/ARCHIVE/` must be accompanied by a short front-matter block (in the archived file itself, or in a co-located `.meta.md` sidecar if the archived item is not itself Markdown) recording:

| Field | Requirement |
|---|---|
| **Original path** | The exact repository path the item lived at before archival. |
| **Date** | The date of archival (not the date the content was originally authored). |
| **Reason** | A one-line statement of why it was archived (e.g. "superseded by studio/02_Art/Kit_Specs_DRAFT.md v3 kit specs, per DEC-00xx"). |
| **Superseding file** | The exact path of whatever now serves the purpose this item used to serve — or "none; retired without replacement" if that's genuinely the case, stated explicitly rather than left blank. |

This mirrors the same discipline the Handbook already requires for asset deprecation (§8.3 "Required asset metadata" — "replacement/deprecation link") and for retcons (§13 — "mark superseded text rather than erasing provenance"), applied to whole-file/whole-block archival rather than just per-asset or per-passage deprecation.

## Process (for a future turn that actually archives something)

1. Identify the specific content to be archived and confirm creator approval exists for the relocation (per the approval-gate note above) — cite the approving decision by DEC-ID or explicit in-thread instruction.
2. Move the content into `studio/07_Repository/ARCHIVE/`, preserving its original filename unless a collision requires disambiguation (in which case prefix with the original path, flattened, e.g. `studio_02_Art_OldFile.md`).
3. Add the required metadata block (see table above) at the top of the archived file.
4. If the content was removed from its original active location rather than merely copied, leave a short pointer comment or note at that original location (or in the file that now supersedes it) so future readers landing on the old path are redirected — this is a meaning-safe mechanical fix ④ may perform under its general charter (Handbook Amendment 1 §A1.2), not a canon edit.
5. Log the archival action in `studio/06_Operations/CHANGELOG.md` under the acting department's turn entry, and cross-reference the approving decision.
6. Update `studio/07_Repository/INDEX.md` to reflect the new `ARCHIVE/` entry and the change at the original location.

## Ownership

This policy file and the `ARCHIVE/` directory's contents belong to ④ Repository & Canon Management's write lane (`studio/07_Repository/**`, per Handbook Amendment 1 §A1.2). Approval to *populate* the archive with a specific item remains the Creator's, per the approval-gate law stated above — ④ stewards the policy and the metadata discipline; it does not unilaterally decide what gets retired.

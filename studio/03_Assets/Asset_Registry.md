# PATCH 10.0 — ASSET REGISTRY (single source of truth for LOCKED assets)
> URL prefix for image IDs: `https://hyperagent.com/api/files/usergenerated/threads/cmrq4obz903rv08adamuf67hg/images/{id}.png`
> Rule: generate nothing character/location-bearing without the relevant LOCKED asset in inputImages. New approvals get appended here with date + status.

## Characters — LOCKED
| ID | Asset | Image |
|---|---|---|
| CHAR-001-M | Seo Han master ("Take B") — identity+style anchor | `7fefab61-ab32-43ab-ad25-b18a7211fd01` |
| CHAR-001-K1 | Han turnaround+heads | `8f1aa96d-3e02-41cd-a990-8f6c9bbf95d8` |
| CHAR-001-K2 | Han expressions (incl. nine-ring glow) | `b1ddf46f-166b-4600-a967-823b262994a8` |
| CHAR-001-K3 | Han combat ref | `cd4a7c6b-47fc-457a-a4ca-51f8c53be140` |
| CHAR-001-V8 | Han 8.0 wasteland master | `458bdd99-d4e8-477e-a9a6-38925ac1535f` |
| CHAR-002-M | Yoon Si-woo master | `17924d43-cfdf-4119-aa30-29f91d4dd684` |
| CHAR-003-M | Yoo Ha-eun master (no hairpin) | `1b6693bf-a1d9-4812-a696-5456b86f48e9` |
| CHAR-004-M | Cha Mi-ran dual master | `2ec02dec-0b7a-46a6-aacd-3a55440452df` |
| CHAR-005-M | Proctor Im Dan-bi design lock | `0f602652-afb4-4eb9-bb99-45027172e266` |

## Environments — LOCKED
| ID | Plate | Image |
|---|---|---|
| ENV-001 | Sparring hall | `919e3994-1d87-49a8-b6cc-3e525d031d25` |
| ENV-002 | Cha's Kitchen interior | `4e486d8f-d2b7-4e38-8540-a8f672770290` |
| ENV-003 | Academy exterior | `2baee793-efe6-458e-a8aa-31c4f6078c34` |
| ENV-004 | Dorm rooftop night | `8b7d84fa-b94f-4738-89f9-65fd906dad2b` |

## Style anchors (real PMU)
Tiles: STYLE-DAILY `2f103f7c-fb32-47d0-b1a9-bbfa7af6b0ed` · STYLE-ACTION `1bf3c5c8-789e-4af7-a2b8-a2ae09e3df82` · STYLE-QUIET `8bb93088-b0e5-4c11-a10a-0950416f5ec7`. Full chapters on disk: `refs/pmu_ch051|085|086|103|142|144|189/`.

## Published works
- EP.1 Part 1 reader — artifact `cmrq8ft2t02fj08adv41cw9e7` (v5). 24 block images (full ID list in `manuscript/bible/story_bible.md`).
- EP.1 Part 2 reader — artifact `cmrqmfttc078s07ad4fht9uln`. 18 anchor-locked blocks + Haeseong establishing `27abd66f…`, dream `2b5166d0…`, moon `10459d76…`, final splash `520b367c…` etc.
- Trailer v1 (69s, calm-teaser register) — video file `cmrqmztjd079107addefval2e`; 8 Veo source clips; Pillow title cards in `trailer/`.
- Master Project Bible — platform document `cmrr0f9vr0bg907ade7vvxsnd` (global).

## DEPRECATED (never use as refs)
All v1 painterly-era and v2 SL-flat-era assets (old covers, old casting sheets `c10f…`/`1a75…`, composed-page tests `4d147beb…`/`5ac71fe7…`, horizontal-seam tears `55d895e7…`/`1f5e0a4e…`). Historical record only.

## Approval workflow
PROPOSED → creator approves → mark **LOCKED** here with date → usable. Any drift found later: re-roll the offending panel against the registry, never "fix" by re-designing the asset.

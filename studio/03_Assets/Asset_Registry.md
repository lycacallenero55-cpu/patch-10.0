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

## APPENDIX — Library lookup table (archived 2026-07-19)
> The platform Library lists images by their generation **display title**. Use this table to locate any locked asset by search. Titles are exact.

**LOCKED (title ↔ registry ID):**
| Registry | Library display title |
|---|---|
| CHAR-001-M (Take B master) | "Seo Han — flat-2D take B" |
| CHAR-001-K1 | "Seo Han v3 — turnaround & heads" |
| CHAR-001-K2 | "Seo Han v3 — expressions" |
| CHAR-001-K3 | "Seo Han v3 — action reference" |
| CHAR-001-V8 | "P1-A0 — Han 8.0 v3 master" |
| CHAR-002-M | "Si-woo v3 master" |
| CHAR-003-M | "Ha-eun v3 master" |
| CHAR-004-M | "Cha Mi-ran v3 dual master" |
| CHAR-005-M | "Proctor Im Dan-bi — design lock" |
| ENV-001 | "ANCHOR — Sparring hall (canonical)" |
| ENV-002 | "ANCHOR — Noodle shop interior (canonical)" |
| ENV-003 | "ANCHOR — Academy exterior (canonical)" |
| ENV-004 | "ANCHOR — Dorm rooftop night (canonical)" |
| STYLE tiles | workspace files `refs/anchor_daily.png`, `refs/anchor_action.png`, `refs/anchor_quiet.png` (sliced from creator's PMU library) |

**EP.1 Part 1 v5 published blocks (titles):** "B1 — Grown crack, Han below" · "B2 — Both hands on the strap" · "B3 — The chalk names" · "B4 — Cha at the wrench" · "B5 — You're sure?" · "B6 — Han answers at dusk" · "B7 — Stars sliding wrong" · "B8 — The wave takes the desert" · "B9 — Rain washing the dust" · "B10 — The canteen" · "B11 — The empty street after" · "Conv page 1/3 — You're sure?" · "Conv page 2/3 — Does it hurt?" · "Conv page 3/3 — Then we build" · plus retained v3 blocks titled "EP1v3 P2-3/P4/P6/P7/P8/P9-10/P12-13/P15-16/P19-20/P22-24/P30-31/P32/P33-34/P35 — …" (full ID list in `manuscript/bible/story_bible.md`).
**EP.1 Part 2 published blocks (titles):** final reader uses the refined "P2-R2 … P2-R19" series ("P2-R2 — Cha serves bowl" → "P2-R19 — Final splash: the world runs early") plus "P2-G1 — Haeseong in festival season". Where a P2-G number has a P2-R counterpart, **R supersedes G**.

**DEPRECATED-ERA TITLES (recognize and never reference):** v1 painterly — "Seo Han character sheet", "Seo Han — Design A/B", "Seo Han — FINAL design", "Seo Han — full-body turnaround / head angle sheet / expression sheet / combat reference", "Supporting cast sheet", "Yoon Si-woo — design", "Yoo Ha-eun — design / proportion fix", "Cha Mi-ran — dual-era design / proportion fix", "PATCH 10.0 — Episode 1 cover", all "EP1 P1…P11 —" and "EP1v2 —" titles, "EP1 PAGE 1 …" tests, "Strip — crack begins/grown", "Interaction test — spar with eyelines", "EP1 conversation page test". v2 SL-era — "Seo Han — SL-style take 1/2/3", "Si-woo / Ha-eun — master (locked style)", "… angles & expressions", "Cha Mi-ran — dual master (locked style)". v3 explorations not locked — "Seo Han — PMU-style recast test", "Seo Han — flat-2D take A / take C (action)", "Han 8.0 wasteland master" (pre-v3), "World test — Haeseong at festival dusk".

**Reference library provenance:** creator's PMU pages came from their Drive folder (`drive.google.com/drive/folders/1_EVgpqiHPo8-q3zLHBprJi8Vy6f5IGOf`) — chapters 51/85/86/103/142/144/189 harvested to `refs/` in the origin-thread workspace. Copyrighted: never commit to repo, never publish; style-anchor use only. Ch.143 was HTML-only in Drive (images never obtained).

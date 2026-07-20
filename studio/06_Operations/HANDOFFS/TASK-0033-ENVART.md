# TASK-0033 — ENVIRONMENT ART HANDOFF (ENV-SPEC-A/B/C plates produced)

**From:** Environment Art Agent · CYCLE-0006 · 2026-07-20
**Authority:** Owner ruling DEC-0018, 2026-07-20 — spec LOCKs recorded in `studio/03_Assets/Asset_Registry.md` at commit `828ef2a999ed5cf4d851147ce4b32187356f5986`; specs pinned at git blob `1356127b39dae889f6559ffaacd4fe1c7e2f5356` of `studio/02_Art/Trailer_v2_Gap_Specs_DRAFT.md` (PART I)
**Work Order:** TASK-0033 (P1), dispatched by Executive Producer Agent at base commit `8ae515c87146e8cb222d601f504bbf5dae1d8924`
**Agent thread (audit + master files):** https://hyperagent.com/thread/cmrswjjuf0zer07ad7whdn6qe
**Pin verification:** the spec file was fetched at commit `828ef2a9…` and the returned blob SHA was exactly `1356127b39dae889f6559ffaacd4fe1c7e2f5356` — generation ran against the Owner-approved bytes, not any later revision.
**Engine law:** every plate generated with `openai/gpt-image-2` (DEC-0003), quality `high`. Zero engine substitutions. Style law: `studio/02_Art/Art_Direction.md` LOCKED v3 (flat-2D PMU webtoon register), enforced in-prompt per its Appendix A constraint doctrine.

## Delivery model

Per house precedent (TASK-0003 destination ruling still OPEN): **zero image bytes in this repository.** The six plate masters are platform-hosted files in the agent thread above (thread-scoped pending TASK-0003 durability). Identity is fixed by the sha256 hashes below; EP relays the files to Visual Review. Platform Library display titles are listed for lookup-table practice (`Asset_Registry.md` appendix convention).

Image URL prefix (this thread): `https://hyperagent.com/api/files/usergenerated/threads/cmrswjjuf0zer07ad7whdn6qe/images/{id}.png`

## Plate index

| Plate | Spec cite (all @ blob `1356127b…`) | Image file id | sha256 | Dimensions | Bytes | Library title |
|---|---|---|---|---|---|---|
| ENV-A1 | ENV-SPEC-A1, PART I §"ENV-SPEC-A" | `bfbb08fe-c62e-4afe-ac0e-981890904634` | `abcbb40ef6cc3556adfcb7c52c4902452fe86d8c56c7cbec509bdcdb85f23862` | 1024×1536 | 2,499,057 | "ENV-SPEC-A1 — 8.0 settlement, wave entering" |
| ENV-A2 | ENV-SPEC-A2, PART I §"ENV-SPEC-A" | `e1df0028-80ce-41d1-95a9-f1d87266758b` | `cc80bfb248b75632d0cabf94130e4fd05549bcb90ece85f15ae5ef7c21119f48` | 1024×1536 | 2,834,259 | "ENV-SPEC-A2 — 9.0 street, wave entering" |
| ENV-B1 | ENV-SPEC-B1, PART I §"ENV-SPEC-B" | `4219571e-91d0-45cc-9ea4-9d546d39c37b` | `e96d9b7742d459901412838f446249eebc09d0d45d23df03f4d02df6ce5e01e8` | 1024×1536 | 2,466,035 | "ENV-SPEC-B1 — 8.0 well-scaffold context, lamplit night" |
| ENV-B2 | ENV-SPEC-B2, PART I §"ENV-SPEC-B" | `e0dfb96e-d89b-471c-9778-4cb0d4cd8320` | `f1cf8214d8581e8c5514557b2ac8156978da137f471772744eba73e1c17947fe` | 1024×1536 | 2,558,477 | "ENV-SPEC-B2 — 9.0 Cha's Kitchen doorway, night rain" |
| ENV-C1 | ENV-SPEC-C1, PART I §"ENV-SPEC-C" | `678d0ada-807b-46dd-808a-930dbafbd308` | `da2f1599b4b4e84fe8e187aa8192e675d13993f8446ec926df3ef6de5ee782ab` | 1024×1536 | 3,033,993 | "ENV-SPEC-C1 — 9.0 street post-patch, festival night" |
| ENV-C2 | ENV-SPEC-C2, PART I §"ENV-SPEC-C" | `01027c93-6033-4c89-b725-4651da9b9238` | `4895839c11ba1066c3f8dd44aa8ba82e1d7ed4b150e5993db0ab05a69c7714a2` | 1024×1536 | 3,317,864 | "ENV-SPEC-C2 — 2.0 murim pass, rain-soaked" |

Model id for every row: `openai/gpt-image-2` · quality `high` · aspect request `9:16` (engine preset delivered 2:3 — see batch deviation D1).

Pair-generation lineage: A2 was generated with A1 as input reference (wave-front geometry + framing skeleton); B2 with B1 as input reference (horizon height + figure scale); C2 with C1 as input reference (locked-camera world-swap edit). A1/B1/C1 were generated prompt-only (see batch deviation D2).

---

## ENV-A1 — 8.0 desert settlement, wide, wave entering

**Spec-compliance self-notes.** Satisfies: true-wide vertical composition, upper ~40% night sky; settlement low and huddled (timber well-scaffold with cross-brace and bolt hardware, oil lamp at the scaffold; round water tank on legs with two tiny illegible chalk scribbles — one white, one pale yellow; cookfire ember glow; patched timber shacks and tarps; red dust) — all per the spec's canon-cited set-dressing list. FX-PATCH grammar verbatim: blinding white rewrite wall, terrain caught mid-conversion as thin white wireframe ghosts, square pixel-static flakes, torn-paper shards; wave reads as weather, not explosion. Front crosses the right portion at ~20–25° from vertical. Right-of-front: 9.0 night boulevard with clock tower silhouette and warm amber windows, muted by night (watchtower→clocktower conversion echo). 8.0-side palette: rust + cold night blues + white static specks. Sky-crack present at a THICK/late progression stage with glass-shatter branching, peeling night-sky shards, and a faint alien glyph row — visibly beyond KF-01/KF-02's thin stages (progression law). Upper-LEFT sky quarter held clean for the S06 card. No figures; no accent glow; funeral register.

**Deviations declared:** (a) The 9.0-side boulevard architecture reads generically European rather than Korean-coastal Haeseong vernacular — flagged as a Visual Review taste-call; re-roll against the same spec is cheap. (b) The two chalk marks read as faint tiny scribbles at wide-plate scale; the illegibility law is satisfied, and legible-scale treatment belongs to a future water-tank close plate, not this wide.

**Generation prompt used (verbatim):**

```
Flat 2-D Korean webtoon environment plate, vertical composition. STYLE LAW (strict): clean confident ink outlines define every form; flat matte color fills; maximum 2–3 hard-edged cel-shadow tones; visible cross-hatch pen shading for texture; smooth simple gradients allowed ONLY in the sky. The finished image must look scanned from a printed webtoon page. STRICTLY FORBIDDEN: 3D volume shading, glossy or specular highlights, photorealism, depth-of-field blur, bokeh, airbrush softness, painterly digital-art rendering, lens flare, film grain.

SCENE — night, true wide establishing shot, upper 40% of the frame is night sky. A tiny huddled desert settlement sits low in the frame, small against a vast empty red desert: a tall timber well-scaffold with cross-braces and heavy bolts standing over a dark shaft; a round metal water tank on legs bearing two tiny unreadable chalk scribbles (one white, one pale yellow — far too small to read); a faint cookfire ember glow between shacks; patched timber shacks and tarps; thin red dust haze; a small oil lamp glowing at the scaffold. Palette on this side: rust red, cold night blues, sparse tiny white static specks floating in the air.

THE WAVE — slicing across the right portion of the frame at a 20–25 degree diagonal from vertical: a blinding pure-white wall of light, a "rewrite wave" converting the terrain line by line. Along its edge the ground and structures are caught mid-conversion as thin white wireframe ghost outlines; small square pixel-static flakes and torn-paper shards drift off the front. To the RIGHT of the white wall the land has already become a different world: a tidy night city boulevard with a clock tower silhouette and warm amber windows, colors muted by night. LEFT of the wall: untouched red desert and the settlement.

SKY — high above the wave on the right side, one thick jagged diagonal white crack in the night sky with glass-shatter branching, night-sky shards peeling like broken mirror, and a faint row of tiny alien glyphs inside the widest part. The upper-LEFT quarter of the sky stays completely clean and empty — plain dark night-sky gradient only, no elements there (reserved for a title card).

No people, no animals, no creatures, no readable text, no logos, no watermark. Mood: a funeral, not a spectacle — the wave moves like slow weather, it does not explode.
```

---

## ENV-A2 — 9.0 Haeseong street, wave entering (matched pair with A1)

**Spec-compliance self-notes.** Satisfies: same framing skeleton as A1 (wide, high sky band); wave-wall at the same diagonal angle and same right-of-frame screen position (A1 passed as geometry reference — the S06 match-cut rhyme). Pre-wave register: bright festival DAY at full 9.0 brightness (warm daylight, festival golds, clear blues, lantern ambers) per the OQ-VIS-2 recommendation-on-record in the locked spec text. Dressing per spec: tram rails, tram-wire poles, plane trees with paper lanterns accumulated in branches, long festival banners along the tram line (lettering distant/unreadable), children's chalk adverts on the pavement (unreadable — the spec's noted canon echo of A1's chalk names). Behind-of-front: the same street drained — desaturated greyed ambers and cold greys, lanterns dark, banners torn/blank, white static flecks in the air. FX-PATCH grammar as A1 (wireframe ghosts, square static flakes, torn-paper shards, blinding core). Sky clean and crackless on the bright side — the wave is the only wrongness in frame (OQ-VIS-2 recommendation-on-record). Upper-LEFT sky quarter clean for the shared S06 card. Street plate, not a re-dress of ENV-003 (no campus/hilltop geometry). No figures — clean plate.

**Deviations declared:** (a) OQ-VIS-4's optional banner-rope-snap beat NOT executed (unforced proposal; base spec text is complete without it). No sibling clean-state variants were produced (they are flagged in the spec but not locked for production). (b) The drained side reads as de-rendered near-linework grey — an interpretation of "colors drained" consistent with FX-PATCH's line-by-line conversion grammar; Visual Review to confirm the register.

**PAIR NOTE (A) — OQ-VIS-1 execution and a flagged tension.** Both sub-plates were executed per ENV-SPEC-A1's canon-cited composition law ("left-of-front still 8.0 desert, right-of-front already 9.0 boulevard — directly per published-script canon [P30]"): in BOTH plates the post-wave state occupies screen-RIGHT and the front implicitly advances screen-left into the older world, at the recommended 20–25° diagonal. Flag: if OQ-VIS-1's "screen-left → screen-right" phrase is read as literal front TRAVEL direction, it is geometrically incompatible with that canon-cited left/right assignment (left→right travel would put the converted zone on the LEFT); it was read here as the old→new spatial reading direction, which P30 satisfies. The A1↔A2 match-cut geometry is internally consistent as delivered; if the Owner rules literal left→right travel, both plates re-roll mirrored — a cheap fix. **This execution resolves nothing: OQ-VIS-1 remains open.**

**Generation prompt used (verbatim; input image = ENV-A1):**

```
Use the reference image ONLY for its framing skeleton: a vertical wide establishing shot with a high sky band, and a blinding pure-white "rewrite wave" wall of light slicing across the RIGHT portion of the frame at the exact same 20–25 degree diagonal angle and same screen position as in the reference. DO NOT copy the reference's desert location, settlement, city content, or sky crack — this is a completely different place and moment.

Flat 2-D Korean webtoon environment plate, vertical composition. STYLE LAW (strict): clean confident ink outlines define every form; flat matte color fills; maximum 2–3 hard-edged cel-shadow tones; visible cross-hatch pen shading for texture; smooth simple gradients allowed ONLY in the sky. Must look scanned from a printed webtoon page. STRICTLY FORBIDDEN: 3D volume shading, glossy or specular highlights, photorealism, depth-of-field blur, bokeh, airbrush softness, painterly rendering, lens flare, film grain.

SCENE — bright festival DAY, wide shot down a Korean coastal city street dressed for a festival: tram rails in the roadbed, a line of tram-wire poles, leafy plane trees with clusters of paper lanterns accumulated in their branches, long festival banners strung along the tram line (any lettering distant, tiny and unreadable), children's chalk drawings and adverts on the pavement (unreadable scribbles), low Korean storefronts. LEFT of the wave-wall (most of the frame): FULL 9.0 brightness — warm golden daylight, festival golds, clear blue sky, lantern ambers, cheerful saturated color.

THE WAVE — the same blinding white vertical wall from the reference, converting the street line by line as it crosses: at its edge, buildings and pavement caught mid-conversion as thin white wireframe ghost outlines; small square pixel-static flakes and torn-paper shards drifting off the front. To the RIGHT of the wall: the SAME street continuing, but drained — colors desaturated to greyed ambers and cold greys, paper lanterns gone dark line-by-line, banners torn and blank, faint white static flecks in the cold air.

SKY — clean clear blue sky on the bright side with NO crack, NO damage — the wave is the only wrongness in the frame. Right of the wall the sky turns drained and cold grey. The upper-LEFT quarter of the sky stays completely clean and empty (reserved for a title card).

No people, no animals, no creatures, no readable text, no logos, no watermark. The street is empty of figures — a clean environment plate.
```

---

## ENV-B1 — 8.0 well-scaffold close context, lamplit night

**Spec-compliance self-notes.** Satisfies: close/medium character-context framing (not a wide); heavy timber platform edge with oversized wrench-scale bolts and iron brace hardware; rust dusting off the timber like red snow; canvas tarp corner; the shaft's black drop implied below the platform edge (depth suggested, not mapped); one warm oil lamp as the single practical light pool (the "one accent light" discipline the spec borrows as its own PROPOSAL), everything else cold night blues + rust; round water-tank silhouette in the mid-background; thin sliver of night sky at the top rimmed with faint white static specks; clear standing-figure staging room just right of center, empty (seam-inner edge — see pair note B); no canteen (OQ-VIS-5 recommendation-on-record: omit); no Cha figure and no kit elements — this is the ENVIRONMENT HALF only, per the LOCK's own scope line.

**Deviations declared:** (a) Eye-level/horizon sits just below mid-frame rather than a strict lower third; the binding pair-law is that B1/B2 MATCH — B2 was generated against B1 to hold that value (see B2). (b) The background tank's chalk marks read only faintly at this darkness — "faint" per spec; Visual Review to confirm sufficiency. (c) The wrench-callus/left-hand clause binds the future character overlay, not this plate; the lamp-pool side of the staging room is kept open so her left hand can read when composited.

**PAIR NOTE (B).** S07's two cards read 8.0 first, 9.0 second, so the seam order was staged as: B1 = left half (figure room on its RIGHT/inner edge), B2 = right half (figure room on its LEFT/inner edge). Both delivered as full-frame plates at matched horizon height and figure scale so assembly retains freedom in the vertical-wipe seam placement. This staging choice is composition execution only — it does not decide OQ-VIS-5's context-vs-close-up question, which the spec itself notes these plates keep producible without resolving.

**Generation prompt used (verbatim):**

```
Flat 2-D Korean webtoon environment plate, vertical composition. STYLE LAW (strict): clean confident ink outlines define every form; flat matte color fills; maximum 2–3 hard-edged cel-shadow tones; visible cross-hatch pen shading for texture; smooth simple gradients allowed ONLY in the sky/background. The finished image must look scanned from a printed webtoon page. STRICTLY FORBIDDEN: 3D volume shading, glossy or specular highlights, photorealism, depth-of-field blur, bokeh, airbrush softness, painterly digital-art rendering, lens flare, film grain.

SCENE — night, close-to-medium environment context shot (not a wide): the edge of a heavy timber well-scaffold platform in a desert work camp. Rough wooden platform planks and railing at the frame's lower half; oversized wrench-scale bolts and iron brace hardware on the beams; fine rust dust drifting off the timber like red snow; the corner of a canvas tarp. Past the platform edge, a black circular shaft drops away into total darkness below — forty meters of nothing, its depth only implied. One warm oil lamp hangs from a post and throws a single warm amber pool of light across the planks; everything outside the lamp pool falls into cold night blues and rust tones. In the mid-background, the dark silhouette of a round metal water tank on legs with faint tiny unreadable chalk marks. At the very top edge of the frame, a thin sliver of night sky rimmed with faint white static specks.

COMPOSITION — eye-level/horizon set at the lower third of the frame. Leave a clear, uncluttered open space just right of center at the scale of a standing adult figure — completely empty, no person there, just clean staging room. Nothing important in the extreme upper corner (kept clean).

No people, no animals, no creatures, no readable text, no logos, no watermark. Mood: quiet, worn, end-of-shift stillness — a humble structure someone finished carefully by lamplight.
```

---

## ENV-B2 — 9.0 Cha's Kitchen exterior doorway, night rain, lantern

**Spec-compliance self-notes.** Satisfies: alley doorway staging (behind-tram-depot context read via chain-link fencing and a tram silhouette in the background gloom); paper lantern the color of a low fire above the door; door slightly ajar with warm interior glow ONLY — no countable interior detail reads through the door (deliberately protects ENV-002's six-stool canon from a count-drift bug; the spec's "warm suggestion, not a redraw of the interior plate"); small door chime; hand-written menu tags pinned at the door edge with tiny unreadable strokes (lettering law); rain as thin STRAIGHT streaks (Effects law); rain-wet paving reflecting lantern amber over cold night blues — the warm/cold palette seam against B1's cold half is the storytelling. Matched horizon height and figure scale with B1 (B1 passed as reference); standing-figure staging room left of center, empty. No Cha figure — environment half only.

**Deviations declared:** (a) The lantern carries a small painted noodle-bowl pictogram (image, not text) — an addition beyond the spec's dressing list; if the Owner/Visual Review prefers a plain low-fire lantern exactly matched to ENV-002's lantern, re-roll is cheap. (b) Benign incidental dressing (potted plant, ceramic jar by the door) not named in the spec — flagged for completeness; nothing canon-bearing.

**Generation prompt used (verbatim; input image = ENV-B1):**

```
Use the reference image ONLY to match two things: (1) the horizon/eye-level height (set just below the middle of the frame, exactly like the reference) and (2) the implied scale of a standing adult figure relative to the frame. DO NOT copy the reference's desert location, scaffold, well, or content — this is a completely different place.

Flat 2-D Korean webtoon environment plate, vertical composition. STYLE LAW (strict): clean confident ink outlines define every form; flat matte color fills; maximum 2–3 hard-edged cel-shadow tones; visible cross-hatch pen shading for texture; smooth simple gradients allowed ONLY in the sky/background. Must look scanned from a printed webtoon page. STRICTLY FORBIDDEN: 3D volume shading, glossy or specular highlights, photorealism, depth-of-field blur, bokeh, airbrush softness, painterly rendering, lens flare, film grain.

SCENE — night rain, close-to-medium environment context shot: the exterior doorway of a tiny Korean noodle shop in a narrow alley behind a tram depot. A single paper lantern the color of a low fire hangs above the wooden door; the door stands slightly ajar and warm amber light spills out through the gap and a small window — only a warm glow, NO interior details visible (no furniture, no counter, nothing legible inside, just soft warm light). A little metal door chime above the door frame; a few small hand-written paper menu tags pinned beside the door (tiny unreadable strokes). Rain falls as thin STRAIGHT vertical streaks. The paving stones are rain-wet and reflect the lantern's amber over cold night blues. Dark alley walls, a hint of tram-depot fencing in the background gloom.

PALETTE — warm lantern ambers pooling around the doorway against cold night blues everywhere else; the warm/cold contrast is the point.

COMPOSITION — eye-level/horizon just below mid-frame, matching the reference. The doorway and lantern sit right of center; leave a clear, uncluttered open space just LEFT of center at the scale of a standing adult figure — completely empty, no person there. Keep the extreme upper corner clean.

No people, no animals, no creatures, no readable text, no logos, no watermark. Mood: warm shelter on a cold wet night — a door that is about to chime.
```

---

## ENV-C1 — 9.0 street, festival night, post-patch battle state (START frame)

**Spec-compliance self-notes.** Satisfies: unnamed mid-city street (OQ-VIS-6 recommendation-on-record — reads Haeseong without spending a named location); medium-wide LOW camera per the power-beat law, strong one-point perspective giving the testimony flood its travel lane; sky band ~upper third. Post-patch state grammar per the Environment Bible's own variant line: debris field, torn festival banners, dead dark lantern strings in bare scorched plane trees, broken stalls — damage kept GENERIC (rubble and torn dressing; no landmark destroyed) per the damage-persists-forever law. 10.0 palette: high-contrast near-monochrome darks; festival golds survive only as drained greyed ambers. Torn-sky light logic: a huge late/wide-stage diagonal crack with glass-shatter branching, square pixel-static leak and faint glyph row is the ONLY sky light — and is a visibly different crack from A1's (progression law: never identical twice). Harbor clocktower silhouette on the skyline at the vanishing point (canon landmark, dressed to carry its C2 counterpart). Every dressing mass chosen to carry a C2 counterpart (rails, pole line, trees, banner/lantern lines, debris, flanking building masses, skyline tower). Upper-LEFT sky corner clean (house reservation; S13 carries no card). Enemy-free, figure-free clean plate per the spec's own packet discipline.

**Deviations declared:** none material.

**Generation prompt used (verbatim):**

```
Flat 2-D Korean webtoon environment plate, vertical composition. STYLE LAW (strict): clean confident ink outlines define every form; flat matte color fills; maximum 2–3 hard-edged cel-shadow tones; visible cross-hatch pen shading for texture; smooth simple gradients allowed ONLY in the sky. The finished image must look scanned from a printed webtoon page. STRICTLY FORBIDDEN: 3D volume shading, glossy or specular highlights, photorealism, depth-of-field blur, bokeh, airbrush softness, painterly digital-art rendering, lens flare, film grain.

SCENE — night, medium-wide shot from a LOW camera angle looking straight down a long Korean city street in strong one-point perspective, vanishing point deep in the frame. Sky occupies roughly the upper third. The street was dressed for a festival but is now dead and battle-damaged: tram rails running down the roadbed into the distance; a marching line of tram-wire poles; bare scorched plane trees hung with strings of dark, dead paper lanterns; long festival banners torn and hanging limp (any lettering distant and unreadable); rubble chunks and scattered debris across the road; broken market stalls. Damage is generic — no single landmark destroyed.

PALETTE — "extinction" register: high-contrast near-monochrome darks; the festival golds and lantern ambers survive only as drained greyed-amber ghosts; deep flat blacks in the shadows.

SKY — the only light source: one huge late-stage jagged DIAGONAL white crack across the night sky, wide and branching like shattered glass, night-sky shards peeling like broken mirror at its edges, small square pixel-static debris leaking from it, a faint row of tiny alien glyphs inside its widest part; harsh white static light falls from the crack onto the street. On the far skyline at the end of the street: the small dark silhouette of a harbor clock tower. Keep the upper-LEFT corner of the sky clean and empty — plain dark sky only, no crack elements there.

No people, no bodies, no creatures, no monsters, no readable text, no logos, no watermark. Mood: silence after catastrophe — an empty stage where a battle will be fought.
```

---

## ENV-C2 — 2.0 murim mountain pass, rain-soaked (END frame, camera-identical with C1)

**Spec-compliance self-notes.** Satisfies the pair-design law — one location wearing two worlds, camera locked: C1 was passed as the input image with a locked-camera edit instruction; the delivered plate holds C1's low angle, one-point perspective, vanishing point, horizon and sky band, with every major mass keeping a counterpart in its silhouette position. The spec's full counterpart map executed: tram rails → rain-worn stone cart-ruts in the same tracks · tram-wire poles → weathered wooden waymarker posts on the same beats · plane trees → wind-bent pines at the same masses · torn banners / lantern strings → faded prayer-cloth strips tied to the waymarkers and lines at the same positions · debris → rain-slicked rocks in the same scatter · flanking building masses → sheer cliff shoulders at the same heights · clocktower silhouette → distant weathered gate-tower silhouette at the same skyline position. No architecture beyond waymarkers and the distant tower — mountain and weather. Palette per the locked spec's proposal text: ink-wash near-monochrome grey-greens, paper-white mist pooling low, matte blacks (FX-QI kinship); rain as straight streaks. Sky-swap payload delivered: a low, WHOLE, unbroken rain sky — no crack, no static anywhere. Solemn/older/quiet register. Enemy-free, figure-free clean plate (OQ-VIS-8 recommendation-on-record: generate clean, decide the stranded-enemy question at packet time). Upper corner clean.

**Deviations declared:** (a) The pair is generative-edit aligned, not pixel-locked: mass-for-mass correspondence is strong but not mathematically identical — S13 first→last interpolation readiness is Visual Review's call, and a re-roll against C1 remains cheap if tighter lock is wanted. (b) **Law note:** this plate cites the ENV-SPEC-C LOCK (Owner ruling DEC-0018) and nothing else. It does NOT constitute first-visual-canon adoption for dead-world 2.0 — **Q-20 remains PENDING**, exactly per the LOCK entry's caveat. The palette and crackless-sky choices execute the locked spec's own proposal text (OQ-VIS-7 recommendation-on-record) without resolving OQ-VIS-7 or Q-20.

**Generation prompt used (verbatim; input image = ENV-C1):**

```
EDIT TASK — world swap with locked camera. Keep the EXACT same camera as the reference image: same low angle, same one-point perspective, same vanishing point, same horizon line, same sky band, same composition. Every major mass in the reference must keep a counterpart occupying the SAME silhouette position. The city becomes an ancient rain-soaked mountain pass — the same place wearing an older world.

COUNTERPART MAP (strict, mass for mass):
- the two tram rails → two rain-worn stone cart-ruts running in the SAME tracks toward the same vanishing point
- each tram-wire pole → a weathered wooden waymarker post at the SAME position and height beat
- each bare scorched plane tree → a wind-bent pine occupying the SAME mass
- torn festival banners and lantern strings → faded prayer-cloth strips tied to the waymarker posts and lines, hanging at the SAME positions
- rubble and debris chunks → rain-slicked grey rocks in the SAME scatter pattern
- the buildings lining both sides of the street → sheer rock cliff shoulders and stone slopes occupying the SAME masses and heights
- the distant clock tower silhouette at the vanishing point → a distant weathered wooden gate-tower silhouette at the SAME skyline position
- NO architecture other than the waymarker posts and that distant gate-tower — this world is mountain and weather, not buildings

SKY SWAP — remove the glowing crack, the static squares and all sky damage entirely. The sky becomes a low, whole, unbroken rain sky of flat grey cloud — no crack, no static, no glow. Rain falls as thin STRAIGHT streaks. Paper-white mist pools low along the pass floor.

PALETTE — ink-wash restraint: near-monochrome grey-greens, paper-white mist, matte blacks, thin white edge light only; solemn, older, quiet — a funeral that outranks any fight.

STYLE LAW (strict): flat 2-D Korean webtoon environment art — clean confident ink outlines, flat matte fills, maximum 2–3 hard-edged cel-shadow tones, visible cross-hatch pen shading, smooth simple gradients only in sky/mist. Must look scanned from a printed webtoon page. STRICTLY FORBIDDEN: 3D volume shading, gloss, photorealism, depth-of-field blur, airbrush softness, painterly rendering.

No people, no animals, no creatures, no readable text, no logos, no watermark. Keep the upper-LEFT corner of the sky clean and empty.
```

---

## Batch-wide deviations (declared plainly)

- **D1 — Dimensions.** All plates are 1024×1536 (2:3 portrait). The locked engine's only portrait preset is 1024×1536; there is no 9:16 preset and DEC-0003 forbids engine substitution, so 2:3 is the lawful maximum-vertical delivery. Compositions were framed for vertical-strip use with safe margins; assembly may crop to 9:16 without losing any spec-required element. Flagged for Visual Review confirmation per plate.
- **D2 — Style anchors unreachable (I-0001 class).** The registered PMU style tiles (STYLE-DAILY/ACTION/QUIET) and `refs/` chapter pages are platform-hosted in the origin thread and are NOT accessible from this production thread (fetch returned "Not authorized"; file lookup 404). Plates were therefore generated with the LOCKED v3 style law rendered as hard flat-2D constraint blocks in every prompt (Art_Direction Appendix A's documented cure), plus in-thread sibling-plate reference stacking for pair geometry. Style-register adherence is prompt-enforced rather than reference-enforced on this batch — Visual Review should weigh PMU-register drift explicitly. This is a fresh, concrete instance of the I-0001 durability problem blocking documented house practice (registry rule: locked assets in `inputImages`); noted for EP/Owner attention on TASK-0003, not re-litigated here.
- **D3 — OQ-VIS-1 tension.** See Pair Note (A): canon-cited side assignment executed; literal left→right front-travel reading would require mirroring; flagged, unresolved, cheap to re-roll.
- **D4 — Open items untouched.** All file-local OQ-VIS items and all official Q-numbers (Q-20/21/22 expressly) remain OPEN. Where generation forced a choice, the execution followed a recommendation-on-record embedded in the Owner-locked spec text and is declared above; no execution resolves any queued item. PART II (monsters) and PART III (registry UI) were not touched, referenced, or visually implied.

## Review checklist — Visual Review Agent

1. **Flat-2D law, per plate:** ink outlines / flat matte fills / ≤2–3 hard cel tones / cross-hatch texture; NO 3D volume shading, gloss, DOF blur, airbrush, painterly rendering. Verdict target: "scanned from a printed webtoon."
2. **Pair A match-cut:** front angle + screen position rhyme between A1↔A2; post-wave state consistently screen-RIGHT in both; FX-PATCH grammar complete in both (blinding core, line-by-line conversion, wireframe ghosts, square static flakes, torn-paper shards); A2 sky fully crackless; upper-LEFT card reservation clean in both. Rule on the D3/OQ-VIS-1 mirror question or pass it to the Owner.
3. **A1 canon anchors:** two chalk marks (one white, one yellow) present and ILLEGIBLE; scaffold hardware family consistent with B1's scaffold; crack at THICK/late stage, distinct from KF-01/KF-02 treatments and from C1's crack (never-identical-twice).
4. **A1 taste flag:** Euro-generic read of the 9.0 boulevard glimpse — accept or order re-roll.
5. **Pair B seam:** horizon height and figure scale match across B1/B2; staging rooms empty and correctly sided (B1 right-of-center, B2 left-of-center); warm/cold palette seam reads; B2 interior is glow-only (six-stool canon not violated — nothing countable); lantern low-fire color vs ENV-002, and the noodle-bowl motif addition — accept or order re-roll; no Cha, no kit elements anywhere.
6. **Pair C centerpiece:** spot-check the counterpart map mass-for-mass (rails/poles/trees/banner-lines/debris/flanks/tower); vanishing point, horizon, sky band identical; C2 sky WHOLE (zero crack/static); C1 damage generic per persists-forever law; judge S13 first→last interpolation readiness explicitly.
7. **Fair-play sweep:** nothing beyond the specs is revealed — no monsters, no registry-card UI, no named characters, no sealed-material implication anywhere in the six plates.
8. **D2 style-drift weighing:** judge PMU-register adherence knowing reference stacking was unavailable; order re-rolls freely (all prompts recorded above for exact re-runs).
9. **Lane confirmation for downstream:** plates enter no production use until this review passes; any registry LOCK entries afterward are Asset Management's lane; Q-20 stays open regardless of outcome.

## Lane confirmation (Environment Art)

Committed in this task: **this handoff file only.** No registry edits, no ops-ledger edits, no Gap_Specs edits, no storyboard/plan edits, no image bytes in the repository, no Drive identifiers in any committed byte. Sealed materials not sought, consulted, or referenced. The plates self-certify nothing — Visual Review gates all downstream use.

*Environment Art lane closed for TASK-0033 pending Visual Review.*

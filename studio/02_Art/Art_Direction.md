# PATCH 10.0 — ART DIRECTION (LOCKED v3)

## Style law (the one look)
Pick Me Up: Infinite Gacha school, **completely flat 2D**: clean confident ink outlines define every form → flat matte color fills → 2–3 hard-edged cel shadow tones max → visible cross-hatch pen shading for texture → simple gradients only in backgrounds. BANNED: 3D volume shading, gloss/specular skin, photorealism, depth-of-field blur, airbrush softness, painterly rendering. Target verdict: "scanned from a printed webtoon."
Style anchors: creator's PMU library at `refs/pmu_ch051|085|086|103|142|144|189/` (full-res strips); sliced tiles registered as images (daily/action/quiet — IDs in Asset Registry).

## Color script (palette = storytelling)
| Section | Palette |
|---|---|
| 8.0 prologue / world-funerals | rust + cold night blues + white static (gloom intentional) |
| 9.0 daily life | FULL brightness: warm daylight, festival golds, clear blues, lantern ambers |
| Patch night | color drains mid-scene |
| 10.0 extinction | high-contrast darks lit by character accent colors |
| World-testimony | the dead world's palette floods back for ~3 breaths |

**Accent system (one glow per character):** Han silver-white (#e8f6ff) · Si-woo warm gold · Ha-eun pale teal · Cha rust (8.0) / lantern amber (9.0) · System cyan #9be8ff on black · Moderator: colorless/redaction.

## Canonical patch visual — the sky-crack
Massive DIAGONAL rift (20–25°), jagged widening fracture glowing white, branching glass-shatter cracks, night-sky shards peeling like broken mirror, square pixel-static debris, faint alien glyph row inside the widest part. **Progression law:** thin at first appearance, visibly grown later; never a straight line; never identical twice.

## Strip format (measured from real PMU; statistical canon)
Borderless full-width blocks, straight edges, ONE moment each. ~40–55 blocks per Part (≈90/chapter). Block heights: median ~1,220–1,330px @800w (some 2,000–3,160). Gaps: 200–400px standard · 400–800 scene change · 800–1,000 ONCE or twice per chapter. Quiet chapters breathe bigger (median ~550px, ~30% blank); grief fragments into SMALLER blocks with MORE air. White pages default; black pages for cold-open/patch/dread.

## Lettering (HTML/Pillow only — never baked)
Small white ovals, 1.5–2px outline, bold ALL-CAPS, tails to speakers, placed in reserved empty corners or floating in gutters; jagged starburst for shouts; tail-less ovals for thought; bordered rectangles for narration; dark ornate cyan plaques for system text; huge rotated Korean SFX (쩌저적 crack · 챙 clash · 탁 tap · 지지직 static · 쿵 thud · 웅성 murmur).
**Dialogue register:** natural FULL sentences, webtoon-translation English; one idea per bubble (≤ ~12 words); reactions get their own beats; devices (mid-sentence rewrite) must be explicitly supported by a follow-up line; no cryptic lines before context exists.

## Cinematic identity (if Ufotable shot a flat webtoon)
Restraint → detonation. Silence is Han's VFX. Low angles for power, high for vulnerability, dutch only for wrongness. Impact frames: 1–2 frame white/black inversion flashes at hit moments (video). Speed lines carry motion; camera never wanders during dialogue. Grief = wide shots + air; dread = empty rooms + distant SFX (boss-reveal rhythm: colossal splash → long gap → empty room + 쿵…).

## APPENDIX A — Style provenance & discoveries (archived from origin thread, 2026-07-19)
- **How the look was found:** creator supplied a Solo Leveling collage + later ~40 real PMU pages + 3 scroll recordings. Two diagnoses unlocked everything: (1) "AI look" = over-rendering; real webtoon style is RESTRAINT (flat masses, minimal face lines, ≤1–2 shadow tones, single accent glow); (2) "3D look" = volume shading/gloss/DOF; cure = hard flat-2D negative constraints + real pages stacked as refs.
- **Reference stacking:** multiple real-page refs per generation call materially improves adherence; single-ref calls drift.
- **Engine history:** Gemini NB2/Pro produced good-but-3D-ish results; the creator blind-picked a GPT-image-2 output ("Take B") as least-AI → engine locked. Do not relitigate without creator.
- **Environment/character anchor stacks** (plate + master per call + restated hair/scar/outfit text) ended the drift class of bugs (changing proctor face, floors, golden-hair slips, broken anatomy).
- **Bubble evolution:** baked-in bubbles (misattributed speakers) → HTML overlay w/ name tags → final: SMALL thin-outline ovals placed only in corners that were RESERVED EMPTY at generation time; more lines float in gutters (real PMU behavior).
- **Copyright note:** the PMU reference pages are analysis/style-anchor material from the creator's own Drive; NEVER commit them to this repository.

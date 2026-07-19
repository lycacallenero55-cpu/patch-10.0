# PATCH 10.0 — IMAGE WORKFLOW + QA
## Image generation recipe (every panel/keyframe)
1. Pick the scene's LOCKED refs from `03_Assets/Asset_Registry.md`: [environment plate] + [character master(s)] (+ STYLE tile if drift appeared last batch).
2. Prompt skeleton: "Reference 1 is the CANONICAL [location] — reproduce its exact [floor/counter/windows/palette] faithfully. Reference 2 = [CHAR] ([restate hair color, eye color, outfit, scar side]). Same flat 2D hand-drawn Korean webtoon technique: clean ink outlines, flat matte fills, hard cel shadows, cross-hatch shading — NO 3D, NO realism, NO blur. Full-bleed borderless block, NO text, NO bubbles. COMPOSITION: keep the [UPPER-LEFT/UPPER-RIGHT] quarter as clean simple background for a speech bubble. SCENE: [one moment; real anatomy; who looks at whom]. [Palette per color script]."
3. Engine: `openai/gpt-image-2`, quality high. Aspect: 2:3 standard block · 9:16 splash · 3:2 wide.
4. Corner reservation is mandatory for any block that will carry a bubble; captions/thoughts go in gutters.
5. Reuse via crops is legitimate (real studios do it) but never as a substitute for a missing keyframe.

## Panel QA checklist (run before assembly)
- [ ] Same face as master (jaw, eyes, hair mass)? Hair COLOR correct?
- [ ] Micro-rules: Han scar LEFT brow / sword RIGHT hand / Si-woo bandage LEFT cheek / Ha-eun no hairpin / proctor black-grey hair?
- [ ] Environment matches plate (floor, windows, furniture count)?
- [ ] Flat-2D law held (no gloss/3D/blur)?
- [ ] Anatomy believable (stance, grip, joints)?
- [ ] Eyelines connect between speakers?
- [ ] Reserved corner actually empty? Bubble won't cover a face?
- [ ] Palette matches color script + single accent glow?
- [ ] Continuity with adjacent blocks (props, damage, time of day)?
FAIL any → surgical re-roll (same refs, name the one fix). Never redesign to excuse drift.

## Reader assembly QA
Gap physics per Art_Direction (200–400 std; 400–800 scene change; 800–1000 max twice) · dialogue register (full natural sentences, ≤12 words/bubble, reactions have beats, devices supported) · black/white sections per color script · SFX layer present · GSAP reveals reduced-motion-safe.

## Escalation
Two failed re-rolls on the same panel → change ONE variable only (camera angle or crop), never the design. Persistent style drift → re-anchor with a real-PMU tile for the next batch. Log every accepted asset into the registry.

## APPENDIX — Proven prompt exemplars (verbatim patterns that worked; archived 2026-07-19)
**1. Style-transfer character master (the "Take B" pattern, GPT-image-2):**
"Study the reference image's hand-drawn Korean webtoon technique and draw an ORIGINAL character in exactly that technique, as if by the same artist. Completely FLAT 2D comic illustration: black ink outlines define every form; flat matte color fills; two to three hard-edged cel shadow tones maximum; visible cross-hatch pen strokes for shading and fabric; hair as flat dark shape with thin sharp highlight strokes; background is a simple flat gradient. Strictly forbidden: 3D volume shading, soft light wrap, depth-of-field blur, gloss, photorealism, airbrush smoothness — output must look like a scanned printed webtoon page. SUBJECT: [character spec]. [Composition]. No text."
**2. Anchor-locked scene panel:**
"Reference 1 is the CANONICAL [location] — reproduce its exact [floor/counter/windows] and palette faithfully. Reference 2 = [CHARACTER] ([hair COLOR], [scar side], [outfit] — keep hair [COLOR]). Same flat 2D hand-drawn Korean webtoon technique: clean ink outlines, flat matte fills, hard cel shadows, NO 3D, NO realism, NO blur. Full-bleed borderless block, NO text, NO bubbles. COMPOSITION RULE: keep the [UPPER-LEFT/UPPER-RIGHT] QUARTER as clean simple background for a speech bubble. SCENE: [one moment; eyelines stated; real anatomy]."
**3. Corner reservation phrasing that works:** "keep the UPPER-RIGHT QUARTER of the image as clean, simple background (wall and steam) — a speech bubble will be placed there later; no important detail in that corner."
**Operational hazards learned:** long pre-signed S3 URLs corrupt easily if retyped — always copy exactly or re-mint; platform /api/ image+media URLs are auth-gated from the sandbox (curl returns 29-byte stubs) — for local processing use GenerateTempExternalDownloadUrl; thread-scoped viewUrls DO work as inputImages within the platform.

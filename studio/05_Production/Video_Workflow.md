# PATCH 10.0 — VIDEO WORKFLOW (keyframe-first)
> Why: video models animate PIXELS, not bodies — no skeleton, no physics, no memory. Fixes: short shots, locked stills as frames, choreography-level prompts, editing does the cinema.

## The law
1. **No video before keyframes.** Every shot needs an approved START still (and END still when the motion is a transformation/travel — use Veo first+last frame interpolation for those).
2. **One action per shot, 4–8 seconds.** Never "a fight" — a single beat of a fight.
3. **Every prompt opens with the preservation clause:** "Motion-comic animation of a flat 2D Korean webtoon panel — preserve the exact flat cel-shaded line art, do NOT morph into 3D, do NOT add realism."
4. **Choreography, not vibes.** Specify: feet/weight, torso mechanics, the strike path, what reacts (debris, cloth, hair), camera behavior, the ONE effect (from Effects Bible), the sound.
5. **Anti-GIF rules:** demand weight ("feet dig, debris kicks"), forbid drift ("no floating, no sliding feet, no morphing faces"); if a result jellies → re-roll same refs, simplify motion.
6. Impact frames, speed ramps, and transitions are added in ASSEMBLY, not asked from Veo.

## Choreography prompt template
"Motion-comic animation of a flat 2D Korean webtoon panel — preserve the exact flat cel-shaded line art, do NOT morph into 3D. [WHO, from the locked design] [SINGLE ACTION with mechanics: 'plants the front foot, hips rotate first, then a horizontal slash — the ink-black calligraphy stroke appears a half-beat after the cut and hangs in the air']. [REACTIONS: dust ring, coat snap, debris]. [CAMERA: e.g., low-angle static / short push-in / handheld half-second shake on impact]. [EFFECT per Effects Bible + accent color]. [AUDIO: one clean sound + room tone]. No text. Vertical framing."

## Shot recipes
- Dialogue/emotion: static or 2% push; blink+breath only; room tone. 4–6s.
- Reveal: slow push toward the wrong thing; audio thins before it hits. 6–8s.
- Action beat: 2–4s; one exchange; impact frame added in edit.
- Transformation/travel (testimony flood, wave conversion): first+last frame interpolation; 6–8s.
- Boss entrance: colossal still animated minimally → CUT to empty-room shot with distant 쿵 (rhythm from real PMU ch.142).

## Assembly (ffmpeg — environment quirks included)
- Fetch clips: platform /api/ media URLs are auth-gated → `GenerateTempExternalDownloadUrl` → curl the S3 URL.
- Normalize every input: `scale=720:1280:force_original_aspect_ratio=decrease,pad=720:1280:(ow-iw)/2:(oh-ih)/2,setsar=1,fps=24,format=yuv420p` + `aformat=sample_rates=48000:channel_layouts=stereo`.
- Joins: montage = `xfade` (0.3–0.5s) + `acrossfade`; action = hard concat ON music beats; the one seam-wipe via xfade=wipeleft.
- Impact frames: 2-frame inverted PNG overlays (`overlay=enable='between(n,X,X+1)'`).
- Speed ramp: `setpts` split segments (0.5× for ≤0.5s only, once per shot max).
- **drawtext does NOT exist in this ffmpeg build** → all cards/logos rendered with Pillow → looped image clips with fades.
- Export: `libx264 crf 20, preset medium, +faststart, aac 192k`. Always probe every downloaded clip before compositing.

## QA per shot
Face/hair/outfit match master? Effect color legal? Weight visible? No jelly/slide/morph? Audio: one clean idea? Duration 4–8s? → then and only then, into the edit.

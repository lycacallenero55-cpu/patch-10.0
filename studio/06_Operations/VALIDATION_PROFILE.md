# Validation Profile
**Status: VALIDATION_UNDEFINED** — no build, test, lint, or link-check tooling exists in this repository. No validation is claimed.
What exists instead (manual/agent checks):
- Markdown: rendered-eyeball only; no linter configured.
- Readers (HTML): render in a sandboxed iframe on the platform; no automated check in-repo. Image URLs inside readers are platform-hosted (see INCIDENTS I-0001 durability note).
- Media: probed ad hoc with ffprobe in the production sandbox; not reproducible from this repo alone.
Proposed (not created — needs creator interest): a tiny CI that link-checks Markdown and validates internal anchors. Until then, never claim tests passed.

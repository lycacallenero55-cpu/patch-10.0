# Incidents
### I-0001 — Reference durability risk (OPEN)
- Severity: S1 for *unattended* visual generation · S3 for interactive in-thread work
- All LOCKED visual masters (character/environment plates in studio/03_Assets/Asset_Registry.md) are platform-hosted, thread-scoped URLs. They resolve for the production thread but are NOT independently durable (no checksums, no rights record, not in creator-controlled storage).
- Per Handbook §9.9 and §15.6 this blocks unattended generation runs that depend on masters; interactive production in the origin thread remains functional.
- Recommended action (TASK-0003): creator chooses a durable home — (a) commit master PNGs to this repo under assets/masters/ (simplest; repo becomes heavier), or (b) creator's Google Drive folder with recorded checksums. Then registry gains checksum + rights fields.
### I-0002 — Historical documents carry superseded guidance (OPEN, informational)
- story_bible.md mixes active canon with deprecated production history (old engines/styles/shot-length guidance). Classification proposed in SOURCE_OF_TRUTH.md; section-level tagging is TASK-0004. Until then do not treat it wholesale as active truth.

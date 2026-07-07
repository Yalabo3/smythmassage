# Build Log

Format: `[Date] — [Client] — [Issue] — [Root cause] — [Fix] — Files: [list]`

---

2026-07-07 — Smyth Massage — Static pitch deploy from HTML mock — Mock used bundled DC-runtime anchors (#home, #staff, #booking) with no FR/EN toggle; pitch spec requires #services, #rates, #about, #location, #contact plus bilingual localStorage toggle — Duplicated mock to `index.html` (original left untouched), added post-render `applySmythDeployPatches()` in bootstrap script to remap section IDs, rebuild nav, inject FR/EN toggle with localStorage persistence, wire Book Online placeholder (`href="#"`, preventDefault), and preserve mailto link — Files: index.html, docs/BUILD_LOG.md

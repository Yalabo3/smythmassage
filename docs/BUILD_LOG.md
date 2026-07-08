# Build Log

Format: `[Date] — [Client] — [Issue] — [Root cause] — [Fix] — Files: [list]`

---

2026-07-07 — Smyth Massage — Static pitch deploy from HTML mock — Mock used bundled DC-runtime anchors (#home, #staff, #booking) with no FR/EN toggle; pitch spec requires #services, #rates, #about, #location, #contact plus bilingual localStorage toggle — Duplicated mock to `index.html` (original left untouched), added post-render `applySmythDeployPatches()` in bootstrap script to remap section IDs, rebuild nav, inject FR/EN toggle with localStorage persistence, wire Book Online placeholder (`href="#"`, preventDefault), and preserve mailto link — Files: index.html, docs/BUILD_LOG.md

2026-07-08 — Smyth Massage — Vercel 404s for `{{ person.photo }}`, quoted asset paths, unstyled page — DC runtime `sc-for` bindings not resolving on Vercel; literal `{{ }}` and extra `"` chars became URL paths (`%7B%7B`, `%22`) — Replaced all `sc-for` loops (staff, conditions, fees) with static HTML; added `fixBrokenAssetAttrs()` post-render patch for quoted src/poster/href — Files: index.html, docs/BUILD_LOG.md

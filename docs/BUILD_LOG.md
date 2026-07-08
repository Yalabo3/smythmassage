# Build Log

Format: `[Date] — [Client] — [Issue] — [Root cause] — [Fix] — Files: [list]`

---

2026-07-07 — Smyth Massage — Static pitch deploy from HTML mock — Mock used bundled DC-runtime anchors (#home, #staff, #booking) with no FR/EN toggle; pitch spec requires #services, #rates, #about, #location, #contact plus bilingual localStorage toggle — Duplicated mock to `index.html` (original left untouched), added post-render `applySmythDeployPatches()` in bootstrap script to remap section IDs, rebuild nav, inject FR/EN toggle with localStorage persistence, wire Book Online placeholder (`href="#"`, preventDefault), and preserve mailto link — Files: index.html, docs/BUILD_LOG.md

2026-07-08 — Smyth Massage — CSP blocks DC runtime `new Function()` / eval on Vercel — Bundled React+DC runtime compiles component scripts at runtime via `new Function()`, which strict CSP rejects — Replaced bundled `index.html` with static HTML export (no React/Babel/manifest); plain JS for FR toggle, hero video, hover styles — Files: index.html, assets/logo.png, docs/BUILD_LOG.md

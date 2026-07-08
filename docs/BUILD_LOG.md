# Build Log

Format: `[Date] — [Client] — [Issue] — [Root cause] — [Fix] — Files: [list]`

---

2026-07-07 — Smyth Massage — Static pitch deploy from HTML mock — Mock used bundled DC-runtime anchors (#home, #staff, #booking) with no FR/EN toggle; pitch spec requires #services, #rates, #about, #location, #contact plus bilingual localStorage toggle — Duplicated mock to `index.html` (original left untouched), added post-render `applySmythDeployPatches()` in bootstrap script to remap section IDs, rebuild nav, inject FR/EN toggle with localStorage persistence, wire Book Online placeholder (`href="#"`, preventDefault), and preserve mailto link — Files: index.html, docs/BUILD_LOG.md

2026-07-08 — Smyth Massage — Vercel 404s for quoted asset paths (`%22assets/...%22`) — DC runtime JSON-wraps img/video attribute values on hydration; browser requests literal quote characters as URL paths — Removed `src`/`poster` from template imgs and video; use `data-smyth-src`/`data-smyth-poster` instead; added `forceAssetUrls()` + MutationObserver; extracted logo to `assets/logo.png` — Files: index.html, assets/logo.png, docs/BUILD_LOG.md

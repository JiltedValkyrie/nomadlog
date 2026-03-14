# CLAUDE.md — Notes for AI Assistants

## Project overview

This repo contains a suite of single-file HTML/CSS/JS tools with no build system, no npm, no framework:

| File | Purpose |
|------|---------|
| `index.html` | Landing hub — links to both apps |
| `apps/nomad.html` | NOMAD LOG — overnight spot tracker for van life |
| `apps/budget.html` | LEOPARD FINANCE — Nissan Leopard road-trip budget tracker |

All apps share the same philosophy: self-contained, no server, portable (runs from a USB drive).

## Architecture

- **Storage**: `localStorage` only. No backend, no network requests except CDN assets and map tiles.
- **Maps**: Leaflet.js (CDN). Dark tile layer from OpenStreetMap.
- **Geocoding**: Nominatim (OpenStreetMap) — free, no API key. Respect 1 req/sec limit.
- **DOM**: jQuery for selectors/events; vanilla JS for data logic.
- **State**: in-memory JS objects synced to `localStorage` on every save.

## Key conventions

- CSS uses CSS custom properties (`--accent`, `--bg`, etc.) defined in `:root` — always use these instead of hardcoded colors.
- Fonts: `'Teko'` for headings/numbers, `'Share Tech Mono'` for labels/meta, `'IBM Plex Sans'` for body text.
- Buttons use `.btn` base class + a modifier (`.btn-primary`, `.btn-ghost`, `.btn-danger`, `.btn-gps`).
- Panels are shown/hidden via `.panel.active` — toggled by `data-panel` on `.nav-tab` buttons.
- Entry data structure: `{ id, name, area, type, date, lat, lng, rating, tags, notes, created }`.

## What to avoid

- Do not split into multiple files without a good reason — the single-file approach is intentional for portability (open directly from a USB drive or file share).
- Do not add a build step or package manager unless the user explicitly asks.
- Do not change the color scheme or typography without being asked.
- Do not introduce a backend or cloud sync without being asked.

## Task tracking — HITLIST rules

- Active tasks live in `HITLIST.md` at the repo root.
- **Always present recommendations to the user and get approval before writing any code.**
- When all items in `HITLIST.md` are checked off, archive it: copy to `archive/HITLIST-YYYY-MM-DD.md` (use the completion date), then start a fresh `HITLIST.md`.
- Create the `archive/` directory if it does not exist.
- Never delete the previous HITLIST — the archive is the history.

# NOMAD LOG // SYSTEMS

A suite of single-file personal tools for life on the road. No server, no account, no cloud — everything lives in the browser's `localStorage`. Open directly in any browser, from a file or USB drive.

## Apps

| File | App | Purpose |
|------|-----|---------|
| `index.html` | Hub | Landing page linking to both apps |
| `apps/nomad.html` | **NOMAD LOG** | Overnight spot tracker |
| `apps/budget.html` | **LEOPARD FINANCE** | Nissan Leopard road-trip budget |

---

## NOMAD LOG

| Tab | Purpose |
|-----|---------|
| **LOG** | Log a new overnight spot — GPS/address pin, spot type, star rating, tags, notes |
| **YT** | Shot-list checklist for YouTube content filmed on the road |
| **JOURNAL** | Browse and search past entries |
| **MAP** | Leaflet map with all GPS-pinned spots + journey playback animation |
| **STATS** | Total nights, avg rating, top tags, spot type breakdown |

- **⌖ SET LOCATION** — opens a modal with address search (Nominatim/OSM), GPS button, and a draggable map pin
- **✎ EDIT** — edit any past entry from the journal list or directly from a map pin popup
- **▶ PLAY JOURNEY** — animates your route chronologically on the MAP tab with a trailing polyline

## LEOPARD FINANCE

| Tab | Purpose |
|-----|---------|
| **DASH** | Budget snapshot — remaining funds, next paycheck, rollover |
| **SPEND** | Log a transaction |
| **BUDGET** | Monthly budget breakdown |
| **RETIRE** | Retirement projection |
| **CAR FUND** | Leopard build fund tracker |
| **HISTORY** | Transaction history with search |
| **CONFIG** | Subscriptions and parameters |
| **◈ DRIVE** | Outrun-style ASCII minigame — speed tied to budget health |

---

## Stack

- Vanilla HTML/CSS/JS — no framework, no build step
- [Leaflet.js](https://leafletjs.com/) 1.9.4 — map rendering (NOMAD LOG)
- [Nominatim](https://nominatim.openstreetmap.org/) — free OSM geocoder, no API key required
- jQuery 3.7.1 — DOM utilities
- Google Fonts: Teko, IBM Plex Sans, Share Tech Mono (Nomad) · Orbitron, Rajdhani (Leopard)
- Canvas API — Outrun road renderer

## Data & Privacy

All data is stored in `localStorage`. Nothing is sent to any server (Nominatim queries are the only network call, from user-initiated address searches). Export JSON backups regularly — clearing browser storage deletes everything.

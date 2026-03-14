# HITLIST

Active task list. When all items are complete, archive this file as `archive/HITLIST-YYYY-MM-DD.md` and start a fresh one.

---

## Landing Page

- [x] Build `index.html` hub linking to `apps/nomad.html` and `apps/budget.html`
- [x] Match shared dark aesthetic; green card for Nomad, cyan for Leopard

---

## NOMAD LOG (`apps/nomad.html`)

### GPS Location Modal
- [x] Build reusable jQuery modal for location entry (address search + GPS button + draggable map pin)
- [x] Integrate Nominatim geocoder for address-to-coords lookup
- [x] Replace inline GPS row on LOG (new entry) with "⌖ SET LOCATION" button that opens modal
- [x] Add "✎ Edit" button to map pin popups — opens full entry edit modal
- [x] Full entry edit modal: pre-populated form, reuses location modal for GPS changes

### Journey Animation (MAP tab)
- [x] "▶ PLAY JOURNEY" button on MAP tab
- [x] Sort entries by date, animate marker with Leaflet `flyTo()` between spots
- [x] Draw trailing polyline (dashed, accent green) as journey progresses
- [x] Popup at each stop: spot name + date, auto-advance after ~2s pause
- [x] Play / Pause / Reset controls
- [x] Progress indicator: "NIGHT N OF N"
- [x] Speed control: slow / normal / fast

---

## LEOPARD FINANCE (`apps/budget.html`)

### Outrun Minigame
- [x] New "◈ DRIVE" tab in budget.html
- [x] Canvas-based perspective road with scroll animation (`requestAnimationFrame`)
- [x] Roadside trees and road signs scale/scroll from vanishing point
- [x] ASCII art Nissan Leopard car at bottom center, rendered on canvas
- [x] Arrow key / WASD steering + touch swipe support
- [x] Speed tied to budget health (savings rate → speed / weather / day/night)
- [x] VFD-style HUD: speed, distance, gear
- [x] Road curves left/right; SPACE for nitro boost

---

## Docs / Meta
- [x] README.md created
- [x] CHANGELOG.md created
- [x] CLAUDE.md created
- [x] HITLIST.md created
- [x] Update CLAUDE.md with HITLIST archival rules
- [x] Update README.md to reflect new `apps/` structure and landing page

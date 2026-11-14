# Customer Editing Guide — wax-seal-royale (Sazid Siddiqui & Muskan Siddiqui)

This template is an Islamic luxury wedding invitation designed for the **Dawat-e-Walima** of **Sazid Siddiqui & Muskan Siddiqui** (Groom-side invitation) with an interactive wax-seal envelope overlay, breaking seal opening animation video, swan background video, custom soundtrack (*ordinary*), live countdown timer, schedule of events, venue details with Google Maps integration, and gift/attire etiquette.

---

## Customer Configuration

All routine customer edits are configured in:
→ `editable/wedding-data.js`

### Couple Information
Edit `couple` in `editable/wedding-data.js`:
- `groom`: `"Sazid Siddiqui"`
- `bride`: `"Muskan Siddiqui"`
- `groomFirst`: `"Sazid"`
- `brideFirst`: `"Muskan"`
- `order`: `"groom-first"` (groom name first per customer specification)
- `subtitle`: `"Two Souls, One Destiny &bull; A Lifetime Written by Allah"`

### Wedding Event Date & Invitation Note
Edit `wedding` in `editable/wedding-data.js`:
- `eventName`: `"Dawat E Walima"`
- `dateLabel`: `"01.12.26"` (Hero banner short date)
- `longDate`: `"Tuesday, 01st December 2026"`
- `time`: `"6:00 PM"`
- `dateISO`: `"2026-12-01T18:00:00+05:30"` (Event start ISO timestamp with IST timezone offset; directly drives the live countdown timer and Google Calendar link)
- `invitationNote`: Main cordial invitation message text

### Schedule of Events
Edit `schedule` array in `editable/wedding-data.js` (4 events):
1. `Guest Arrival` — `6:00 PM`
2. `Dawat-E-Walima` — `7:00 PM`
3. `Dinner` — `8:30 PM`
4. `Duas & Wishes` — `9:30 PM`

### Venue & Location
Edit `venue` in `editable/wedding-data.js`:
- `name`: `"Dulhan Palace"`
- `address`: `"GT Road, Mughalsarai, Chandauli, Uttar Pradesh"`
- `mapsUrl`: `"https://maps.app.goo.gl/znBq1mM28vjNSYhN6?g_st=ic"`

### Special Request & W.B.C.F. (Replaced Gift & Dress Code)
Edit `specialRequest` and `wbcf` in `editable/wedding-data.js`:
- `specialRequest`:
  - `title`: `"Special Request :"`
  - `name`: `"Dr. Arif Jamal Siddiqui"`
- `wbcf`:
  - `title`: `"W.B.C.F."`
  - `members`: `"Samsuddin Siddiqui, Sirajuddin Siddiqui, Sabir, Sahir,<br />Shahid, Khalid, Javed &amp; All Siddiqui Family &amp; Relatives &amp; Friends."`

### Media & Assets
Configured in `editable/wedding-data.js` under `media`:
- `overlayImage`: Wax-seal envelope graphic (`editable/assets/ChatGPT Image Jun 23, 2026, 04_40_29 PM.png`)
- `sealVideo`: Wax-seal breaking/opening MP4 (`editable/assets/1782224012851.mp4`)
- `heroVideo`: Ambient background video (`editable/assets/Swans2.mov`)
- `audio`: Background soundtrack (*ordinary*) (`editable/assets/ordinary.mp3`)

---

## Rules for Future Agents

1. Make customer content edits in `editable/wedding-data.js` and replace media in `editable/assets/`.
2. Keep ISO date strings with proper timezone offsets (e.g. `+05:30`).
3. Validate changes with `node --check editable/wedding-data.js`.

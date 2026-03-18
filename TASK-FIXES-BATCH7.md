# TASK — Frontend Fixes Batch 7 (16 March 2026)

## Context
Single-file frontend MVP (`index.html`, all CSS/JS inline).
PGG = compliance system for UK care providers.
DO NOT change any formatting, styling or layout of things not listed here.

## Changes Required

### 1. Rename "Contact Events" → "Contact Activity"
- Find and replace ALL visible UI instances of "Contact Events" or "Contact Event" → **"Contact Activity"**
- Nav items, headings, buttons, form titles, any visible text
- Do NOT break JS function names — only change visible text/labels

### 2. Add "New Resident Checklist" to SU Profile Forms Dropdown
- On the SU profile, there's a grouped **"Forms"** dropdown button
- Add **"New Resident Checklist"** as a new option in that dropdown
- On click: show a toast "New Resident Checklist — Coming soon" (placeholder for now)

### 3. TL Dashboard — Add Staff Performance Quick Access Link
- On the TL Dashboard, add a **"Staff Performance"** button/link
- Style it similar to the SM Dashboard Quick Access buttons
- Place it near the top (below stat boxes, near notifications/to-do area)
- On click: navigate to the Staff Performance page (nav('staff-performance') or equivalent)

### 4. NEW: Rotas & Scheduling Page (Mockup)
- Add new nav item under **Operations**: **"Rotas & Scheduling"** with a 📅 icon
- Build a mockup page showing:

**Weekly Rota View:**
- Table/grid: staff names down the left, days (Mon-Sun) across the top
- Demo data for 4-5 staff members showing shifts:
  - Shift times (e.g. "08:00-16:00", "14:00-22:00", "Night")
  - Property/location assigned
- Colour coding: confirmed shifts (green background), draft (amber), unfilled/gap (red/light red)
- Heading: "Weekly Rota — Week of 17 March 2026"

**Buttons at top:**
- "Publish Rota" button (toast: "Rota published — sent to staff dashboards")
- "Previous Week" / "Next Week" navigation (toast: "Demo — week navigation")

**Shift Legend:**
- Small legend below: Day (green), Night (blue), Sleep-in (purple), On-call (grey), Unfilled (red)

**Info text:**
- "Rotas & Scheduling is configurable per setting — toggle ON/OFF based on organisational requirements"

### 5. NEW: Staff Expenses Tab (alongside Mileage)
- On the SW Dashboard, in the Lone Working / Mileage section, add an **"Expenses"** tab alongside the existing Mileage tab
- When clicked, show:

**Expense Form (mockup):**
- Date (date picker)
- Category dropdown: Travel, Equipment, Training, Meals, SU Activity, Other
- Amount (£ input)
- Receipt Upload button (toast: "Upload — Coming soon")
- Description/notes (text area)
- SU Related? (Yes/No toggle) — if Yes, shows SU name dropdown
- Submit button (toast: "Expense submitted for approval")

**Recent Expenses List (demo data):**
- 3 demo entries showing: date, category, amount, status (Submitted/Approved/Rejected)
- Running total at bottom: "Total submitted this month: £47.50"
- Status colours: Submitted (amber), Approved (green), Rejected (red)

## Rules
- DO NOT change formatting, styling, or layout of anything not listed above
- Keep ALL existing functionality working
- Keep mobile responsiveness
- Commit with descriptive message
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: Batch 7 — Contact Activity rename, New Resident Checklist, TL staff link, Rotas mockup, Expenses tab" --mode now

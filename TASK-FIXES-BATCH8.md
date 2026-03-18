# TASK — Frontend Fixes Batch 8 (16 March 2026 Evening)

## Context
Single-file frontend MVP (`index.html`, all CSS/JS inline).
PGG = compliance system for UK care providers.
DO NOT change any formatting, styling or layout of things not listed here.

## Changes Required

### 1. URGENT: Replace Real Names in Demo Data
These are real people's names — find and replace ALL instances throughout the ENTIRE file:
- **Megan Thorne** → **"Emma Lawson"**
- **Arouba Khan** (may appear as "Ari Rubicon" or similar) → **"Priya Sharma"**
- **Jack Vinton** → **"Tom Bradley"**
Check: staff arrays, demo notes, contact notes, incidents, kanban cards, SW login, everywhere.

### 2. Homepage — Remove Stat Boxes
Remove these stat boxes from the Homepage top bar:
- **"Total Notes"** — remove entirely
- **"Service Users"** (showing count 634) — remove entirely
Keep all others: Notes This Week, Average AI Score, No Note >7 Days, Open Incidents, Welfare Concern, Welfare Watch, Open General Audits, Open Post-Incident Audits

### 3. Homepage — Remove Analytics Sections
Remove from Homepage:
- **Compliance Rate** section (the donut chart with Score 4/3/2/1 breakdown)
- **Notes Per Week (Last 12 Weeks)** graph
- **Top Gaps Identified by AI** section — move this content to the Support Notes dashboard stats area
Keep on Homepage: Notifications, To-Do, Recent Activity, Recent AI QA Activity, Pillar AI Status

### 4. Homepage Notifications — Make Collapsible
- Add ▼/▲ toggle to the Notifications section heading on the Homepage
- Same collapsible pattern used everywhere else

### 5. Remove Notifications Dashboard from Nav
- Under Overview in the nav, there's a "Notifications" nav item
- REMOVE it — notifications are on the Homepage now, separate page not needed

### 6. Nav — All Categories Collapsible
- Currently only "Analytics & Reports" has a ▼ toggle to expand/collapse its sub-items
- Add the same collapsible ▼/▲ toggle to ALL nav categories:
  - Overview
  - Service Users
  - Compliance
  - Frontline
  - Operations (being renamed, see below)
  - Housing
  - Settings
- Default: all expanded (so nothing looks missing). User can collapse to tidy up.

### 7. Nav Restructure
**A) Rename "Operations" → "Support Operations"**

**B) Move "Properties & Voids"** from Support Operations → under **Housing** section

**C) Move "Housing Benefit"** from Support Operations → into NEW nav section called **"Accounts"**
- Create new nav category "Accounts" (with € or 💰 icon)
- Housing Benefit goes under it
- Position Accounts section between Housing and Settings in the nav

**D) Move "8-Week Guide"** from wherever it is → under **Compliance > Support Documentation** (or directly after Support Documentation in the Compliance section)

### 8. Audit Dashboard — Rename Categories
- On the Audits page, rename "General Case Audits" tab/section
- Split into TWO tabs/sections:
  - **"In-House Audits"** (internally scheduled)
  - **"External Request Audits"** (requested by council, HB, regulatory body)
- Keep "Post-Incident Audits" as-is
- So three sections total: Post-Incident Audits, In-House Audits, External Request Audits

### 9. Support Notes Dashboard — Remove "Team Leader Review"
- On the Support Notes dashboard, remove the "Team Leader Review" stage/tab/column
- TLs don't review or sign off notes — just awareness
- "Awaiting Verification" = notes waiting for AI (Beacon) QA — keep this

### 10. Notes Per Week → Move to Support Notes Stats
- The "Notes Per Week (Last 12 Weeks)" graph removed from Homepage (fix #3)
- Add it to the Support Notes dashboard in the stats/overview area

## Rules
- DO NOT change formatting, styling, or layout of anything not listed above
- Keep ALL existing functionality working
- Keep mobile responsiveness
- Commit with descriptive message
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: Evening batch — names replaced, homepage cleaned, nav restructured, audit renamed, TL review removed" --mode now

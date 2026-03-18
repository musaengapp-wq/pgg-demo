# TASK — Frontend Fixes Batch 3 (16 March 2026)

## Context
Single-file frontend MVP (`index.html`, all CSS/JS inline).
PGG = compliance system for UK care providers.
DO NOT change any formatting, styling or layout of things not listed here.

## Fixes Required

### 1. Remove "Log New Note" from Support Notes Dashboard
- On the Support Notes dashboard (formerly Contact Notes, under Compliance), there's a "Log New Note" option/tab/button
- REMOVE it — notes are only logged from the SU profile, not from this dashboard
- This dashboard is for QA/compliance oversight only

### 2. Incidents & Risk Page — Reorder Sections
Reorder the sections on the Incidents & Risk page so actionable items are at the TOP and analytics/data at the BOTTOM:

**Top (in this order):**
1. Incidents Kanban (Open / Monitoring / Closed)
2. Welfare Concerns Kanban
3. Welfare Watch — Active Alerts
4. Abandonment Process — Active Cases

**Bottom (in this order):**
5. Incident trends/graphs
6. WC trends
7. LA Breaches
8. Any other charts/data/analytics

### 3. Eviction Risk → Rename to "Evictions"
- Rename the nav item and page heading from "Eviction Risk" to **"Evictions"**

### 4. Eviction Risk Assessment — Add SU Name Column
- In the Eviction Risk Assessment table/list, add a **"Name"** column showing the service user's name
- Currently only shows identifier + property — name is missing

### 5. NEW: Notices Issued Section (under Evictions)
- Add a NEW subsection under the Evictions page, BELOW the Eviction Risk Assessment section
- Heading: **"Notices Issued"**
- Show a table/list with demo data (2-3 entries):
  - SU ID/identifier
  - SU Name
  - Property
  - Support Staff
  - Date Issued
  - Notice Length (e.g. "28 Days", "14 Days", "7 Days", "Immediate")
  - Category/Reason (e.g. "Persistent ASB", "Rent Arrears", "Breach of Licence")
  - Countdown (days remaining — e.g. "18 days remaining", "OVERDUE — 3 days past")
  - Eviction Date (date issued + notice length, starting from the day after issue date)
- Overdue items should be highlighted in red
- Demo data: make one entry in-date, one close to deadline, one overdue

### 6. NEW: Warnings Section on Incidents & Risk
- Add a NEW section on the Incidents & Risk page (between the kanbans and the analytics sections)
- Heading: **"Warnings"**
- Show a table/list with demo data (2-3 entries):
  - SU Name
  - Warning Type (e.g. "Formal Warning", "Final Warning", "Verbal Warning")
  - Logged By (staff name)
  - Date Logged
  - Status: "Needs Approval" / "Approved" / "Closed"
  - "Needs Approval" items should have an "Approve" button (toast: "Warning approved")
- Demo data: one needing approval, one approved, one closed

## Rules
- DO NOT change formatting, styling, or layout of anything not listed above
- Keep ALL existing functionality working
- Keep mobile responsiveness
- Commit with descriptive message
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: Fixes batch 3 — removed log note, reordered incidents page, evictions rename, notices issued, warnings section" --mode now

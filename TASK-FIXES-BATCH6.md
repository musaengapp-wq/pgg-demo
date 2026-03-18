# TASK — Frontend Fixes Batch 6 (16 March 2026)

## Context
Single-file frontend MVP (`index.html`, all CSS/JS inline).
PGG = compliance system for UK care providers.
DO NOT change any formatting, styling or layout of things not listed here.

## Changes Required

### 1. Individual Staff Profile — Expand Sections
Under Staff Performance, when you click on a staff member's name it opens their individual profile. Currently it shows Performance Feedback + Documents & Meeting Notes.

**A) Performance Feedback — add who logged it:**
- Each feedback entry must show: **date/time** + **who logged it** + **their role**
- Demo data examples: "Katie Cook — Support Service Manager", "Philip Mills — Housing Manager"
- Any manager from any department can leave feedback

**B) Documents & Meeting Notes — update categories:**
- Rename/restructure the document categories to:
  - TL One-to-Ones
  - SM Supervisions
  - Disciplinary Meetings
  - Capability / Performance Management Meetings
  - Other
- REMOVE "Team Meeting Minutes" if it exists — doesn't belong on individual profiles
- Keep existing upload functionality

**C) Add NEW sections (with demo data):**

**QA Score:**
- Show average Beacon AI quality score (e.g. "Average QA Score: 3.2 / 4.0")
- Show last 5 scores in a mini list (date + score)

**Training:**
- Table/list showing: Course Name, Status (Completed / In Progress / Overdue), Date Completed
- Demo: "Safeguarding Level 2 — Completed — 15/01/2026", "Fire Safety — Overdue — Due 01/03/2026", "Manual Handling — In Progress"
- Overdue items in red

**Attendance:**
- Summary: "Days absent this quarter: 3" / "Sickness episodes: 1"
- Small list of recent absences with dates and reason

**Performance Scores:**
- Show 3-4 KPIs with scores, e.g.:
  - Contact note compliance: 94%
  - Support plan reviews on time: 100%
  - Average response time: 2.1 days
  - Caseload capacity: 8/10

**All new sections should be collapsible** (same pattern as SU profile — heading + ▼ toggle, default collapsed)

### 2. SM Dashboard — Add Quick Access Links
On the Service Manager dashboard, add a **"Quick Access"** section (near the top, below stat boxes, above or beside Notifications/To-Do):
- Staff Performance → links to staff performance page
- Incidents & Risk → links to incidents page
- Evictions → links to evictions page
- Document Management → links to document management page
- Style as clean buttons or card links (match existing design)

## Rules
- DO NOT change formatting, styling, or layout of anything not listed above
- Keep ALL existing functionality working
- Keep mobile responsiveness
- Commit with descriptive message
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: Staff profiles expanded (QA, training, attendance, KPIs), SM quick access links added" --mode now

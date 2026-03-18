# TASK — Frontend Fixes Batch 2 (from Sar's Review 16 March 2026)

## Context
Single-file frontend MVP (`index.html`, all CSS/JS inline).
PGG = compliance system for UK care providers.
DO NOT change any formatting, styling or layout of things not listed here. Only change what's specified.

## Fixes Required

### 1. Renames — find and replace ALL instances
- "Leavers Notification" → **"Leaver's Form"** (everywhere — nav, headings, buttons, form titles, any JS text)
- "Moving Checklist" → **"New Resident Checklist"** (everywhere)
- "Contact Notes" → **"Support Notes"** (everywhere EXCEPT where it refers to the actual data type "contact note" in code logic — only change visible UI text/labels/headings/nav items)

### 2. Leaver's Form — Multi-Select Dropdown
- On the Leaver's Form (SU profile), the "Notification sent to" field needs to be a **multi-select dropdown**
- NOT checkboxes, NOT a single dropdown
- It should look like a clean dropdown, but when clicked, shows checkboxes inside so multiple can be selected
- Options: Accounts Team, Service Manager, Compliance Team
- Selected items should show as tags/chips inside the dropdown field
- When closed, shows selected items (e.g. "Accounts Team, Compliance Team")

### 3. Close (✕) buttons on ALL forms
- Every form that opens on the SU profile or anywhere else needs a **✕ close button** in the top right corner
- Check ALL forms: Log Incident, Log Welfare Concern, Log Complaint, Log Compliment, Upload Document, Support Plan Review, Reassign, New Referral, any others
- Some forms already have ✕ or Cancel — leave those alone
- Only ADD ✕ where it's missing
- Clicking ✕ takes user back to where they were before opening the form

### 4. To-Do Lists — Make Collapsible
- ALL to-do list sections (SW, TL, wherever they appear) should be **collapsible**
- Default: show heading with count (e.g. "My To-Do List (5)") and first 2 items only
- Click heading or a ▼ arrow to expand and see all items
- When expanded, click again to collapse back to 2 items
- This applies to every to-do list in the system

### 5. Service Manager Dashboard — Add To-Do List
- SM dashboard currently has NO to-do list
- Add one, positioned **next to / opposite the Notifications section** (split the area)
- Layout: Notifications on one side, To-Do on the other
- To-Do has two buttons:
  - **"Add Reminder"** — opens a simple form (title, date, notes) with toast "Reminder saved"
  - **"Assign Task"** — opens form with: staff dropdown (TLs + SWs), task description, due date. Toast "Task assigned"
- Show 2-3 demo tasks
- Collapsible (same as fix #4)

### 6. Compliance Homepage — Add To-Do List
- On the Compliance Homepage/Notifications page, split the area:
  - Left/one side: existing Notifications
  - Right/other side: new To-Do / Task List
- Same two buttons as SM:
  - **"Add Reminder"**
  - **"Assign Task"** — staff dropdown includes SMs, TLs, SWs
- Show 2-3 demo tasks
- Collapsible

### 7. TL Dashboard To-Do — Add Buttons
- The TL to-do list already exists and is at the top
- Replace the current "Add Task" button with TWO buttons:
  - **"Add Reminder"** — personal reminder (title, date, notes)
  - **"Assign Task"** — assign to team members (SW dropdown, task description, due date)
- Keep existing demo tasks

## Rules
- DO NOT change formatting, styling, or layout of anything not listed above
- DO NOT rename or restructure anything not specified
- Keep ALL existing functionality working
- Keep mobile responsiveness intact
- Commit with descriptive message
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: Fixes batch 2 — renames, multi-select dropdown, close buttons, collapsible to-dos, SM+Compliance to-do lists, TL buttons" --mode now

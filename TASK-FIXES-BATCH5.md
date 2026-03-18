# TASK — Frontend Fixes Batch 5 (16 March 2026)

## Context
Single-file frontend MVP (`index.html`, all CSS/JS inline).
PGG = compliance system for UK care providers.
DO NOT change any formatting, styling or layout of things not listed here.

## Fixes Required

### 1. WC + Incident Forms — Make Editable on Kanban Detail View
When a manager clicks into a WC or Incident card on the Incidents & Risk kanban, the detail modal opens. Currently the original SW-submitted content is NOT editable.

**Fix:** Make the SW-submitted fields (description, witnesses, details, police ref, etc.) **editable text fields** (not read-only) when viewed from the kanban detail modal. The manager should be able to:
- Edit any field the SW originally filled in
- Add manager observations (this may already work)
- Set to monitoring / close with reasons (this may already work)

Apply this to BOTH:
- Incident detail modal (when clicking incident kanban cards)
- Welfare Concern detail modal (when clicking WC kanban cards — `showConcernDetail`)

### 2. TL Dashboard — Escalations Click-Through to Editable Form
On the TL Dashboard, there's an escalations/notifications section showing recently opened incidents and WCs from their team.

**Fix:** When a TL clicks on an escalation item:
- It should open the full incident/WC form
- The SW-submitted content should be **editable** (TL can fix errors — wrong police ref, missing info)
- The manager observations section should be **read-only / hidden** for TLs (they can't add observations)
- Show a toast/note: "You can edit staff-submitted content. Manager observations are restricted."

If the escalation items are not already clickable, make them clickable with this behaviour.

### 3. TL Dashboard Escalation Labels
- Change any "Awaiting TL review" labels to just **"Recently opened"** or **"New incident from your team"**
- The TL is being NOTIFIED, not asked to review — review is the manager's job. TL just fixes content errors.

## Rules
- DO NOT change formatting, styling, or layout of anything not listed above
- Keep ALL existing functionality working
- Keep mobile responsiveness
- Commit with descriptive message
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: Editable incident/WC forms on kanban, TL click-through with edit permissions" --mode now

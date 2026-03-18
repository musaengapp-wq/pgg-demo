# TASK — Frontend Fixes Batch (from Sar's Review 16 March 2026)

## Context
Single-file frontend MVP (`index.html`, all CSS/JS inline).
PGG = compliance system for UK care providers.
DO NOT change any formatting, styling or layout of things not listed here. Only change what's specified.

## Fixes Required

### 1. Leaver's Form — "Notification sent to" revert to dropdown
- On the SU profile Leaver's Form, the "Notification sent to" field was changed from a dropdown to checkboxes
- REVERT it back to a **dropdown** (it was a dropdown before and shouldn't have been changed)
- Keep the same options: Accounts Team, Service Manager, Compliance Team

### 2. Reassign button — move position on SU profile
- The "Reassign" button on the SU profile needs to move
- Move it to the **top area of the SU profile**, in the personal details box area, on the **opposite side** from the SU name
- It should be visible but not so close to other buttons that it could be clicked accidentally
- Keep all existing functionality (temp/permanent options, TL = temp only)

### 3. TL Dashboard — move To-Do List + Notifications to top
- On the Team Leader dashboard, move the **To-Do List** and **Notifications** sections to the TOP
- They should sit directly below the stat boxes at the top
- ABOVE the My Team / Support Staff Overview / Team QA Summary sections
- Keep all existing content, just reorder

### 4. SW Dashboard — move To-Do List to top
- On the Support Worker dashboard, move the **To-Do List** section to the TOP
- It should sit below the personal info/greeting section
- ABOVE My Service Users and Check-in/Check-out sections
- Keep all existing content, just reorder

### 5. Messaging — restore on ALL dashboards
- The internal messaging feature (mail icon with badge in top nav, slide-out panel) has disappeared from dashboards
- Ensure the messaging icon + panel exists and works on ALL of these:
  - Homepage
  - SW Dashboard
  - TL Dashboard
  - Service Manager Dashboard
  - Compliance pages
- Each should have Inbox (demo messages) + Send Message functionality
- Send message form: To (staff dropdown), Subject, Message, checkbox "Add to recipient's To-Do list"
- Mail icon should show badge with unread count (e.g. "3")

### 6. G (Guidance) button — add to ALL forms
- Currently the G guidance button was added to incident and WC forms
- Add the same G button to ALL other forms in the system:
  - Leaver's Form
  - Contact Note form
  - Support Plan Review form (if exists)
  - Upload Document form
  - Any other form that has a submit button
- Same behaviour: green G icon next to form title, toggles inline guidance panel
- Guidance text: "Quick guidance notes — configurable per organisation" (placeholder)

## Rules
- DO NOT change formatting, styling, or layout of anything not listed above
- DO NOT rename or restructure anything not specified
- Keep ALL existing functionality working
- Keep mobile responsiveness intact
- Commit with descriptive message
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: Frontend fixes batch — dropdown revert, reassign move, to-do reorder, messaging restore, G button on all forms" --mode now

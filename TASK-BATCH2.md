# PGG MVP — Build Batch 2 (New Features)

This is a single-file frontend demo: `index.html` (all CSS/JS inline).
DO NOT break existing functionality. Commit after each major change.
These are FRONTEND MOCKUPS — demo data is fine, no real backend needed.

## New Features

### 1. Current / Archived Service Users Split
- Split the Service Users section into TWO tabs/views: **Current Service Users** and **Archived Service Users**
- Current = active SUs getting support now (default view)
- Archived = discharged/moved on SUs
- RBAC rules (show as demo — visual only):
  - SW: only sees SUs on their caseload + temporarily reassigned
  - TL: sees own caseload + team members' SUs
  - Service Manager + all managers: sees ALL current + ALL archived
  - Archived tab: managers only (show a lock/permission message if SW tries to access)

### 2. Leavers Dashboard + Notification Workflow
- **New nav item under Compliance: "Leavers"**
- Shows a list/kanban of submitted leavers notifications awaiting compliance sign-off
- Each card shows: SU name, leave date, reason, submitted by, status (Pending Approval / Approved / Archived)
- Click opens the full leavers notification with all fields
- **On SU Profile** — enhance existing "Leavers Notification" form:
  - Add: Forwarding contact details / forwarding address fields
  - Add: Keys handed in (Yes/No toggle)
  - "Completed by" auto-populated (show logged-in user name)
  - "Leavers Note" field — note that this also creates a contact note (show a small info text: "This note will also appear as a final contact event")
  - Notification sent to: show checkboxes for Accounts Team, Service Manager, Compliance Team

### 3. Reassignment System
- **On SU Profile:** Enhance existing "Reassign" button with two options:
  - **Temporary** — shows: new SW dropdown, start date, end date, reason
  - **Permanent** — shows: new SW dropdown, effective date, reason
- **On Service Manager Dashboard:** Add a "Bulk Reassign" section/button
  - Select multiple SUs via checkboxes → reassign to a new SW
  - Same temp/permanent options
- **TL Dashboard:** Reassign button shows ONLY temporary option (no permanent)

### 4. To-Do List on TL Dashboard
- Add a **To-Do List** section on the Team Leader dashboard
- Demo items showing assigned tasks with: task description, assigned by, due date, status (Pending/Overdue/Complete)
- Overdue tasks highlighted in red
- "Add Task" button (for managers assigning tasks — show the form as mockup)

### 5. Internal Messaging — Add Send Function to ALL Dashboards
- Currently messaging may only be on some dashboards
- Ensure the mail icon + slide-out messaging panel exists on:
  - SW Dashboard
  - TL Dashboard  
  - Service Manager Dashboard
  - Compliance Dashboard
  - Homepage
- Each should have both "Inbox" and "Send Message" functionality
- Send message form: To (staff dropdown), Subject, Message, checkbox "Add to recipient's To-Do list"

### 6. Closed Incidents — 14-Day Visibility
- On the Incidents & Risk kanban, "Closed" column items should show a subtle label: "Visible for X more days" (demo with "Visible for 11 more days", "Visible for 3 more days" etc.)
- After 14 days they'd disappear (just show the label for now — no actual timer needed)

### 7. WC ↔ Incident Auto-Linking
- On the Welfare Concern detail/form, add a field: "Related Incident: INC-XXX" (clickable link, show on one demo WC)
- On the Incident detail/form, add a field: "Originated from: WC-XXX" (clickable link, show on one demo incident)
- Visual cross-reference between the two

### 8. Regulatory Notifications Dashboard (Placeholder)
- **New nav item under Compliance: "Regulatory Notifications"**
- Show a placeholder dashboard with:
  - Section header: "Regulatory Notifications"
  - Subtext: "Auto-generated notifications for CQC, Ofsted (Reg 40), and Local Authority reporting"
  - A demo kanban or list: Pending Review / Approved / Sent
  - One or two demo items showing: incident reference, notification type, regulatory body, deadline countdown, status
  - "Send" button (greyed out / mockup)
  - Info text: "Notifications are auto-generated based on incident type configuration"

## Commit Strategy
- Commit after every 2-3 related changes
- Use descriptive commit messages
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: PGG Batch 2 complete — Current/Archived split, Leavers dashboard, reassignment, to-do lists, messaging, regulatory notifications" --mode now

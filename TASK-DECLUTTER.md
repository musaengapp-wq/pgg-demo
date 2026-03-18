# TASK — SU Profile Declutter + Dashboard Cleanup

## Context
Single-file frontend MVP (`index.html`, all CSS/JS inline).
PGG = compliance system for UK care providers.
The SU profile and dashboards have too many sections/buttons visible at once. This task reorganises them to be cleaner and more manageable.

## IMPORTANT
- DO NOT change any existing functionality
- DO NOT remove any features — just reorganise/collapse them
- DO NOT change colours, fonts, or the overall design language
- Keep mobile responsiveness

## SU Profile Changes

### 1. Group Action Buttons
Currently there are many individual buttons scattered on the SU profile (Log Incident, Log WC, Log Complaint, Log Compliment, Leaver's Form, Upload Document, Edit Personal Details, Edit Next of Kin, etc.)

Replace with **3 grouped dropdown buttons** near the top of the profile (below the header/personal info area):

**📝 Forms** — click to show dropdown menu:
- Log Incident
- Log Welfare Concern
- Log Complaint
- Log Compliment
- Leaver's Form

**📄 Documents** — click to show dropdown menu:
- Upload Document
- View Support Plans
- View Risk Assessments
- View All Documents

**👤 Profile** — click to show dropdown menu:
- Edit Personal Details
- Edit Next of Kin
- About Me Profile (AMP)

Each dropdown should:
- Show on click (not hover — mobile friendly)
- Close when clicking elsewhere
- Have clear labels
- Keep the same onclick actions as the original buttons

Remove the original scattered buttons and replace with these 3 grouped ones.

### 2. Make ALL Content Sections Collapsible
Every section on the SU profile should be collapsible with a ▼/▲ toggle arrow next to the heading.

**Default collapsed (show heading + summary only):**
- **Support Notes** — show "Support Notes (X)" count + last 2 notes preview. Click heading to expand full list.
- **Support Documentation** — show "Support Documentation" with counts (e.g. "3 Plans · 2 Risk Assessments · 5 Documents"). Click to expand subsections.
- **Manager Feedback** — show count only. Click to expand.
- **Activity Log** — show "Activity Log" + last 3 entries. Click to expand full log.

**Default expanded (these are key working sections):**
- **Support Needs** — expanded by default (this is what SWs actively work with)
- **Progress Tracker** — expanded by default

Each collapsible section:
- Click heading or ▼ arrow to toggle
- Smooth transition (CSS transition on max-height or similar)
- Remember: heading always shows the count so users know there's content inside

### 3. Support Notes — Limit Default View
- Show only the **last 3 notes** by default
- Add a "View all (X)" link/button to expand the full list
- Notes should show in a compact format: date, SW name, first line of note
- Click individual note to expand full text

## Dashboard Changes (TL, SW, SM)

### 4. Make Dashboard Sections Collapsible
Apply the same collapsible pattern to dashboard sections:

**SW Dashboard:**
- To-Do List — already collapsible ✅
- My Service Users — make collapsible (default expanded)
- Check-in/Check-out — make collapsible (default collapsed)
- Mileage — make collapsible (default collapsed)
- QA Stats — make collapsible (default collapsed)

**TL Dashboard:**
- To-Do + Notifications — already at top, already collapsible ✅
- My Team — make collapsible (default expanded)
- Team QA Summary — make collapsible (default collapsed)
- Meetings — make collapsible (default collapsed)

**SM Dashboard:**
- Notifications + To-Do — already done ✅
- Team Overview — make collapsible (default expanded)
- Open Incidents — make collapsible (default expanded)
- Staff Performance — make collapsible (default collapsed)
- Compliance Score — make collapsible (default collapsed)

### Implementation Notes
- Use a consistent pattern: `<div class="collapsible-section">` with heading + toggle
- ▼ when collapsed, ▲ when expanded
- Add `cursor: pointer` on section headings
- Transition: smooth slide (not instant show/hide)
- Section heading shows count where applicable

## Rules
- DO NOT remove any content or features
- DO NOT change the visual design/theme
- Only reorganise and add collapsible behaviour
- Commit with descriptive message
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: SU profile declutter + dashboard collapsible sections — grouped buttons, collapsible content, cleaner layout" --mode now

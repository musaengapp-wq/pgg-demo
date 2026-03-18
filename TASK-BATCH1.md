# PGG MVP — Build Batch 1 (Quick Wins + Restructure)

This is a single-file frontend demo: `index.html` (~11,600 lines, all CSS/JS inline).
DO NOT break existing functionality. Commit after each major change.

## Quick Wins (Renames & Fixes)

### 1. Rename "Pen Portrait" → "AMP" (About Me Profile)
- In the SU profile documents section, any reference to "Pen Portrait" should say "AMP" or "About Me Profile"

### 2. Contact Notes Dashboard Glitch Fix
- Bug: When first navigating to the Contact Notes dashboard, a "Log a New Contact Note" form briefly flashes under "Recent Notes" before disappearing
- User has to click to AI QA Review tab and back for Recent Notes to show properly
- Fix: ensure Recent Notes shows immediately on load, no flash of the log form

### 3. Remove Team Leaders from SW Dashboard "View As" dropdown
- The "View As" dropdown on the Support Worker dashboard should NOT list Team Leaders
- TL profiles are accessed from the TL Dashboard only

### 4. SU List View — Column Changes
- **Remove:** "Support Plan" column
- **Remove:** "Status" column  
- **Add:** "Identifier" column (between Name and Location) — placeholder showing "DOB" or "NI Number" as example data
- Keep: ID, Name, Location/Property Name, Support Staff, Team Leader, Last Note

### 5. CFC → WC rename check
- Search entire file for any remaining "CFC" references and change to "WC" (Welfare Concern)
- Check: "CFC Trend" → "WC Trend", "Open CFC" → "Open WC", "Overdue CFC" → "Overdue WC"

## SU Profile Restructure

### 6. Support Documentation Section (NEW structure on SU profile)
Currently documents are in one flat list. Restructure to:

**Support Documentation** (new section header on SU profile)
  - **Support Plans** (subsection) — show original plan + subsequent reviews, each clickable to view/print
  - **Risk Assessments** (subsection) — show original + updates, multiple versions. RISK ASSESSMENTS WERE MISSING — add them

**Documents** (general section — below Support Documentation)
  - Keep everything else here: AMP, referral, needs assessment, licence agreement, moving checklist, proof of address
  - Remove support plans from this section (they moved up)

### 7. Rename "Support Plan" section → "Support Needs"
- The section on SU profile that shows extracted needs with review/update buttons should be called "Support Needs" not "Support Plan"
- Progress Tracker sits directly underneath Support Needs

### 8. Move Missing Data Alerts
- Currently buried further down the SU profile
- Move to **top right** of the profile, near sign-up date / property info area

### 9. Welfare Concern Form on SU Profile — MAJOR FIX
- Currently: clicking "Log Welfare Concern" on SU profile shows a "Concern Log" dashboard view with stats (total concerns, pending review, escalated to incident) — THIS IS WRONG
- Should work EXACTLY like the incident form: click → opens FORM only
- Form structure:
  - **Concern Type** dropdown: "General Concern" / "Safeguarding Concern"
  - If Safeguarding selected, show guidance text at top: "Complete this form if you're concerned that a service user is being harmed or is at risk of harm from: physical abuse, domestic violence/abuse, sexual abuse, psychological/emotional abuse, financial/material abuse, modern slavery, discriminatory abuse, neglect/acts of omission, self-neglect."
  - Fields: Details/description of concern, Any other relevant information, SU background/needs, Witnesses, Immediate action taken
  - ℹ️ Policy link icon (same as incident form)
  - Submit button + Save & Close button

### 10. Welfare Concern Kanban — Make Clickable
- The Welfare Concern kanban (under Incidents & Risk) is NOT clickable — incidents kanban IS
- Make it clickable: clicking a card opens the full welfare concern form (same layout as when logged from SU profile)
- Manager can: edit form content, add observations, set review date, set to monitoring (with reason), close (with reason)

### 11. Upload Document Button on SU Profile
- Add "Upload Document" button in the Documents section
- Document Type dropdown with categories: Personal Details, Proof of Address, Benefits Letter, Miscellaneous
- If "Miscellaneous" selected → must show a text field to name it (can't just be "miscellaneous")
- Optional: review date field

### 12. Contact Note Type Dropdown
- Add a "Type" dropdown to the contact note form on SU profile
- Options: Support Session, Third Party Contact, Handover Note
- This is the START of making contact note content flexible per setting

## Commit Strategy
- Commit after every 2-3 related changes
- Use descriptive commit messages
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: PGG Batch 1 complete — renames, SU profile restructure, welfare concern form, document upload, contact note types" --mode now

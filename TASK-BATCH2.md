# TASK — Batch 2: Beacon QA Workflow Redesign

## File: index.html (single file, all CSS/JS inline)

## Items:

### 1. Remove Verify + Accept Buttons from Support Notes QA Dashboard
The Support Notes dashboard (under Compliance) currently shows "Verify" and "Accept" buttons on the QA review view. REMOVE both buttons from this dashboard. This is a management VIEW only — managers don't verify or accept notes.

### 2. Add Verify Step to Log Support Note Form (SU Profile)
On the SU Profile, when a support worker fills in the "Log Support Note" form, add a verify checkbox/disclaimer BEFORE the Submit button.

**Exact wording:**
> ☐ "I confirm that this is an accurate and factual record of the support activity that took place. I understand that this note will be processed by Beacon for quality assurance, and that the original version will be retained."

- This checkbox must be ticked before the Submit button becomes active/clickable
- Style it clearly — maybe a bordered box with the text, and a checkbox to the left
- Submit button should be greyed out / disabled until verified

### 3. Add "Accept & Submit Published Version" Mockup
After a note has been submitted and "processed by Beacon", the SW needs to see the Published Version and accept it. 

**On the SW Dashboard**, add a notification-style item in the notifications/to-do area:
- "You have 2 notes awaiting acceptance" (demo data)
- Clickable — shows the published version with an "Accept & Submit Published Version" button

**On the SU Profile** under Recent Support Notes, for notes that have been QA'd but not yet accepted, show:
- The Beacon Published Version text
- An "Accept & Submit Published Version" button
- A small label: "Beacon QA Score: 3.8/4.0" — but ONLY if visible to the logged-in role
  - If logged in as SW: do NOT show QA score (management only by default)
  - If logged in as Admin/Manager: show QA score

## IMPORTANT:
- The QA Score and Feedback should NOT be visible on any SW-facing view
- The Support Notes QA Dashboard should still show QA scores and feedback (management view)
- Do NOT remove View Original 🔒 Management Only — that stays where it is

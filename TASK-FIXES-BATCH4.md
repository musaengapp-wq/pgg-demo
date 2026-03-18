# TASK — Frontend Fixes Batch 4 (16 March 2026)

## Context
Single-file frontend MVP (`index.html`, all CSS/JS inline).
PGG = compliance system for UK care providers.
DO NOT change any formatting, styling or layout of things not listed here.

## Fixes Required

### 1. SM Dashboard — Move Notifications + To-Do to Top
- On the Service Manager dashboard, the Notifications and To-Do List sections are at the BOTTOM
- Move them to the TOP — directly below the stat boxes
- They should sit ABOVE Team Overview and Compliance Score sections
- Keep the split layout (Notifications on one side, To-Do on the other)
- Keep all existing content and functionality

### 2. Move ALL Analytics OFF Incidents & Risk Page
- On the Incidents & Risk page, there are analytics/charts/data sections:
  - Incident trends/graphs
  - WC trends
  - LA Breaches quarterly trend
  - Any other charts/data/analytics
- REMOVE all of these from the Incidents & Risk page
- MOVE them into the "Incident Analysis" page (under Analytics & Reports in the nav)
- The Incidents & Risk page should ONLY have actionable items remaining (kanbans, Warnings, Welfare Watch, Abandonment)

### 3. Rename "Incident Analysis" → "Incident & Risk Analysis"
- Under Analytics & Reports in the nav, rename "Incident Analysis" to **"Incident & Risk Analysis"**
- Update the nav item text, page heading, and any other references
- This page now contains ALL the analytics that were moved from Incidents & Risk

## Rules
- DO NOT change formatting, styling, or layout of anything not listed above
- Keep ALL existing functionality working
- Keep mobile responsiveness
- Commit with descriptive message
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: SM dashboard reorder, analytics moved to Incident & Risk Analysis, rename done" --mode now

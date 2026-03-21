# TASK — Batch 3: View All Support Notes Page

## File: index.html (single file, all CSS/JS inline)

## Items:

### 1. Add "View All Support Notes →" Button on SU Profile
Under the "Recent Support Notes" section on the SU Profile, add a button/link: **"View All Support Notes →"**

When clicked, it should navigate to a new full-page view (add a new data-page section called "su-all-notes" or similar).

### 2. Build the "All Support Notes" Full Page View
Create a new page/section that shows ALL support notes for a specific service user. This is a SEPARATE FULL PAGE, not a slide-out panel.

**Layout:**
- **Header:** "Support Notes — [SU Name]" with a "← Back to Profile" button
- **Filters bar:**
  - Date range: From [date picker] To [date picker]
  - Search: [text input] "Search by keyword..."
  - Filter by Support Worker: [dropdown]
  - "Print / Export" button (right-aligned)
- **Notes list** (chronological, newest first):
  - Each note shows:
    - Date + Time
    - Support Worker name
    - Published Version text (the Beacon-polished version)
    - Two buttons (right side):
      - 🔒 "View Original" — Management Only (only visible when logged in as Admin, hidden for SW login)
      - "View Feedback & QA Score" — Management Only by default (only visible when logged in as Admin)
  - Notes displayed in a clean card/row format
  - **Demo data:** Use 10-15 demo notes spanning different dates and support workers

### 3. Print Exclusion Rule
When the "Print / Export" button is clicked, show a print-preview style view that includes ONLY:
- Date | Support Worker | Published Support Note
- NO QA Score
- NO Beacon Feedback  
- NO Original Note
- Clean grid/table layout suitable for printing
- Add a "Print" button and "Close Preview" button

## IMPORTANT:
- This page must work on mobile (responsive)
- Use existing styling patterns from the rest of the app
- The "View Original" and "View Feedback" buttons should be HIDDEN (not just greyed out) when logged in as SW
- Add this new page to the nav system so the back button works properly

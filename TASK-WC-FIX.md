# TASK — Fix WC Kanban Clickability

## Problem
The Welfare Concern kanban cards on the Incidents & Risk page are NOT clickable. Users click on them and nothing happens. The `showConcernDetail()` function exists but the onclick handlers may not be firing properly.

## What to do
1. Open the live demo in a browser or test the HTML locally
2. Navigate to Incidents & Risk page
3. Find the Welfare Concerns section (recently added, below incidents)
4. Debug WHY clicking on WC cards doesn't trigger `showConcernDetail()`
5. Fix it — make sure every WC card opens the detail modal when clicked
6. Also check: does the `showConcernDetail` function work when called directly from console? If yes, it's a wiring issue. If no, the function itself needs fixing.
7. Test by opening the HTML in a browser and confirming clicks work

## Rules
- Keep ALL existing functionality working
- Commit with descriptive message
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: WC kanban cards now clickable on Incidents & Risk page" --mode now

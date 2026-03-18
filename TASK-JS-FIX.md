# TASK — Fix JavaScript Breaking (Nothing Clickable)

## Problem
After the last commit (declutter), the page loads visually but NOTHING is clickable — nav items, buttons, forms, nothing responds to clicks. This means there's a JavaScript error that's stopping all event handlers from working.

## What to do
1. Open index.html in a browser
2. Open the browser console (F12 → Console tab)
3. Look for JavaScript errors
4. Fix ALL errors so the page is fully interactive again
5. Test: nav items work, buttons work, forms open, dropdowns work
6. Make sure the declutter changes (grouped buttons, collapsible sections) STILL work after the fix

## Rules
- Fix the JS errors, don't remove features
- Keep ALL existing functionality
- Commit with descriptive message
- Push to GitHub when done

When completely finished, run this command to notify me:
openclaw system event --text "Done: Fixed JS errors — page fully interactive again" --mode now

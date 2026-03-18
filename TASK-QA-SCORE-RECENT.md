# TASK — Add QA Score to Recent Notes on Support Notes Dashboard

Work on: `/tmp/pgg-demo/index.html`

## What to fix

On the Support Notes Dashboard, under the "Recent Notes" section, when you expand/click on a note, the QA Score is NOT showing. It needs to be there.

Find where the Recent Notes are rendered on the Support Notes Dashboard. Each expanded note should show the QA Score (e.g. "QA Score: 3.2/4") — same style as on the Beacon AI QA Review page:
- Bold, slightly larger text
- Colour coded: green for 3-4, amber for 2, red for 1
- Shown BEFORE the feedback text

The QA score data should already be available in the note data objects (look for qaScore property).

Do NOT touch any other sections — only the Recent Notes on the Support Notes Dashboard.

After completing, run:
cd /tmp/pgg-demo && git add -A && git commit -m "Add QA Score to Recent Notes on Support Notes Dashboard" && git push -f origin main

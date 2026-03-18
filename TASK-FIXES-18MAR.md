# TASK — 3 Fixes (18 March)

Work on: `/tmp/pgg-demo/index.html`
This is a large single-file HTML app with all CSS/JS inline.

## Fix 1: Remove "View Original" toggle from Beacon AI QA Review page

On the Beacon AI QA Review section (the page/tab where you see Beacon Published Version, AI Feedback etc), there is currently a "View Original (Management Only)" toggle with a 🔒 icon. REMOVE it from this page entirely — it makes no sense here because the original note is already visible above the published version.

## Fix 2: Add "View Original (Management Only)" toggle to 3 locations

Add a "View Original" toggle (with 🔒 icon and "Management Only" label, same style as what was on the QA Review page) to these locations:

1. **SU Profile** — on each support note shown on the Service User profile. When toggled, shows the original SW note underneath the published version.
2. **Audit Dashboard** — on support notes that appear within the audit embedded SU view. Same toggle pattern.
3. **Support Notes Dashboard** — on the Recent Notes section. Each note in the recent notes list should have the toggle.

The toggle should show/hide the original note with the amber background styling (same as was used on the QA review page).

## Fix 3: Add QA Score to AI Feedback section on Beacon AI QA Review page

On the Beacon AI QA Review page, find the "AI Feedback" section within a note. Currently it just shows the feedback text. Change it so:
- **QA Score** is shown FIRST (e.g. "QA Score: 3.2/4" or whatever the demo score is)
- Then the AI Feedback text below it

Make the QA Score visually prominent (bold, slightly larger, maybe with a colour indicator).

---

Keep existing look and feel. Don't change fonts, colours, or formatting.

After completing ALL 3 fixes, run:
cd /tmp/pgg-demo && git add -A && git commit -m "Fix: move View Original to correct locations, add QA Score to AI Feedback" && git push -f origin main

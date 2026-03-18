# TASK — SW Dashboard Expanded Check-In/Check-Out

Work on the file: `/tmp/pgg-demo/index.html`

This is a large single-file HTML app (~14000+ lines) with all CSS and JS inline.

## What exists already
The Support Worker dashboard already has a basic check-in/check-out section. Search for "Check-In" or "Lone Working" in the SW dashboard area.

The Team Leader dashboard already has an EXPANDED check-in/check-out view with:
- Active check-ins panel (who is checked in, where, elapsed time)
- Check-in history (recent entries with timestamps)
- Overdue alerts for lone working
- Location and notes fields

## What to add
Add a similar expanded view to the **Support Worker dashboard**, but scoped to the SW's OWN check-ins only (they don't see other staff). Include:

1. **My Active Status** — am I currently checked in? Where? How long? (show elapsed time)
2. **My Recent History** — last 5-10 check-in/check-out entries with timestamps, location, duration
3. **Location field** — when checking in, capture where they're going (property address or "Office")
4. **Notes field** — optional notes (e.g. "Visiting SU at 26 Moorgate Street, expected 1hr")
5. **Lone working alert** — if checked in as lone working for > 2 hours, show amber/red warning on their own dashboard

Add demo data:
- Show the SW (Megan Thorne / Emma — whoever the current demo SW is) as currently checked in at a property
- 3-4 recent completed check-in/out entries
- One previous lone working entry

Match existing styles exactly — same colours, fonts, card styles, spacing.

After completing, run: cd /tmp/pgg-demo && git add -A && git commit -m "Add expanded check-in/check-out view to SW dashboard"

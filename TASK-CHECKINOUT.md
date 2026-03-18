# TASK — TL Check-In/Check-Out Expanded View

Work on the file: `/tmp/pgg-demo/index.html`

## TL Check-In/Check-Out Expanded View

The basic check-in/check-out with staff selector already exists on the TL Dashboard. It needs expanding:

Currently there are three check-in/check-out types:
- SW (self) — support worker checks themselves in/out
- TL (with staff selector) — team leader checks in with a specific staff member
- Lone Working (with staff selector) — for lone working situations

The expanded view needs:
1. **Active check-ins panel** — show who is currently checked in, where they are, how long they've been checked in (elapsed time display)
2. **Check-in history** — recent check-ins/check-outs with timestamps, staff name, location, duration
3. **Overdue check-ins** — if someone has been checked in for too long (e.g. lone working > 2 hours without update), highlight in red/amber as an alert
4. **Location field** — when checking in, should capture where the staff member is going (property address or "Office")
5. **Notes field** — optional notes on check-in (e.g. "Visiting SU at Moorgate Street, expected 1hr")

Add some demo data showing:
- 2-3 staff currently checked in at different locations
- A few recent completed check-in/out entries
- One overdue lone working check-in (highlighted as alert)

Keep the existing look and feel. Match existing styles, colours, and formatting.

Commit with message: "Expand TL check-in/check-out view with active panel, history, and overdue alerts"

# TASK — Two Queued Items

Work on the file: `/tmp/pgg-demo/index.html`

## 1. Property Auto-Fill on New Resident Checklist

When a New Resident Checklist is opened from a Service User's profile, the property/location field should auto-populate from the SU's profile data (their assigned property). Don't make the user type it in manually.

Look at how the New Resident Checklist is currently implemented and find where the SU's property info is stored. Auto-fill it into the checklist form.

## 2. Expenses Approval Visual Flow

On the Staff Expenses tab, add a visual workflow showing the approval stages:

**Flow:** SW Submits → Pending TL Approval → Pending SM Sign-off → Approved / Denied / Amended

- Show the current status with a visual indicator (like the kanban cards or a progress stepper)
- Each stage should be visually distinct (pending = amber, approved = green, denied = red, amended = blue)
- When TL or SM clicks on a pending expense, they should see the form as submitted with options to: Approve, Deny, or Amend
- Amendment must show WHAT was changed
- Add a few demo expense entries at different stages so Sar can see the flow

Keep the existing look and feel — don't change fonts, colours, or formatting style. Match what's already there.

Commit with message: "Add property auto-fill on New Resident Checklist + expenses approval workflow"

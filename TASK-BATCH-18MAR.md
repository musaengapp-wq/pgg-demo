# TASK — Batch 18 March

Work on the file: `/tmp/pgg-demo/index.html`
This is a large single-file HTML app with all CSS/JS inline.

## 1. Move Support Notes underneath Support Documentation in nav
In the sidebar navigation, move the "Support Notes" item so it sits directly underneath "Support Documentation". Keep everything else in the same order.

## 2. Move Staff Performance underneath Evictions in nav
In the sidebar navigation, move "Staff Performance" so it sits directly underneath "Evictions". Keep everything else in the same order.

## 3. Fix TL Dashboard Staff Performance quick access button size
On the Team Leader Dashboard, there's a "Staff Performance" quick access button/link that is full width of the screen. It needs to match the size of the other quick access buttons — small rectangle, not full width. Look at how the other quick access buttons are sized on the SM Dashboard and match that pattern.

## 4. Logo text cleanup
Find the logo/branding area (likely in the sidebar or header). Make these changes:
- Remove "Governance Group" text that appears under/near the logo
- Change "Compliance Infrastructure as a Service" → "Compliance Infrastructure"
- Keep the logo image itself as-is

## 5. Beacon QA flow rework on Support Notes dashboard
Find the AI QA review section on the Support Notes dashboard and make these changes:
- Rename "AI Reframed Version" → "Beacon Published Version"
- In the "AI Feedback" section: show the QA Score FIRST (the number), then the feedback text below it
- Remove the "Accept Reframe" button — replace with just "Accept" 
- Remove the "Staff AI QA Opt-In" / "Opted into Auditron Proofread" toggle at the bottom
- Add a brief explanatory line about the flow, something like: "Each note is scored by Beacon QA, then polished for spelling, grammar and professionalism. The Beacon Published Version preserves the original meaning — only SPAG and presentation are improved."

## 6. "View Original" toggle on Support Notes
On the Support Notes dashboard, next to each note that shows the Beacon Published Version, add a "View Original" toggle/link. When clicked, it should show/hide the original SW note underneath. Add a visual indicator that this is management-only (e.g. a small 🔒 icon next to it, or style it with a subtle "Management Only" label).

## 7. Remove HB payment status from eviction risk assessment
Find the eviction risk assessment section and remove any "HB in payment" / "HB not in payment" fields or indicators. This was Greenbridge-specific and not universal.

---

Keep the existing look and feel — don't change fonts, colours, or formatting style. Match what's already there.

After completing ALL changes, run:
cd /tmp/pgg-demo && git add -A && git commit -m "Batch 18 Mar: nav moves, logo cleanup, Beacon QA rework, View Original toggle, HB removal"

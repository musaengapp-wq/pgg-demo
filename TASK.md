# TASK: Fix Service User Profile Mobile View

## File: `/tmp/pgg-demo/index.html`

Fix the mobile responsiveness of the Service User Profile page (id="p-su-profile"). Test at 375px width.

## Issues to Fix

### 1. Profile Header + Missing Data Alerts Layout
- Around line 3252, there's a flex container: `<div style="display:flex;gap:14px;align-items:flex-start;flex-wrap:wrap">`
- The Missing Data Alerts card has `flex:0 0 280px` — this is too wide on mobile (375px screen minus padding)
- **Fix:** Add a `@media (max-width: 768px)` rule that makes both children stack vertically (full width). Override the inline `flex:0 0 280px` on `#sup-missing-alerts-card` with `flex: 1 1 100% !important` at mobile breakpoint.

### 2. Profile Header Content (sup-header)
- The header rendered by `loadSUProfile()` JS function shows avatar, name, status badges, personal details, and action buttons
- On mobile the name gets truncated ("A. Rahu...") 
- **Fix:** Ensure the profile header content wraps properly. Look for the JS function `loadSUProfile` and check how the header HTML is generated. The avatar + name + badges row needs to stack or wrap on mobile. Add CSS rules for `.sup-header` children to be `flex-wrap: wrap` and full width on mobile.

### 3. Contact Activity + Incidents Side-by-Side
- There's a two-column grid/flex layout showing Contact Activity on the left and Incidents/Concerns/Alerts/Cases/Welfare Watch tabs on the right
- On mobile these should stack vertically (full width each)
- Look for the container that holds these two sections and add mobile stacking rules

### 4. SU Selector Row
- The selector row with dropdown + search input should stack on mobile
- Class is `.sup-selector` — make it flex-wrap or flex-direction: column on mobile

### 5. Support Needs Grid
- The support needs categories (Therapeutic Support, Health & Well-being, etc.) display in a 2-column grid
- Make sure this works on mobile — 1 column on very small screens

## Rules
- Add all CSS fixes in the existing `@media (max-width: 768px)` block or create targeted rules
- Use `!important` where needed to override inline styles
- Don't change the desktop layout — only mobile
- Test that existing functionality still works (collapsible sections, action groups, etc.)
- Keep changes minimal and surgical — CSS only where possible

## After fixing, commit with message "fix: mobile responsive SU profile layout"

# TASK — Welfare Concern Kanban on Incidents & Risk Page

## Context
Single-file frontend MVP (`index.html`). PGG = compliance system for UK care providers.
The Incidents & Risk page currently shows ONLY the incidents table. There's no Welfare Concern section visible on this page.

## Problem
The WC kanban cards with `showConcernDetail()` onclick exist in the code (line ~10046, `cfcCard` function) but they only render in per-SU views, NOT on the main Incidents & Risk dashboard. Users expect to see and click WC cards from the main Incidents & Risk page.

## What's Needed
Add a **Welfare Concern section** below the incidents table on the Incidents & Risk page (`nav('incidents')` / page id `p-incidents`):

### 1. Section Header
- "WELFARE CONCERNS" heading (same style as "INCIDENTS (10)")
- Show count: "WELFARE CONCERNS (X)"

### 2. Kanban-style layout with columns:
- **Open** — red left border
- **Monitoring** — amber left border  
- **Resolved/Closed** — green left border

### 3. Each card shows:
- SU name (clickable link to SU profile)
- WC ID + concern type
- Date raised
- Assigned staff
- Status badge
- If monitoring: days in monitoring

### 4. Cards are CLICKABLE
- Use the existing `showConcernDetail(wcId)` function (line ~10062) — it already has the full modal with manager actions (edit, observations, review date, monitoring/close)
- Wire up onclick on each card

### 5. Data source
- Use the demo WC data that's already in the code (the arrays with WC-0234, WC-0288, WC-0301 etc. around lines 5035-5403)
- These are the per-SU demo concerns — aggregate them into the main view

### 6. Also add a NEW feature: Guidance Notes (G) button
- Next to "Log Welfare Concern" title AND "Log Incident" title on their respective forms
- A small **G** button/icon (styled like the existing ℹ️ policy link icon)
- On click: toggles open/closed an inline guidance panel below the title
- Panel text: "Quick guidance notes — configurable per organisation" with placeholder guidance text
- This is SEPARATE from the ℹ️ policy link (which links to full policy document)
- G = inline quick reference, ℹ️ = full policy link

## Rules
- Do NOT break existing functionality
- Keep mobile responsive
- Use existing design language (green theme, card-based)
- The `showConcernDetail` function already works — just need to call it from the new kanban cards
- Commit with descriptive message
- Push to GitHub when done

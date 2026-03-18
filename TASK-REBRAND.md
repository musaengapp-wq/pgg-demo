# TASK: Rebrand MVP to Beacon Governance — DO NOT BREAK ANYTHING

## File: index.html (11,600+ lines — be VERY careful)

## ONLY these changes:

### 1. Branding Text
- Replace "Pillar Governance Group" → "Beacon Governance Group" everywhere
- Replace "PGG" → "Beacon Governance" where it's used as company name (NOT in CSS class names or JS variable names — leave code identifiers alone)
- Replace "Pillar OS" → "Beacon" if it appears
- "Beacon" AI QA brand stays as-is (it's already correct)

### 2. Colour Scheme — match the website
Update CSS variables/colours to:
- Primary navy: #1a1a3e
- Primary navy light: #252560  
- Gold accent: #c9a84c
- Gold light: #d4b96a
- Keep all existing layout, spacing, fonts — ONLY change colour values
- If the existing scheme uses different navy/gold hex values, update them to match the above

### 3. Add rounded corners
- border-radius: 12px on cards, stat boxes, modals, forms
- Match the report styling

## CRITICAL RULES:
- DO NOT change any JavaScript functionality
- DO NOT change any layout or spacing
- DO NOT remove any features or sections
- DO NOT rename CSS classes or JS functions (only text content)
- DO NOT change demo data
- Test: if a button worked before, it must work after
- If in doubt, DON'T change it

## When done:
- git add, commit: "Rebrand to Beacon Governance Group + colour match"
- git push
- Run: openclaw system event --text "Done: MVP rebranded to Beacon Governance" --mode now

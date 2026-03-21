# TASK — Batch 1: TL Dashboard Fixes

## File: index.html (single file, all CSS/JS inline)

## Items:

### 1. TL Expenses Form — Match SW Layout
The TL Dashboard has a stripped-down expenses form. It needs to match the SW Dashboard expenses form EXACTLY.

**SW Dashboard expenses has (TL needs ALL of these):**
- Date field
- Category dropdown
- Amount (£) field
- **Upload Receipt button** ← MISSING on TL
- **Description / Notes text area** ← TL only has a small "Details..." field
- **✏️ Dictate + 🔊 Read back toggles** ← MISSING on TL
- **SU Related? (No / Yes radio)** ← MISSING on TL
- **"Submit Expense" button** (TL currently says "Log Expense" — change to "Submit Expense")
- **Approval Workflow visual** ← MISSING on TL

**TL Approval Workflow visual should show:** TL Submits → Pending SM Sign-off → Approved/Denied/Amended
(Different from SW which shows: SW Submits → Pending TL Approval → Pending SM Sign-off → Approved/Denied/Amended)
The TL skips the TL approval step because they ARE the TL.

### 2. TL Mileage Form — Add Accessibility Toggles
The TL Dashboard mileage form is missing the ✏️ Dictate and 🔊 Read back toggles. Add them to match the SW mileage form.

### 3. TL Mileage/Expenses Tab Glitch Fix
There's a bug where clicking the "Mileage" tab on the TL Dashboard sometimes shows the Expenses content, and vice versa. The tab highlight and content are out of sync. Fix the tab switching logic so the selected tab always matches the displayed content.

## IMPORTANT:
- Do NOT change anything on the SW Dashboard — only fix the TL Dashboard
- Do NOT remove any existing elements — only ADD missing ones and fix the tab glitch
- Match the SW Dashboard styling exactly for consistency

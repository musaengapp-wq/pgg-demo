# TASK — URGENT Logo Fix

Work on the file: `/tmp/pgg-demo/index.html`

## Problem
The logo image was accidentally removed in the last batch. It needs to be PUT BACK exactly as it was before.

## What to do
1. Find where the logo/branding area is in the sidebar/header
2. The LOGO IMAGE must be restored — it was there before the last commit and should not have been removed
3. Check the git history: `git diff HEAD~1 HEAD` to see what was changed in the logo area
4. Restore the logo image element exactly as it was
5. Keep the text changes that WERE requested:
   - "Governance Group" text under the logo should stay REMOVED
   - "Compliance Infrastructure" (not "as a Service") should stay
6. ONLY the logo image itself needs restoring — do NOT change anything else

Run: cd /tmp/pgg-demo && git add -A && git commit -m "Restore logo image - was accidentally removed"

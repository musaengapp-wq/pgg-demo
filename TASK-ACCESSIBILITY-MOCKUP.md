# TASK — Accessibility Mockup Buttons

Work on: `/tmp/pgg-demo/index.html`

## What to add

Add two small mockup icon buttons to ALL forms in the system (support notes/contact note form, incident form, welfare concern form, leaver's form, new resident checklist, and any other forms with text input areas):

1. **🎤 Mic button (Speech-to-Text)** — small icon button near text input areas
   - Hover tooltip: "Speech-to-Text: Speak your note and it will be transcribed automatically"
   - On click: show a toast/alert saying "Speech-to-Text — coming soon" (mockup only)
   
2. **🔊 Read-back button (Text-to-Speech)** — small icon button near text input areas
   - Hover tooltip: "Text-to-Speech: Read your note aloud before submitting to check for errors"
   - On click: show a toast/alert saying "Text-to-Speech — coming soon" (mockup only)

Place them next to or below text areas on forms — small, unobtrusive, but visible. Style them to match the existing UI (same colour scheme, border radius etc).

Keep existing look and feel. Don't change anything else.

After completing, run:
cd /tmp/pgg-demo && git add -A && git commit -m "Add accessibility mockup buttons (mic + read-back) on all forms" && git push -f origin main

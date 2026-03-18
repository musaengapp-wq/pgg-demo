# TASK — 2 Fixes

Work on: `/tmp/pgg-demo/index.html`

## Fix 1: Rename "Log Contact Activity" → "Log Support Note"

Find ALL instances of "Log Contact Activity" in the file and rename them to "Log Support Note". This includes:
- Buttons on SU profiles
- Nav items
- Form headings
- Any other references

Do NOT rename "Contact Activity" when it refers to the overview/dashboard — only rename the "Log Contact Activity" action/button/form.

## Fix 2: Add 🎤 🔊 accessibility buttons to the Log Support Note form

The Log Support Note form (previously called Log Contact Activity) is missing the 🎤 Dictate and 🔊 Read back buttons. These buttons should appear below the textarea on this form, same as they do on all other forms.

The accessibility buttons are injected via JavaScript using a MutationObserver that targets textareas — the form may be dynamically generated. Check that the textarea in this form is being picked up. If not, ensure the buttons get added to it.

After completing BOTH fixes, run:
cd /tmp/pgg-demo && git add -A && git commit -m "Rename Log Contact Activity to Log Support Note + add accessibility buttons" && git push -f origin main

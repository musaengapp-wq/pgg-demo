# TASK — Add Beacon Logo Image

Work on: `/tmp/pgg-demo/index.html`
Logo file: `/tmp/pgg-demo/beacon-logo.jpg`

## What to do

1. Convert `beacon-logo.jpg` to base64 and embed it as a data URI inline in the HTML

2. **Sidebar logo**: Find the `<div class="sidebar-logo">` section. Replace the text-based logo (h1 "BEACON" etc) with an `<img>` tag using the base64 data URI. Keep "Compliance Infrastructure" tagline text below it. Max width ~180px.

3. **Login screen**: Find the login box (class "login-box"). Replace the `<h2>BEACON</h2>` (or any existing img tag there) with the same logo image. Max width ~220px with margin-bottom.

4. Make sure the logo displays properly on mobile too (it should scale down).

5. Verify by opening the file in a browser if possible.

After completing:
cd /tmp/pgg-demo && git add -A && git commit -m "Embed Beacon logo image in sidebar and login screen" && git push -f origin main

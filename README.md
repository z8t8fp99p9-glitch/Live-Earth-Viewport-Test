# LIVE // EARTH — Viewport Test v4 (isolated)

This is a diagnostic page only. It is NOT the LIVE // EARTH app and does not access location or user storage.

## What changed
- Keeps `viewport-fit=cover`, iOS standalone mode, and `apple-mobile-web-app-status-bar-style=black-translucent` in the HTML head.
- Runs the same repeated viewport rechecks after rotation/page-show.
- Adds a button: **TRY EXTRA BOTTOM BACKGROUND FILL**. Turn it ON to test whether painting an oversized decorative background can cover the measured `screen.height - window.innerHeight` strip. It does not move the diagnostic panel or the five illustrative orbs.

## Apply this only to the separate test repository
Repository: `z8t8fp99p9-glitch/Live-Earth-Viewport-Test`
Replace only `index.html` with `LIVE-EARTH-Viewport-Test-index-v4.html`. Leave the live `z8t8fp99p9-glitch/Live-Earth` repository untouched.

After the test repository publishes, remove only the old **test icon** from the Home Screen and add the test page again using Safari → Share → Add to Home Screen. The status-bar meta configuration can be captured at installation, so a newly installed test icon is needed for a fair comparison. Do NOT delete any LIVE // EARTH icons or clear browser/site data.

## Test
1. Open the new test icon.
2. Record the diagnostic readings with the toggle OFF.
3. Tap **TRY EXTRA BOTTOM BACKGROUND FILL: OFF** to turn it ON.
4. Look at the black bottom strip; screenshot both the readings and the page.
5. Rotate once and return to portrait, then see whether the result holds.

If the strip remains black with the background overdraw ON, this is evidence the strip is outside the page's drawable viewport; do not copy the experiment into the production app.

Suggested commit title for the separate test repository only:
`Test iOS bottom background overdraw`

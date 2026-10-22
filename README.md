# LIVE // EARTH — Isolated iOS Viewport Test

**Purpose:** Test one variable only: the test page intentionally omits
`apple-mobile-web-app-status-bar-style=black-translucent`. It keeps
`viewport-fit=cover`, the iOS standalone-capable meta tag, a standalone web app
manifest, a full-bleed background and a five-item illustrative bottom row.

**This is NOT the LIVE // EARTH application.** It contains no app controllers,
service worker, geolocation calls, database, or local recovery logic. It does
not modify or replace the app's v75 files. Its on-screen orb row is illustrative.

## Safe test procedure

1. Create a separate free GitHub repository named `Live-Earth-Viewport-Test`.
2. Upload the files in this ZIP to the root of that NEW repository. Do not upload
   anything to `z8t8fp99p9-glitch/Live-Earth` and do not replace any v75 files.
3. In the new repository, open **Settings → Pages** and enable Pages from the
   `main` branch and `/ (root)` folder. If GitHub uses a different branch name,
   select the branch containing these files.
4. Open the published Pages URL in Safari on the same iPhone. Confirm the page
   says **ISOLATED VIEWPORT TEST** and the measurements are visible.
5. In Safari's Share menu, choose **Add to Home Screen**. Launch the new
   `LE View Test` icon directly from the Home Screen (not from a browser tab).
6. Compare the top and bottom colored artwork against the two existing app
   shortcuts. Save a screenshot of the test and note the displayed measurements.

## What this experiment can tell us

- If this isolated standalone page also has a black bottom band, that supports an
  iOS/WebKit standalone viewport or status-bar presentation issue beyond our app's
  scene/controllers.
- If this page fills the available screen but the app does not, the difference
  is more likely in the app's own document/CSS composition or launch setup.
- Removing the translucent-status-bar setting may make the status bar opaque;
  this is a diagnostic trade-off, not a promised production fix.

## Guardrails

- `z8t8fp99p9-glitch/Live-Earth` `main` remains unchanged.
- Do not delete shortcuts, clear website data, reset storage, or change v75.
- This test does not access Location or store user data.
- Do not copy any test files into the live app repository until the result has
  been reviewed and the user explicitly approves a next step.

Suggested commit title for the NEW test repository only:
`Add isolated iOS viewport diagnostic`

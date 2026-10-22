# LIVE // EARTH — Full-Screen Viewport Test v3

This isolated test is for the separate `Live-Earth-Viewport-Test` repository only. It does not include the LIVE // EARTH app, app controllers, service worker, geolocation, or local database.

## What changed in v3
- Restores `apple-mobile-web-app-status-bar-style=black-translucent`, matching the LIVE // EARTH standalone-app install configuration.
- Adds full-page/root background painting using the same scene palette, so iOS-owned viewport gaps can be assessed for visual blending.
- Includes the previously planned viewport recovery measurements after `orientationchange` and `pageshow` (immediate, 180, 420, 800 ms).
- Prints screen height, layout viewport height, their difference, visual viewport offset, safe-area values, stage dimensions, standalone mode, and recovery trigger.
- Does not apply an arbitrary 68px shift to artwork. The measurements must guide any correction.

## Critical test instruction
The status-bar meta needs to be present when a Home Screen icon is added. After replacing `index.html` on the TEST repository and waiting for GitHub Pages to publish it, open the Pages URL in Safari and add a **new separate test icon**. Keep existing LIVE // EARTH shortcuts and the earlier test icon; do not delete them. Launch the new test icon directly and capture the diagnostic after waiting and after one portrait → landscape → portrait cycle.

Do not upload this file to `z8t8fp99p9-glitch/Live-Earth`. Do not change its `main`, clear storage, or reset local data.

This test can confirm the geometry and whether root background painting visually blends reserved areas. It cannot make DOM/canvas pixels accessible inside a viewport strip withheld by iOS/WebKit. See WebKit reports 313800 and 316008 for this platform limitation and install-time metadata behavior.

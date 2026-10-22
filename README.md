# LIVE // EARTH — Isolated iOS Viewport Test v5

This is a test-only HTML page. It does not include the LIVE // EARTH app, a service worker, geolocation calls, database logic, or local recovery code.

## Update the existing test repository
Replace **only `index.html`** in `z8t8fp99p9-glitch/Live-Earth-Viewport-Test` with this file. Leave `README.md`, `manifest.webmanifest`, `icon.png`, and `icon.svg` unchanged. Do not upload anything to `z8t8fp99p9-glitch/Live-Earth`.

## Test
1. Commit the replacement in the separate test repo and wait for GitHub Pages to update.
2. Delete only the isolated viewport-test Home Screen icon, then install it again from Safari using Share → Add to Home Screen. Do not delete any LIVE // EARTH shortcut.
3. In portrait, screenshot measurements with both controls OFF.
4. Tap **STAGE HEIGHT: 100%** to switch to `100dvh`, wait a second, and screenshot.
5. Tap **ROOT PAINT PROBE: NEON ON**. This temporarily colors the HTML/body background bright magenta. Observe whether the bottom black strip changes color. Tap again to restore normal color.
6. Rotate to landscape and back to portrait. Wait one second and take a final screenshot.

## Interpretation
- If the 100dvh control changes the measured stage height or fills more screen, that approach may help within the page viewport.
- If the neon root-paint probe does not color the bottom strip, that is evidence the strip is outside the part of the screen the webpage can paint. A PWA cannot place interactive content into a region withheld by iOS/WebKit.
- If the strip changes to magenta, the system is painting some page background there, and we can evaluate whether a matching color can cosmetically blend it. This is diagnostic only, not a production design.

## Guardrails
Keep the live `Live-Earth` repository and v75 build untouched. Do not clear site data, reset storage, or delete real app shortcuts. User manually uploads and commits; no commits or deployments are made by the assistant.

Suggested commit title for the separate test repo only: `Compare iOS viewport height and root painting`

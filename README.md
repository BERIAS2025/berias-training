# BERIAS Training

Browser and Android installation: https://berias2025.github.io/berias-training/

This is the standalone training app repository. Meal prep stays in its separate repository at https://github.com/BERIAS2025/meal-prep-app and at https://berias2025.github.io/meal-prep-app/.

German hybrid training with three evening Mobility sessions, editable and archivable custom exercises, local session history, conservative interval progression and complete JSON backup/restore. Fresh installations use the updated hybrid plan.

## Android
Open the training address in Chrome. Verify Version 2.2. Use Installieren or the Chrome menu > Add to Home screen > Install. Wait for Offline bereit. Physical Android installation and correction of an existing home-screen icon require verification on the device.

## Saved records
Export a full backup before changing installations. Do not clear browser/site data. Storage is local to the browser profile and origin; these two GitHub Pages repositories share an origin, but training and meal prep use separate storage keys. Training history from the old GitHub training path may already be visible here. Records from the older chatgpt.site address require full backup/restore. Each device remains separate. Check the restored history before removing old shortcuts.

## App isolation
The training manifest has explicit ID, start URL and scope /berias-training/. The meal planner keeps its legacy app ID / to preserve the installed meal app identity. The training service worker has its own scope and cache prefix. Never revert these IDs to the same relative ./ value: manifest IDs resolve against the origin.

## Development and publishing
App sources are in dist/ with no build dependencies. Run npm test (Node 22+) and npm start for a local preview. GitHub Actions runs tests and publishes dist/ from main to GitHub Pages. Workflow permissions and the github-pages environment apply only to this repository. No personal training logs are included.

Initial GitHub setup: Repository Settings > Pages > Source > GitHub Actions. The workflow publishes an already-enabled Pages site and does not attempt to change repository administration settings.

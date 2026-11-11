# Okinawa Family Trip Website

沖繩家族之旅｜2026/11/15–11/19 五天四夜自駕行程網站。

## Publish the website

This repository uses the GitHub Actions workflow at `.github/workflows/deploy-pages.yml`.

The workflow supports two source layouts:

- **Repository-root files (preferred):** `index.html`, `control-panel.html`, `trip-data.json`, and the `assets/` folder.
- **ZIP-only upload:** `site-bundle.zip` in the repository root. The workflow extracts the archive and publishes the website files from it.

When both are available, the workflow uses the complete repository-root files first. This prevents an older ZIP archive from overwriting newer edits.

### First-time setup

1. Open [Settings → Pages](https://github.com/simonBOSS1019/okinawa-family-trip/settings/pages).
2. Set the build and deployment source to **GitHub Actions**.
3. Open [Actions](https://github.com/simonBOSS1019/okinawa-family-trip/actions) and confirm that **Deploy Okinawa Trip Website** completes successfully. You can also start it manually with **Run workflow**.
4. After a successful run, use the public URL shown in the deployment job.

### Updating the website

- Changes to the root HTML/data files, anything under `assets/`, the ZIP archive, or this workflow trigger a deployment when committed to `main`.
- To publish from a ZIP on a phone, upload it to the repository root with the exact name `site-bundle.zip`, then commit it to `main`.
- The ZIP must contain `index.html`, `control-panel.html`, `trip-data.json`, and `assets/cover.png` together in one website folder. That folder may be at the archive root or inside one enclosing directory.

## Current deployment checklist

- The repository-root website files are present.
- The workflow supports both repository-root files and a ZIP-only upload.
- The live deployment is confirmed only after the latest **Deploy Okinawa Trip Website** run succeeds.

Repository: https://github.com/simonBOSS1019/okinawa-family-trip

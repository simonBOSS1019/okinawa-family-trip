# Okinawa Family Trip Website

沖繩家族之旅｜2026/11/15–11/19 五天四夜自駕行程網站。

## Publish the website (one-time setup)

This repository now includes a GitHub Actions workflow at `.github/workflows/deploy-pages.yml`. The complete site bundle contains the HTML, itinerary data, CSS/JavaScript, and all illustrations.

1. Download the complete ZIP supplied in the ChatGPT conversation.
2. On GitHub, choose **Add file → Upload files** and upload the ZIP to the repository root, naming it exactly **`site-bundle.zip`**. Upload the ZIP as a single file; do not extract it on the phone.
3. Commit the upload to the `main` branch.
4. If Pages is not enabled yet, open [Settings → Pages](https://github.com/simonBOSS1019/okinawa-family-trip/settings/pages) and select **GitHub Actions** as the build/deployment source.
5. Follow [Actions](https://github.com/simonBOSS1019/okinawa-family-trip/actions) and confirm **Deploy Okinawa Trip Website** succeeds. The final public URL will be shown in the deployment job.

The workflow extracts `site-bundle.zip`, verifies that `index.html` and the `assets` folder are present, and publishes the contents using GitHub Pages.

## Current status

- The deployment workflow has been added to this repository.
- The website bundle has not yet been uploaded to this repository.
- GitHub Pages has not been verified as deployed; do not treat the site as live until the Actions job succeeds.

Repository: https://github.com/simonBOSS1019/okinawa-family-trip

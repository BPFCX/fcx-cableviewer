# FibreconX Cable Fibre & Circuit Viewer — V11

Static GitHub Pages package. `index.html` is the existing V11 application, unchanged.

## Publish on GitHub Pages

1. Create a **private repository** if your organisation permits GitHub hosting. Review internal information-security requirements before making a public site. GitHub Pages sites may be publicly reachable even when repository visibility is restricted, depending on plan and configuration.
2. Upload `index.html`, `.nojekyll`, and this `README.md` to the repository root.
3. In repository **Settings → Pages**, select **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
4. The site address is generally `https://<username>.github.io/<repository>/`.
5. In `index.html`, replace `YOUR_PORTAL_APP_ID` in `CONFIG.appId` with your registered ArcGIS Portal OAuth application ID. Configure the matching GitHub Pages redirect URL in Portal's registered app settings. Do not publish passwords or ArcGIS tokens in GitHub.
6. Open the published page and sign in, or use the temporary-token option for testing.

## Notes

- Portal: `https://arcgis.fibreconx.com.au/portal` (configured in application).
- Data: 3-GIS Telecom MapServer layers 7 (FiberCable), 27 (Fiber), 30 (Signal); cable-to-fibre relationship 117.
- This application uses browser-side requests; ArcGIS Server must allow the deployed origin under its CORS and authentication policies. GitHub Pages hosting does not override SharePoint CSP or network access restrictions.
- This package contains the existing V11 application and has not been live-tested against the private FibreconX service.
- `.nojekyll` tells GitHub Pages to serve static files without Jekyll processing.

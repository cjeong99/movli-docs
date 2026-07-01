# Publishing these pages on GitHub Pages

This folder contains the three static pages Kickwise needs for App Store
submission: a support page, a Privacy Policy, and Terms of Use.

## Before publishing — fill in these placeholders

Every file in this folder has bracketed placeholders. Find-and-replace
across `privacy-policy.html` and `terms-of-use.html`:

| Placeholder | What it needs |
|---|---|
| `[EFFECTIVE DATE]` | The date you publish these, e.g. "July 1, 2026" |
| `[DEVELOPER NAME]` | Your name or business/LLC name, as it should appear legally |
| `[CONTACT EMAIL]` | A real, monitored email address (the app currently uses `feedback@kickwise.app` in `AppLinks.swift` — use that if it's real, or pick a different one and update both places) |
| `[STATE/COUNTRY]` | The jurisdiction for the "Governing law" clause in Terms of Use, e.g. "the State of California, USA" |

## Enabling GitHub Pages

1. Push this repo to GitHub (if it isn't already).
2. In the repo on GitHub: **Settings → Pages**.
3. Under "Build and deployment", set **Source: Deploy from a branch**.
4. Branch: `main` (or whichever branch you push to), folder: **`/docs`**.
5. Save. GitHub will publish at
   `https://<your-username>.github.io/<repo-name>/` within a minute or two.

Your three pages will be at:
- `https://<your-username>.github.io/<repo-name>/index.html` (support)
- `https://<your-username>.github.io/<repo-name>/privacy-policy.html`
- `https://<your-username>.github.io/<repo-name>/terms-of-use.html`

## After you have the real URL

Update these to point at it instead of the `kickwise.app` placeholder:
1. `kickwise/Utilities/AppLinks.swift` — `privacyPolicy` and `termsOfUse`
2. `AppStoreAssets/Metadata.md` — Support URL / Privacy Policy URL sections
3. App Store Connect's own "Support URL" and "Privacy Policy URL" fields
   when you set up the app record

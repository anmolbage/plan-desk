# SBI Life Plan Desk

A phone-friendly working tool: customer pitch, key terms and brochure links for 26 SBI Life individual plans, with return calculators for the six unit-linked plans. It is an independent aid, not an SBI Life product or an official benefit illustration.

## Files

| File | What it is |
|---|---|
| `index.html` | The whole app: page, plan data, calculators |
| `manifest.webmanifest` | Lets phones install it as an app |
| `sw.js` | Makes it open without a connection |
| `icon-192.png`, `icon-512.png`, `icon-maskable-512.png`, `apple-touch-icon.png` | App icons |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

All of them must sit together in the same folder.

## Put it on GitHub Pages

1. Create a new repository on GitHub, for example `plan-desk`.
2. Upload every file in this folder to the top level of the repository (Add file → Upload files). Include `.nojekyll`.
3. Open Settings → Pages. Under "Build and deployment" choose "Deploy from a branch", branch `main`, folder `/ (root)`, and save.
4. After a minute or two the app is live at `https://<your-username>.github.io/plan-desk/`.

## Install it on a phone

- Android (Chrome): open the address, then menu → "Add to Home screen" or "Install app".
- iPhone (Safari): open the address, then Share → "Add to Home Screen".

Once opened one time with a connection, it works offline. Links to SBI Life brochures still need a connection.

A plan can be opened directly by adding its code to the address, for example `.../plan-desk/#retire` or `.../plan-desk/#platplus`.

## Updating

Replace `index.html` with the new version. Phones pick it up the next time they open the app online. If you also change icons or the manifest, raise the `VERSION` line at the top of `sw.js` (for example to `plan-desk-v2`).

## Things to know

- A GitHub Pages site is public: anyone who has the address can open it. The page asks search engines not to index it, but that is a request, not a lock.
- Plan terms were read from SBI Life brochures on 8 and 9 October 2026, and fund returns are a snapshot from the same dates. Neither refreshes on its own.
- Fonts load from Google Fonts when online and are kept for offline use after the first visit; before that the app falls back to the phone's own fonts.

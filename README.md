# Clueframe Landing

Static website for **Clueframe: Picture Riddles** (Android) by Clueframe Games.

## Structure

- `public/index.html` — landing page
- `public/privacy/index.html` — privacy policy (served at `<site>/privacy/`)
- `.github/workflows/static.yml` — deploys `public/` to GitHub Pages on every push to `main`

## Before publishing — required

- [ ] **Contact email** — replace the highlighted `[CONTACT EMAIL — SET BEFORE PUBLISHING]` placeholder in `public/privacy/index.html`. A privacy policy without a working contact is a Play review problem.
- [ ] **Hosting / final URL** — decide where this is served. Note: `clueframe.com` is registered to an unrelated company and must not be used. GitHub Pages for this repo would serve at `https://clueframe.github.io/Clueframe_Landing/`, making the policy URL `https://clueframe.github.io/Clueframe_Landing/privacy/`. All internal links are relative, so any host works.
- [ ] **Update the app** — set `policy_link` in the Android app's `strings.xml` and the Play Console listing to the final policy URL.
- [ ] **Ad network list** — re-verify the network list in the policy against the final CAS mediation configuration (`cas_settings*.json`) before release, and again whenever networks are added or removed.
- [ ] **app-ads.txt** — once ad networks are connected in the CAS mediation dashboard, publish the `app-ads.txt` it generates at the site root (`public/app-ads.txt`), and set this site's URL as the developer website in the Play listing so networks can verify it.
- [ ] **Store link** — add the Google Play link to `public/index.html` once the listing is live.
- [ ] If in-app purchases are ever enabled, extend the policy accordingly (it currently describes an ads-only app with no accounts).

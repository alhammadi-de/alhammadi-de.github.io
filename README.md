# Peel's public site — alhammadi-de.github.io

Three pages and one file that App Store Connect and AdMob need. Plain HTML, one stylesheet, no
scripts, no cookies, no trackers. Not published yet: read the text first.

| Page | URL once published | Goes in |
|---|---|---|
| `index.html` | https://alhammadi-de.github.io/ | App Store Connect → version → **Marketing URL** (AdMob reads app-ads.txt from this domain) |
| `peel/index.html` | https://alhammadi-de.github.io/peel/ | App Store Connect → version → **Support URL** |
| `peel/privacy/index.html` | https://alhammadi-de.github.io/peel/privacy/ | App Store Connect → App Privacy → **Privacy Policy URL**, and the AdMob consent message |
| `app-ads.txt` | https://alhammadi-de.github.io/app-ads.txt | Checked by AdMob (must sit at the domain root) |

## Filled in (6 Oct)

- Support and privacy email: **ipa.tech23@gmail.com**; developer: **Mohamed Alhammadi**.
- `app-ads.txt`: AdMob publisher **pub-3362624298374447**.
- The privacy page matches his answers of 6 Oct: 13+ with ads rated T, the Home banner and the
  interstitial (after a save or share, before Snapchat, at most once every 3 minutes), Report ad in
  Settings. Mohamed reads the privacy text before anything is published (his ruling (d)).

## Publish

Tell Claude "publish the site". Claude then, with the Mac's `gh` (signed in as alhammadi-de):

1. creates the **public** repository `alhammadi-de/alhammadi-de.github.io`
   (the name must be exactly this for a user site; on GitHub Free a Pages repository must be public),
2. pushes this folder to `main`,
3. checks Settings → Pages: Source = Deploy from a branch, `main`, `/ (root)`,
4. waits for the site (up to 10 minutes) and opens all four URLs.

Or by hand: github.com → New repository → name `alhammadi-de.github.io`, Public → push this folder →
Settings → Pages → Deploy from a branch → `main` / root → Save.

The app's code repository (`alhammadi-de/peel`) stays private. This site holds no code.

## Keep in step with the app

- If the app's data practices change (a new SDK, a new ad format, analytics), update the privacy
  page and its date first, then App Store Connect → App Privacy.
- AdMob re-reads `app-ads.txt` on its own; it can take 24 hours after a change.
- `.nojekyll` makes GitHub Pages serve the files exactly as they are.

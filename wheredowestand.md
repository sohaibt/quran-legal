# Where do we stand — qurantutors.app website (quran-legal)

Public GitHub Pages repo for https://qurantutors.app (custom domain via `CNAME`). The app itself lives in the `quran` repo.

## RESUME HERE
**2026-10-26 (MacBook Air):** Landing page **live** at https://qurantutors.app/ (Arabic) and /en/ (English), in "coming soon" mode: PR #1 merged on the owner's OK (merge commit f2ec58e), GitHub Pages build checked, all pages and privacy/terms return 200. Owner chose to go live before App Review approval.
- `index.html` = Arabic (primary, RTL), `en/index.html` = English. One responsive page each (phone + desktop from one HTML; breakpoint 1000px). Styles in `landing.css`; `style.css` stays for `privacy.html` / `terms.html` (both untouched; App Store links to `/privacy.html`).
- Real app screenshots in `assets/` (WebP, 640px wide, 24–48 KB each), from `quran/docs/store-screenshots/{ar,en}`. Step 1 (add learners) uses a small HTML "learners" card, not a screenshot (no matching screen; `4-chat` is copied but unused).
- Apple's official badges: `assets/app-store-badge-en.svg` and `-ar.svg` (Arabic one = `.../black/ar-ar`; `ar-sa` returns English).
- "Coming soon" vs "live" mode: one line per page, `APP_STORE_URL` in the `<script>` in the `<head>` of `index.html` and `en/index.html`. Empty = coming soon (chip "Coming soon on iPhone", "App Store · Coming soon" text, no "Apply in the app" button). Filled = live (adds class `live` to `<html>`: official badges + "Apply in the app" appear and link to the URL, chip says "Now on iPhone"). Elements carry `when-soon` / `when-live`; rules at the end of `landing.css`. Both modes tested in a browser. Likely URL: `https://apps.apple.com/app/id6824174298` (ascAppId in the quran repo's eas.json); confirm in App Store Connect.
- Design source: Claude Design canvas https://claude.ai/artifact/UeJU5Y1dH8rXvtAHsjjyEZ page "Landing page" (boards LP-AR/EN-Desktop/Mobile).

Next-session startup prompt:
```
quran-legal repo (sibling of the quran repo). git fetch and compare to origin/main and origin/landing-page; pull --ff-only if behind. Read wheredowestand.md RESUME HERE.
Check App Review status for Quran Tutors (see the quran repo's RESUME HERE). After Apple approves AND the app is released: paste the App Store URL into the APP_STORE_URL line in index.html and en/index.html (on main), check both pages, then ask me before pushing to main.
Ask me before anything outward-facing (merge, push to main, DNS).
```

## Session log
- 2026-10-18 — Privacy policy and terms (ar + en) published; domain qurantutors.app via CNAME.
- 2026-10-26 — Landing page (ar + en) built on `landing-page`, PR opened, not merged. Checked locally at 390px and 1440px; privacy/terms unchanged.
- 2026-10-26 — Owner chose to go live before App Review: added "coming soon" mode (one-line switch to live). PR #1 merged; site live.

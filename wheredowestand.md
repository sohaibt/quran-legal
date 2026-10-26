# Where do we stand — qurantutors.app website (quran-legal)

Public GitHub Pages repo for https://qurantutors.app (custom domain via `CNAME`). The app itself lives in the `quran` repo.

## RESUME HERE
**2026-10-26 (MacBook Air):** Landing page built on branch `landing-page`, PR open, **not merged** (merging = going live). Go live only after Apple approves the app.
- `index.html` = Arabic (primary, RTL), `en/index.html` = English. One responsive page each (phone + desktop from one HTML; breakpoint 1000px). Styles in `landing.css`; `style.css` stays for `privacy.html` / `terms.html` (both untouched; App Store links to `/privacy.html`).
- Real app screenshots in `assets/` (WebP, 640px wide, 24–48 KB each), from `quran/docs/store-screenshots/{ar,en}`. Step 1 (add learners) uses a small HTML "learners" card, not a screenshot (no matching screen; `4-chat` is copied but unused).
- Apple's official badges: `assets/app-store-badge-en.svg` and `-ar.svg` (Arabic one = `.../black/ar-ar`; `ar-sa` returns English).
- App Store link: one place per page, the `APP_STORE_URL` line in the `<script>` at the bottom of `index.html` and `en/index.html`. It fills every button marked `data-app-store`. Empty now (buttons point to `#`).
- Design source: Claude Design canvas https://claude.ai/artifact/UeJU5Y1dH8rXvtAHsjjyEZ page "Landing page" (boards LP-AR/EN-Desktop/Mobile).

Next-session startup prompt:
```
quran-legal repo (sibling of the quran repo). git fetch and compare to origin/main and origin/landing-page; pull --ff-only if behind. Read wheredowestand.md RESUME HERE.
Check App Review status for Quran Tutors (see the quran repo's RESUME HERE). Only after Apple approves:
1. On branch landing-page, paste the App Store URL into the APP_STORE_URL line in index.html and en/index.html. Commit, push.
2. Ask me before merging the landing-page PR (merging = the site goes live).
3. After merge, open https://qurantutors.app/ and /en/ on a phone and check /privacy.html and /terms.html still work.
Ask me before anything outward-facing (merge, push to main, DNS).
```

## Session log
- 2026-10-18 — Privacy policy and terms (ar + en) published; domain qurantutors.app via CNAME.
- 2026-10-26 — Landing page (ar + en) built on `landing-page`, PR opened, not merged. Checked locally at 390px and 1440px; privacy/terms unchanged.

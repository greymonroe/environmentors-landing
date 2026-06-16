# EnvironMentors @ UC Davis — program website

Static site for the UC Davis EnvironMentors program, hosted on **GitHub Pages**.
This is the site intended to become the program's public home at `environmentors.ucdavis.edu`
(replacing the old SiteFarm site).

- **Owner:** `EnvironMentors-UC-Davis` org (transferred from `greymonroe/` on 2026-06-16)
- **Live URL (now):** https://environmentors-uc-davis.github.io/environmentors-landing/
- **Live URL (goal):** https://environmentors.ucdavis.edu/ — pending UC Davis IET DNS (CNAME → `environmentors-uc-davis.github.io`)
- **Pages source:** `master` branch, root
- **Interest form:** a Google Form is embedded in `index.html` (responses → Google Sheet); the form is owned/edited from the `grey-matter` project

> ⚠ The old `greymonroe.github.io/environmentors-landing/` URL **404s** after the org transfer
> (GitHub doesn't redirect Pages across owners). The recruitment QR routes through **bit.ly**, so
> repoint that short link to the new URL — until then the printed QR is dead.

> **Operational status, the DNS cutover plan, and the activity log live in the program repo:**
> `~/Dropbox/myapps/environmentors-program/website/README.md`. Update it when you change the site.

## Structure (current — editorial redesign)

- `index.html` — home / get-involved, with the embedded interest form
- `faq.html` — audience FAQ
- `support.html` — giving + broader-impacts case for PIs
- `blog.html` — updates / highlights
- `site.css` — shared stylesheet
- `STYLE.md` — design/voice notes
- `photos/` — program photography
- `_archive/` — superseded work: the old **audience-picker** architecture
  (`audiences/*.html`, `build_audiences.py`, `styles.css`) and early design `_concepts/`.
  Kept for reference; not part of the live site.

## Custom-domain cutover (do in order)

1. **[blocked on IET]** UC Davis IET creates the `environmentors.ucdavis.edu` → `environmentors-uc-davis.github.io` CNAME.
2. **Only after DNS resolves:** Settings → Pages → Custom domain = `environmentors.ucdavis.edu` (writes a `CNAME` file). Do **not** commit a `CNAME` file before DNS is live — it breaks serving.
3. Wait for the auto HTTPS cert (~24 h), then enable "Enforce HTTPS".
4. Retire the SiteFarm version.

## Editing

Plain static HTML/CSS — edit the `.html` files and `site.css` directly, commit, push to `master`; Pages redeploys automatically. Keep content **public-safe and generic** (no rosters, contact info, completed forms, or minors' names/faces without consent — those stay in access-controlled Google Drive and are only linked).

# photo-site

A simple public photo site for sharing with friends and family, hosted free on
GitHub Pages at https://dallhoff.github.io/photo-site/

## About the owner

- An IT professional who hasn't done hands-on development in years.
- Often works from an iPhone, so give phone-friendly steps (Safari, not the
  GitHub app, for settings pages).
- Explain technical topics simply. For key decisions, explain the options and
  trade-offs and ask before choosing.

## Goal

Right now the site is a test gallery of food photos. The plan is to turn it
into a site friends and family actually use: more photos, organized sections,
and some written info (stories, updates, captions).

## How the site works

- `index.html` is the whole site: HTML, CSS and JavaScript in one file. No
  build step and no frameworks.
- The `photos` list near the bottom of `index.html` controls which photos
  appear and in what order. Each entry is a file name plus a short
  description (used as alt text for screen readers, not shown on the page).
- `photos/full/`: large copies, about 1600 px on the long side, JPEG quality 82.
- `photos/thumb/`: grid thumbnails, about 600 px, same file names, quality 78.
- File names are `NN-short-description.jpg`; the number sets the order.
- `.nojekyll` makes GitHub Pages serve the files as they are.
- Publishing is automatic: GitHub Pages redeploys whenever `main` changes
  (Settings → Pages → Deploy from a branch → `main`, `/ (root)`).

## Rules

- **Privacy first. The repo and site are public.** Before adding any photo,
  strip all metadata (GPS location, date, device), fix its rotation, resize
  it, and save it as JPEG. Never commit original photos, because Git history
  keeps them even after they're deleted.
- Before publishing anything personal (names, faces of kids, addresses,
  schedules), point out that it will be public and confirm with the owner.
- New photos usually arrive as chat attachments. Process them with Python
  Pillow (`ImageOps.exif_transpose`, `thumbnail`, save without EXIF).
- Work on a `claude/...` branch, open a pull request, then merge it into
  `main` once the owner agrees. Don't push straight to `main`.
- Test changes in a phone-sized browser (Playwright with
  `/opt/pw-browsers/chromium` in cloud sessions) before pushing.

## Resume here

When the owner says "resume", "pick up where we left off" or similar, read
this section, summarize where things stand, and suggest the next step.
Update this section at the end of each working session: keep it short and
current, and remove items once they're done.

**Status (2026-10-23):**
- Site is live with 11 test food photos, titled "From My Kitchen".
- Grid with a tap-to-open full-screen viewer (swipe, arrow keys, dark mode).

**Next steps / ideas:**
- Decide the real purpose and title of the site for friends and family.
- Choose how to organize it (sections or albums, captions, text pages).
- Replace or keep the test food photos.
- Decide whether anything should be less public (GitHub Pages sites are
  always public on the free plan).

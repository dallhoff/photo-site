# photo-site

Simple web site built with Claude Code to share photos.

## What's here

- `index.html`: the whole site. It shows a grid of photos; tap one to see it
  full screen, then swipe or use the arrow keys to move between them.
- `photos/full/`: the large versions (about 1600 px tall).
- `photos/thumb/`: small versions for the grid, so the page loads fast.
- `.nojekyll`: tells GitHub Pages to serve the files as they are.

All photos have had their metadata (location, date, device) removed.

## Adding a photo

1. Put a large copy in `photos/full/` and a small copy with the same name in `photos/thumb/`.
2. Add a line for it to the `photos` list near the bottom of `index.html`.

## Publishing

The site is served by GitHub Pages from the `main` branch
(Settings → Pages → Deploy from a branch → `main`, folder `/ (root)`).

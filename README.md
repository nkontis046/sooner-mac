# Sooner: the site

Two static pages, no build step, no scripts:

- `index.html`: the landing page (the App Store's Marketing URL)
- `privacy.html`: support, privacy policy, terms of use and copyright on one page. It's both the
  App Store's Support URL (`privacy.html#support`) and its Privacy Policy URL
  (`privacy.html#privacy`).

`css/site.css` styles both, in light and dark.

## Publish

Any static host works. Point it at this folder:

- **GitHub Pages**: Settings → Pages → deploy from branch, folder `/site`.
- **Cloudflare Pages / Netlify**: build command none, output directory `site`.

The drive this repo lives on writes `._*` AppleDouble files next to everything. Git ignores
them, but a drag-and-drop upload won't: deploy from git, or delete them first
(`find site -name '._*' -delete`).

## Where it lives

Published at https://nkontis046.github.io/sooner-mac/ from the GitHub repo
`nkontis046/sooner-mac` (Pages, main branch, root). The App Store link points at app ID
6836703564. Apple prefers its official "Download on the Mac App Store" badge from the App Store
marketing tools; the button uses the same words, so you can swap the badge in.

## Where the pictures come from

Every picture is the real app on its built-in fake sample statements:

- `assets/screens/*.png`: window captures from `tools/make_store_screenshots.sh` (it keeps the
  raw captures in `~/Library/Caches/Sooner/store-raw`), resized to 1600 wide.
- `assets/share.png`: the first App Store screenshot, resized.
- The icons are the real app icon, rendered by Icon Composer's command-line tool from
  `App/Sooner/AppIcon.icon`.

# Site photos

These are the **web-optimized images the site loads**. Gallery photos are real `<img>` tags in
`index.html`; heroes, sub-heroes and location cards are still `url('images/<slot>.jpg')`
backgrounds in `styles.css`. Each file is a resized/compressed copy (long edge ~2000 px,
~280–620 KB) of a full-resolution original kept in the repo-root **`/images`** archive.

Every image area also has a refined gradient fallback in `styles.css`, so the site still looks
intentional if a file is missing.

## What's here now
**Lost Trail** (from the `CAMPFIRE-RANCH-LOST-TRAIL-LODGE-*` originals):

| Filename | Where it shows | Source original |
|---|---|---|
| `hero.jpg` | Homepage full-screen hero | `…LODGE-13` (lodge in the pines) |
| `lost-trail.jpg` | Home location card **+** Lost Trail page hero | `…LODGE-9` (sunlit lodge) |
| `lt-1.jpg` | Galleries + Instagram strip | `…LODGE-19` (great room) |
| `lt-2.jpg` | Galleries + Instagram strip | `…LODGE-33` (bedroom) |
| `lt-3.jpg` | Galleries + Instagram strip | `…LODGE-21` (deck + canyon) |
| `lt-4.jpg` | Galleries + Instagram strip | `…LODGE-30` (kitchen + dining table) |
| `lt-5.jpg` | Galleries + Instagram strip | `…LODGE-3` (Coldstream creek) |
| `lt-6.jpg` | Galleries + Instagram strip | `…LODGE-1` (arched windows + golden aspen) |

**Thelma** (from the high-res `Thelma Hut *` / `Thelma Winter *` / `IMG_*` originals):

| Filename | Where it shows | Source original |
|---|---|---|
| `thelma.jpg` | Home location card **+** Thelma page hero | `Thelma Hut 13` (dusk, hut + peak) |
| `rmp-1.jpg` | Thelma gallery | `Thelma Hut 20` (kitchen / dining) |
| `rmp-2.jpg` | Thelma gallery | `Thelma Hut 16` (deck + the view) |
| `rmp-3.jpg` | Thelma gallery | `Thelma Hut 28` (bedroom) |
| `rmp-4.jpg` | Thelma gallery | `Thelma Hut 27` (bunk room) |
| `rmp-5.jpg` | Thelma gallery | `Thelma Winter 01` (snow, dusk) |
| `rmp-6.jpg` | Thelma gallery | `IMG_7537` (ski touring) |

## To swap a photo
Replace the web copy here, keeping the same filename (JPG, ~2000 px long edge, under ~500 KB).
Nothing else to change.

## To add a photo
The Lost Trail gallery is markup-driven — no CSS rule per photo any more. Two steps:

1. Drop the web-sized JPG in this folder (`lt-7.jpg`, `lt-8.jpg`, …).
2. Copy one `<button class="gallery__tile">` block in the gallery section of `index.html`,
   point `src` at the new file, and write the `alt` (a real description, for SEO and screen
   readers) and the `<span class="gallery__cap">` (2–4 words, shown on hover).

Order in the HTML is the order on the page. The lightbox, the photo counter and the
"View all N photos" button pick up new tiles automatically. Past `GALLERY_PREVIEW` photos
(set in `app.js`, currently 6) the grid collapses behind that button; with JS off, every
photo shows.

The old `.img-lt-1` … `.img-lt-6` background rules in `styles.css` are no longer used by the
gallery. They're left in place because `styles.css` is shared with the sibling sites — don't
delete them here without regenerating all three.

**Heads up:** `styles.css` and `app.js` are shared/generated files. The gallery rebuild
(2026-09) was made directly in this repo, so fold it into the `huts` master source before the
next regeneration or it will be overwritten.

## Rights
The Lost Trail set was originally shot for Campfire Ranch — confirm SIG has the right to publish
before the site goes live.

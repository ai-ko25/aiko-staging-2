# Lumisphere

Three online-safety mini-games for kids aged 8 to 12, led by Aiko. Each game
teaches a different skill through a different loop, not through reading text
and answering questions.

| Game | Loop | Skill |
| --- | --- | --- |
| Night Shift | Sorting under time pressure | Spotting scams, phishing and pressure tactics |
| Breadcrumbs | Hidden-object hunting | How small public details add up to identify you |
| Vault | Arcade defence | What actually makes a password strong |

## Running it

The whole product is a single self-contained file, `index.html`. There is no
build step, no dependencies and no network calls. Every image, font and script
is inlined, so it works from a web server, from a USB stick, or opened straight
off disk.

Locally:

    python3 -m http.server 8000

Then open http://localhost:8000

## Deploying

Any static host works. The repo is already set up for GitHub Pages: `.nojekyll`
stops Pages from running Jekyll over the file, and `index.html` at the root is
served as the landing page.

## Why everything is inlined

The original target was a published Claude artifact, where a strict
content-security policy blocks requests to every external host. No CDN, no
remote fonts, no image URLs. That constraint is why the file is around 1 MB:
the six photographs live inside it as base64 JPEGs. It stays useful outside
that context, since a single file with no dependencies cannot break from a dead
link or a missing asset.

## Source assets

`source/` holds the originals, kept here so the artwork can be re-edited later:

- `aiko.svg` is Aiko's vector artwork. The game inlines it as an SVG `<symbol>`
  and swaps expressions by moving eyelid and mouth paths over the shared body.
- `art/*.png` are the six full-resolution Breadcrumbs photographs. The versions
  in the game are square-cropped to 880x880 and compressed to JPEG q82, which
  took 11.3 MB down to 508 KB.

Each photograph deliberately contains a blank area (a shirt patch, a street
sign, a certificate, a monitor). The clue text is drawn over those areas as
live HTML, not baked into the image, so it can highlight on tap, change state
when found, and be read aloud by a screen reader.

## Testing notes

- Works on desktop and touch. Layout switches at 620px.
- Progress is saved to `localStorage`. To test a first run, clear site data or
  open a private window.
- Nothing is collected, transmitted or stored off the device.

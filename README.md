# Photo Grid Composer

A small, single-file web tool that crops photos into squares and composes them
into a 2×2 or 3×3 grid. Built with vanilla JS and the Canvas API — no build
step, no framework, no backend.

## Highlights

- **100% client-side.** Photos never leave the browser. No uploads, no
  servers, no tracking.
- **No accounts, no watermarks, no paywall.** Open the page and use it.
- **Single static file.** `index.html` is the whole app. Drop it on any
  static host or run it locally.
- **Pan & zoom framing.** Click any cell in the output to pan/zoom the
  source photo. Drag · scroll wheel · pinch.
- **Original-resolution export.** PNG output preserves the smallest
  source crop's resolution — no forced downscaling beyond that.
- **Optional center divider** between cells for a paper-collage feel.
- **Lofi paper aesthetic.** Fraunces serif + JetBrains Mono on a warm
  beige palette.

## Usage

Open `index.html` in any modern browser, or visit the live demo (link below).

1. Pick a layout: **2 × 2** (4 photos) or **3 × 3** (9 photos)
2. Drop in or select your photos (JPG / PNG / WEBP)
3. The output grid appears as soon as you have enough photos
4. Click any cell to pan/zoom the framing
5. Toggle **Center divider** if you want gaps between cells
6. **Download PNG** when you're happy

Drag thumbnails in the Photos panel to reorder them.

## Self-host

Just put `index.html` somewhere static:

- GitHub Pages
- Cloudflare Pages
- Netlify / Vercel
- Any web server (`python3 -m http.server` works locally)

There is no build step.

## Tech

- Vanilla JavaScript (ES2020+)
- HTML5 Canvas for cropping and composition
- HTML5 Drag & Drop for thumbnail reordering
- Pointer Events for pan/zoom (mouse and touch)
- Google Fonts CDN for typography (the only external dependency)

The cell size of the final image equals the smallest source crop, so all
cells share a single resolution and no photo is upscaled. The bottleneck
photo is the smallest one — replace it for a higher-resolution result.

## Limits

- Layouts are square only (2×2 and 3×3). No 3:4 / 16:9 / freeform.
- No text, stickers, filters, or effects. This tool does one thing.
- Thumbnail reorder uses HTML5 Drag & Drop, which works on desktop only.
  Cropping/framing works on mobile via touch.

## License

[MIT](LICENSE)

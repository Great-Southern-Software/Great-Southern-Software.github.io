# Great Southern Software — Brand Guide

**Concept: Crux Graph.** The Southern Cross drawn as a node graph. The stars are modules; the sightlines between them are dependencies. The mark says *southern* and *software* in one gesture rather than bolting a constellation next to a laptop.

---

## Palette

| Role | Hex | Notes |
|---|---|---|
| **Ink** | `#0E1726` | Primary background. Near-black with a cold blue bias — night sky, not charcoal. |
| **Star** | `#E8B04B` | The nodes. Warm gold. Use sparingly; it is the only warm colour in the system. |
| **Sightline** | `#8FB8D9` | The edges, and the second line of the wordmark. Cool, recessive. |
| **Paper** | `#F4F6F8` | Light background. Deliberately *cool* off-white, not cream. |
| **Muted** | `#5F7182` | Secondary text, captions, metadata. |

Deliberate choice: no warm cream, no terracotta. The palette is a cold southern night with a single warm point of light, and that contrast is the whole idea. Don't add a third accent colour.

---

## Typography

**Space Grotesk** — the wordmark. Open source (SIL OFL), free for commercial use.
**Inter** or **Inter Tight** — body and UI copy. Also open source.

The wordmark's two lines are set in deliberate tension: `GREAT SOUTHERN` in Bold with tight tracking, `SOFTWARE` in Regular with wide tracking. Don't set both the same — the contrast *is* the wordmark.

**The wordmark in these files is outlined to vector paths.** It renders identically everywhere with no font installed and no licensing question. Never rebuild it as live text.

---

## Files

### Mark only
- `logomark.svg` / `logomark-512.png` — the bare mark, transparent background
- `logomark-tile-dark.svg` / `.png` — mark on a rounded ink tile (app icons, avatars)
- `logomark-mono-ink.svg` — single colour, dark. For stamps, embroidery, one-colour print
- `logomark-mono-white.svg` — single colour, light. For dark photography, merch

### Lockups
- `logo-horizontal-dark.svg` / `.png` — the default. Use this unless you have a reason not to
- `logo-horizontal-light.svg` / `.png` — for light backgrounds
- `logo-horizontal-light-transparent.svg` — same, no background fill
- `logo-stacked-dark.svg` / `logo-stacked-light.svg` — for square and narrow spaces

### Web
- `favicon.svg` — chunkier geometry so it survives small sizes. Not the same file as the logomark
- `favicon.ico` — 16/32/48 bundled, for legacy browsers
- `favicon-{16,32,48,64,180,192,512}.png` — 180 is the Apple touch icon, 192/512 are PWA manifest sizes
- `og-image.png` — 1200×630, for link previews on social, Slack, iMessage

---

## Usage

**Clear space.** Keep free space around the mark equal to the diameter of the largest star (the bottom node). Nothing intrudes into that margin.

**Minimum sizes.** Mark: 24px. Horizontal lockup: 160px wide. Below that, use the mark alone — the wordmark's second line goes to mush.

**Backgrounds.** Ink, paper, or a photograph dark enough that the gold nodes hold. On busy imagery, use the mono white version, not the two-colour one.

**Don't:**
- Recolour the nodes. Gold on ink is the identity.
- Rotate the mark. The Southern Cross has an orientation and people know it.
- Add a gradient, a bevel, or a drop shadow.
- Stretch either lockup non-proportionally.
- Set the wordmark in a different typeface and call it the logo.

---

## Web snippets

```html
<link rel="icon" href="/favicon.ico" sizes="32x32">
<link rel="icon" href="/favicon.svg" type="image/svg+xml">
<link rel="apple-touch-icon" href="/favicon-180x180.png">
<meta property="og:image" content="https://greatsouthernsoftware.com.au/og-image.png">
<meta property="og:image:width" content="1200">
<meta property="og:image:height" content="630">
```

```css
:root {
  --gss-ink:       #0E1726;
  --gss-star:      #E8B04B;
  --gss-sightline: #8FB8D9;
  --gss-paper:     #F4F6F8;
  --gss-muted:     #5F7182;
}
```

---

## One caveat worth keeping in writing

"Great Southern" is a crowded phrase in Australia — most notably Great Southern Bank. Before this goes on anything public-facing, run a trade mark search at IP Australia in **class 9** (software) and **class 42** (software services). A distinctive logo helps: it gives you something protectable that the words alone may not.

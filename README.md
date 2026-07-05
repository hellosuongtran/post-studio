# Post Studio

A single-file, client-side maker for Instagram carousel posts (1080×1350) —
photo/solid backgrounds, big bold headlines (fill/outline/shadow), sticker &
text-box elements, HEIC support, multi-slide export to PNG, plus a **recipe
mode** for automation.

**Live:** https://hellosuongtran.github.io/post-studio/

No build step, no backend. Everything runs in the browser.

## Recipe mode (automation)

Paste a JSON "recipe" into the Recipe box → **Load** (preview) or **Load +
Export all** (renders every slide and downloads each as PNG). Images should be
embedded as base64 `data:` URIs so canvas export isn't blocked by CORS. Plain
`https://` URLs work only if the host sends CORS headers.

You can also drive it from the page console / Chrome automation:
`await PostStudio.loadRecipe({...})` then `PostStudio.exportAll()`.

### Recipe schema

```json
{
  "handle": "@yourhandle",
  "font": "Anton",
  "scrim": "top",
  "scrimStr": 0.45,
  "slides": [
    {
      "bg": { "mode": "photo", "image": "data:image/jpeg;base64,...", "zoom": 1, "offsetX": 0, "offsetY": 0 },
      "kicker": "POV",
      "headline": "AI can code\nfaster than us",
      "body": "Are we cooked?",
      "textStyle": "outline",
      "color": "#FFFFFF",
      "valign": "top",
      "hsize": 120,
      "elements": [
        { "type": "image", "image": "data:image/png;base64,...", "x": 540, "y": 900, "scale": 0.6, "rot": -6, "shadow": true },
        { "type": "text", "text": "1. Context Engineering", "x": 540, "y": 700, "scale": 1, "rot": 0, "box": "#FFFFFF", "color": "#0E1116" },
        { "type": "text", "text": "Nguồn: Microsoft WTI 2026", "x": 350, "y": 1140, "scale": 0.62, "box": "none", "color": "#9AA3AE", "italic": true, "maxw": 1200 }
      ]
    },
    {
      "bg": { "mode": "solid", "color": "#1D4ED8" },
      "headline": "Are we cooked?",
      "textStyle": "fill",
      "color": "#FFFFFF",
      "valign": "top"
    }
  ]
}
```

Field notes:
- `font`: `Anton` | `Archivo Black` | `Inter` | `Oswald`
- `textStyle`: `fill` | `outline` | `shadow`
- `valign`: `top` | `middle` | `bottom`
- `bg.mode`: `photo` (needs `image`) | `solid` (needs `color`)
- text elements: `italic: true` renders italic 400 weight (dùng cho dòng nguồn / chú thích), `maxw` overrides max width before wrap (default 560, tính theo px canvas trước khi nhân `scale`)
- text element `box`: a hex color for a bubble, or `"none"` for plain text (e.g. an arrow `→`)
- canvas is 1080×1350, so `x`/`y` are in that coordinate space

# PETCORP Office Globe

Interactive 3D globe built with Three.js that displays office locations as glowing markers on a rotating Earth.

## Quick Start

Open `index.html` in a browser, or serve it locally:

```bash
npx serve .
```

Deploy to GitHub Pages by pushing this folder to a repo and enabling Pages on the `main` branch.

## URL Parameters

| Parameter    | Default | Description                              |
|-------------|---------|------------------------------------------|
| `theme`     | `dark`  | `dark` or `light`                        |
| `autoRotate`| `true`  | `true` or `false`                        |
| `showArcs`  | `true`  | Show connection arcs from HQ to offices  |
| `focusLat`  | —       | Initial camera latitude focus            |
| `focusLng`  | —       | Initial camera longitude focus           |
| `data`      | —       | URL to a JSON file with custom locations |

Example: `index.html?autoRotate=false&showArcs=false`

## Custom Data

Pass `?data=https://example.com/offices.json` to load a custom dataset. The JSON should be an array of objects matching this shape:

```json
[
  {
    "name": "Office Name",
    "city": "City",
    "country": "Country",
    "address": "Full address",
    "lat": 40.7128,
    "lng": -74.0060,
    "type": "headquarters",
    "employees": "100+",
    "description": "Description"
  }
]
```

Set one location's `type` to `"headquarters"` for the HQ marker style and arc origin.

## Tech

- Three.js v0.172.0 via CDN (unpkg)
- Single HTML file, no build step
- Inter font via Google Fonts

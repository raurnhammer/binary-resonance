# Binary Resonance

Generative art inspired by Manfred Mohr's P-Series algorithms — n-dimensional hypercube projections rendered as evolving grid patterns.

## Overview

Binary Resonance is a single-file generative art piece that implements a Mohr P-Series grid algorithm. It plots diagonal lines across a raster grid, selecting each cell's diagonal direction using noise fields and density falloff from the center. A red accent square breaks the pattern at an algorithmically determined position.

[Demo](https://raurnhammer.github.io/binary-resonance/)

## Features

- **Algorithmic diagonal selection** — Per-cell binary decisions based on Perlin noise fields
- **Density falloff** — Line density decreases toward the edges, creating a radial fade effect
- **Overlay complexity** — A second noise layer adds subtle pattern variation
- **Interactive controls** — Adjust grid size, noise parameters, stroke weight, and falloff in real time
- **Seed-based generation** — Navigate through variations with prev/next/random seed controls
- **Export** — Download transparent PNG or SVG versions

## Parameters

| Parameter | Description | Range |
|---|---|---|
| Grid Rows | Number of grid rows | 10 – 80 |
| Grid Cols | Number of grid columns | 10 – 80 |
| Noise Scale | Primary noise field resolution | 0.1 – 2.0 |
| Noise Scale 2 | Secondary overlay noise resolution | 0.1 – 3.0 |
| Stroke Weight | Line thickness | 0.3 – 2.0 |
| Show Grid Lines | Toggle faint grid overlay | true / false |
| Falloff Exponent | How quickly density fades from center | 0.1 – 5.0 |
| Hard Cutoff | Maximum radius as fraction of diagonal | 0.0 – 1.0 |

## Run Locally

Open `binary-resonance.html` in any modern browser — no build step or server required.

```bash
# Or serve locally for a cleaner experience
python3 -m http.server 8080
# then open http://localhost:8080/binary-resonance.html
```

## Deploy to GitHub Pages

1. Push this file to a repository on GitHub
2. Go to **Settings → Pages**
3. Set **Source** to `Deploy from a branch` → select `main` / `root`
4. Your page will be live at `https://<username>.github.io/<repository>/binary-resonance.html`

## Dependencies

- [p5.js 1.7.0](https://p5js.org/) (loaded via CDN)

## License

Private — Manfred Mohr inspired algorithmic geometry.

# Mechanics Interactive Page

This repository contains a single static HTML page:

- `/home/runner/work/mechanics/mechanics/vectors.html`

It now includes:
1. The original vector calculator.
2. An **Inclined Plane (Tilted Floor) animation** with gravity, normal, and friction forces.

## Run locally

Because this is a client-only static page, you can open the file directly in a browser:

- `file:///home/runner/work/mechanics/mechanics/vectors.html`

Or serve the folder with any static server (for cleaner URL sharing), for example:

```bash
cd /home/runner/work/mechanics/mechanics
python -m http.server 8000
```

Then open `http://localhost:8000/vectors.html`.

## Inclined-plane controls

Editable inputs:

- Angle `θ` (deg)
- Static friction `μs`
- Kinetic friction `μk`
- Mass `m` (kg)
- Gravity `g` (m/s²)

Behavior:

- If `mg sin(θ) <= μs N`, the block remains at rest (static friction balances downslope gravity).
- If `mg sin(θ) > μs N`, the block slides and kinetic friction is used (`fk = μk N`).

Buttons:

- **Play/Pause**
- **Reset** (position + velocity)
- **Restart with new params**

## Share URL + QR code (for TeX/LaTeX)

The page generates a shareable URL from the **current page URL + query parameters** (`angle`, `mus`, `muk`, `mass`, `g`).

- Copy/share the URL directly, or
- Scan/use the generated QR code to open the same parameter set.

Example query:

```text
vectors.html?angle=28&mus=0.45&muk=0.35&mass=2.5&g=9.81
```

For LaTeX workflows, insert the QR image/screenshot into your document so readers can scan and open the same configuration.

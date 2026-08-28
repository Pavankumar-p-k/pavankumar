# PAVAN KUMAR — F1 Model Showcase

A scroll-driven 3D showcase built with Three.js. A fully photoreal 2022 Formula 1 car (local GLB model) is rendered live in the browser and explored by scrolling — panel by panel, spec by spec — over a dark polished race-track floor with a telemetry HUD.

## Features

- Three.js GLB model rendered with PMREM environment lighting, bloom and film-grain post-processing
- Scroll-driven cinematic camera keyframes + subtle idle car spin
- Custom Audi-inspired livery applied procedurally (stripes, carbon, alcantara, black rims, sponsor decals: P ZERO / PAVAN KUMAR)
- Telemetry HUD: scroll-progress dial + current-view readout
- Scroll-reveal section animations (IntersectionObserver)
- **AUTO TOUR** — 34s cinematic auto-scroll of the whole page with the Tokyo Drift soundtrack
- **MUTE / UNMUTE** toggle for the soundtrack
- Responsive: camera auto-frames and HUD/buttons adapt to phones and tablets

## Run locally

The page loads its model and audio from local files, so any static server works:

```bash
python -m http.server 8000
```

Then open http://localhost:8000

## Deploy to GitHub Pages

1. Push this repository to GitHub (branch `main`).
2. Repo → **Settings → Pages** → Source: **Deploy from a branch** → branch `main` / folder `/ (root)` → **Save**.
3. Your site goes live at: `https://<username>.github.io/<repo>/` (here: `https://pavankumar-p-k.github.io/pavankumar/`)
4. First build takes a minute or two — after it reports **Your site is live**, open the URL.

> Tip: audio autoplay is blocked by browsers until the first tap/click — that's expected, not a bug.

## Structure

```
├── index.html                       ← the whole site (HTML + CSS + Three.js app)
├── README.md
└── f1_web_car/
    └── assets/
        ├── car.glb                  ← 2022 F1 car model
        └── audio/
            └── tokyo_drift.mp3      ← AUTO TOUR soundtrack
```
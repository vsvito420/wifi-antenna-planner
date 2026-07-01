# WLAN 3D Antennen Planer

Interactive 3D WiFi antenna pattern visualizer for GitHub Pages.  
Built for Vito's ASUS TUF WiFi 7 Tri-Band router (6 antennas, WiFi 7 Tri-Band).

## Features
- Load OBJ models with textures (select folder in browser)
- iOS-style glass UI, fully mobile touch optimized
- Orbit / pan / pinch-zoom 3D navigation
- Place router and target pins in 3D (tap on surface)
- Transparent wall mode (backface visible, front transparent)
- 6-antenna model: 2 outer L/R + 4 center with adjustable spread
- Neighbor suppression (Nachbarseite dampening)
- Live radiation pattern: mesh + animated particles + antenna direction lines
- Auto-compute optimal angles from placed targets

## Live App
https://vsvito420.github.io/wifi-antenna-planner/

## Deploy
This repo is configured for GitHub Pages from the `main` branch root.
The app lives in `index.html`.

## Pattern Model
Each antenna uses a dipole gain model: G(θ) ∝ sin²(θ) relative to the antenna axis.  
All 6 antennas are summed with weighting, then a neighbor-side suppression factor is applied.

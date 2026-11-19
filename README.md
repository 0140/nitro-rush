# Nitro Rush

A 3D arcade racing game that runs in the browser (three.js r128). One HTML page, no build step.

## Run it

The page loads the car models from the `*.js` files next to it, so serve the folder over HTTP:

```bash
python3 -m http.server 8000
# then open http://localhost:8000/
```

## Features

- 5 tracks: Green Valley, Alpine Pass, Desert Canyon, Coastal Bay, Neon City
- 6 weather types: sunny, sunset, fog, rain (wet road, less grip), snow (less grip), night (headlights) — plus "Mixed"
- Single race or championship (pick several tracks, F1-style points)
- Garage with 4 cars on 2 bodies (GT Coupe, GT Coupe R, Spider, Spider Drift), 8 paint colours
- Crash physics: impulse collisions with spin, body dents at the impact point, damage that costs speed, grip and steering, engine smoke, "wrecked" limp mode
- Nitro, boost pads, AI opponents, split-screen 2 players, touch controls
- Graphics (High/Fast) and brightness settings

## Controls

| Action | 1 player | 2 players |
|---|---|---|
| Steer | ← → or A D | P1: A D · P2: ← → |
| Gas / brake | ↑ ↓ or W S | P1: W S · P2: ↑ ↓ |
| Nitro | Space | P1: Space · P2: Enter |
| Camera | C | C |
| Reset car onto track | R | R |
| Menu | Esc | Esc |

## Files

| File | What it is |
|---|---|
| `index.html` | The whole game: rendering, tracks, physics, AI, HUD, menus |
| `concept_model.js`, `concept_lod.js` | GT Coupe model (detailed + distant), base64 glTF |
| `car_model.js`, `car_lod.js` | Spider model (detailed + distant), base64 glTF |
| `car_ao.png` | Contact shadow under the cars |

## Credits

- **Car Concept** — © 2024 Darmstadt Graphics Group GmbH, model and textures by Eric Chadwick, from the Khronos glTF Sample Assets, licensed [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/). Based on "Free Concept Car 004" by Unity Fan (CC0). Khronos logos were removed; the model was compressed and simplified for this game.
- **Ferrari 458 Italia** — by [vicent091036](https://sketchfab.com/models/57bf6cc56931426e87494f554df1dab6) on Sketchfab, via the three.js examples (`ferrari.glb`, `ferrari_ao.png`). Simplified for this game. Ferrari is a trademark of its owner; this project is not affiliated with it.
- [three.js](https://threejs.org/) (MIT), loaded from cdnjs / jsdelivr.

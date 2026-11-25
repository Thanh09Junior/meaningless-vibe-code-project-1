# ZOMBIE DEFEND (`meaningless-vibe-code-project-1`)

A complete, single-file WebGL2 first-person zombie-defence shooter packed into [`index.html`](./index.html) with **zero local assets** (no external images, audio, models, or font files).

## What `index.html` Contains
All HTML, CSS, JavaScript, and GLSL shaders are self-contained inside `index.html`:
- **Rendering & Shaders (Three.js `0.175.0` via CDN importmap):** Custom GLSL sky dome (gradient, sun/moon disc, FBM clouds, stars), per-mission procedural ground shaders, exponential height fog, GPU weather particles (dust, haze, rain, snow, embers), single shadow-mapped directional light + billboard glow impostors, and a fullscreen post-processing pass (ACES filmic tone mapping, vignette, luminance-masked grain, damage chromatic aberration) with dynamic resolution scaling (`0.6–1.0`).
- **5-Mission Campaign + Endless Survival:** *Last Light*, *Dead Checkpoint*, *Quiet Hospital*, *Whiteout*, and *Red Dawn*, each with distinct lighting/maps, objectives, barricades, 5 zombie types (*Walker*, *Runner*, *Brute*, *Spitter*, *Bloater*), and 5 unique bosses, plus *Rookie / Veteran / Nightmare* difficulties and `localStorage` save progress.
- **Weapons & WebAudio Synth:** 4 procedural primitive viewmodels with first-person hands, spring-damper recoil, multi-stage reloads (*Pistol*, *SMG*, *Shotgun*, *Marksman Rifle*), grenades, between-wave supply shop, radar minimap, and zero-asset procedural WebAudio sound effects + threat-reactive drone.

## Controls
- **Move / Sprint / Crouch / Jump:** `W A S D` / `Shift` / `Ctrl` or `C` / `Space`
- **Aim / Fire / ADS:** Mouse (pointer lock) / `LMB` / `RMB`
- **Reload / Switch Weapons:** `R` / `1–4` or Mouse Wheel
- **Grenade / Flashlight / Interact (Repair & Shop):** `G` / `F` / `E`
- **Pause / Perf Overlay:** `Esc` / `F3`

## GitHub Pages Deployment
This repository is structured for static GitHub Pages hosting with no build step required:
1. Open **Settings → Pages** in this repository.
2. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
3. Select branch **`main`** and folder **`/ (root)`**, then click **Save**.
4. Once built, play at `https://thanh09junior.github.io/meaningless-vibe-code-project-1/` (first load requires internet access to fetch Three.js `0.175.0` from jsDelivr).

## Run Locally
```bash
python -m http.server 8080
```
Open `http://localhost:8080/` in a WebGL2-capable browser.

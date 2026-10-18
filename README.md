# 🪟 FOGGY MIRROR — Photorealistic Window Condensation Edition

> **A photorealistic, camera-driven interactive foggy mirror and steamy window simulation powered by computer vision, 5-layer optical physics, procedural Perlin noise, and hardware-accelerated canvas compositing.**

Experience the authentic sensation of drawing on a steamed-up bathroom mirror or rainy car window. Built for creative technology showcases, hackathons, and tournament competitions, **FOGGY MIRROR** replaces flat white overlays and digital artifacts with a multi-layered, physically inspired condensation simulation featuring microscopic specular water beads, organic cloud variations, meniscus stroke ridges, and warm steam breath restoration.

---

## 🔴 Live Interactive Experience

👉 **[abhineet22singh.github.io/foggy-web](https://abhineet22singh.github.io/foggy-web/)**

---

## 🔬 Photorealistic 5-Layer Condensation Architecture

| Layer | Physical Component | Rendering Technique |
|---|---|---|
| **Layer 1** | **Clear Glass & Optical Light Scattering** | Untouched glass diffuses the background reflection (webcam or atmospheric room) with a 16px Gaussian light-scattering blur. Cleared regions reveal a razor-sharp, high-contrast mirror reflection underneath via hardware-accelerated alpha masks (`destination-in`). |
| **Layer 2** | **Macro Condensation Clouds** | C2-continuous quintic Perlin noise ($6t^5 - 15t^4 + 10t^3$, wavelength ~200px) creating soft, organic variations in moisture density across the pane, with naturally cooler, denser frame perimeter edges. |
| **Layer 3** | **Meso Moisture Eddies & Swirls** | Secondary octave noise (~48px wavelength) producing realistic turbulence, uneven patches of moisture, and delicate translucent mist tendrils. |
| **Layer 4** | **Micro-Droplet Condensation Field** | Over 4,000 microscopic water beads (0.8px–3.2px) rendered with soft contact shadow crescents, refractive bodies, and pinpoint specular catchlights from ambient room lighting. |
| **Layer 5** | **Living Gravity Droplets & Runs** | Fluid water beads with surface tension wobble and gravity acceleration that roll down the glass, wiping clear trickle trails through the condensation. |

---

## ✨ Key Features & Innovations

- 🚫 **Zero Checkerboard / Grid Artifacts:** Replaced blocky integer-step noise with true C2-continuous quintic gradient noise; eliminates repeating patterns and digital grid artifacts.
- 🌫️ **Authentic Translucent Mist Tone:** Replaced flat, chalky white fills with soft neutral mist-greys (`#c2d0df` base in bathroom mode) with natural translucency (0.42 to 0.72 alpha), letting diffused room reflections and ambient lighting shine through realistically.
- ✍️ **Contact Meniscus Edge Ridge:** Etching or wiping with finger/mouse pushes moisture to the perimeter of the stroke, creating a subtle ridge of condensed water beads along the boundary before revealing 100% crystal-clear glass.
- 🌬️ **Organic Nucleation & Steam Breath:** Click **Blow Mist** or hit `B` / `M` to breathe a warm puff of steam onto the glass! Mist blooms outward from the center via organic nucleation sites with an authentic synthesized breath whoosh sound.
- ☝️ **Dual-Mode CV Gesture Tracking:** MediaPipe Hands integration detecting 21 3D landmarks in real time. Point with an index finger (`☝️`) to etch crisp lines; open your palm (`🖐`) to wipe away mist across a broad radius.
- 🎨 **Mirror Moments Presets:** Instant parametric condensation etchings: **Heart**, **Star**, **Smile**, and **Sun** etched with realistic edge-feathered strokes.
- 🧪 **Fog Lab Sandbox:** Modal environment controls to switch live lighting presets (**Bathroom Warmth**, **Obsidian Studio**, **Sunset Glow**), adjust real-time Gaussian scattering blur (4px–32px), and tune droplet density.
- 🎬 **Demonstration Mode (Tour):** 6-stage automated presentation sequence with an on-screen HUD badge demonstrating Draw, Palm Wipe, Stencils, and Optical scattering without manual intervention.
- 📸 **Snapshot Studio:** High-res PNG export (`foggy-mirror-snapshot-<timestamp>.png`) with an optical shutter flash and toast notification.
- ↩️ **Bounded Undo Stack:** Reverses recent stroke or wipe actions (`Ctrl + Z` / `Cmd + Z`).
- 🔊 **Procedural Web Audio Steam:** Zero-asset soothing ambient steam and wiping impulses synthesized purely through Web Audio API pink/white noise nodes (muted by default).

---

## ✋ Interaction Guide

### 1. Pointer / Touch / Stylus Input
- **Draw:** Click/touch and drag across the mirror surface to etch crisp transparent lines through the mist.
- **Wipe:** Switch to Palm Wipe mode (`W`) to clear broad regions with soft, feathered edges.
- **Blow Mist:** Click **Blow Mist** in the toolbar or press `B` or `M` to breathe warm steam onto the glass.
- **Undo:** Click `Undo` in the studio bar or press `Ctrl + Z` (`Cmd + Z` on macOS).
- **Fullscreen:** Press `F` to toggle full-screen immersion.

### 2. Touchless Air Gestures (MediaPipe Hands)
- **☝️ Point Gesture:** Extend only your index finger (curling other fingers) to draw without touching your device.
- **🖐 Open Palm Wipe:** Open all fingers and swipe your hand across the webcam view to wipe away condensation.
- **Interior Reflection Fallback:** If camera access is denied or unavailable, the mirror automatically falls back to an atmospheric interior reflection so all features remain 100% functional.

### 3. Keyboard Shortcuts

| Shortcut | Action |
|---|---|
| `D` | Switch to Draw Mode |
| `W` | Switch to Palm Wipe Mode |
| `B` / `M` | Blow warm breath / steam onto mirror |
| `R` | Re-fog entire mirror organically |
| `C` | Wipe mirror clean |
| `Ctrl + Z` / `Cmd + Z` | Undo last stroke |
| `F` | Toggle Fullscreen |
| `Esc` | Close open modals (Fog Lab, Moments) |

---

## 🚀 How to Run Locally

FOGGY MIRROR has **zero build tools, bundlers, or package installations**. It runs directly as a static web application:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/Abhineet22singh/foggy-web.git
   cd foggy-web
   ```

2. **Open `index.html` in your browser:**
   - **Windows:** Double-click `index.html` or run:
     ```powershell
     Start-Process index.html
     ```
   - **macOS:**
     ```bash
     open index.html
     ```
   - **Linux:**
     ```bash
     xdg-open index.html
     ```

3. When prompted, grant webcam permission to activate hand tracking, or decline to enjoy the atmospheric reflection mode.

---

## 🌐 Deployment to GitHub Pages

1. Push the repository to GitHub:
   ```bash
   git add index.html README.md
   git commit -m "🌫️ FOGGY MIRROR — Photorealistic Window Condensation Redesign"
   git push origin main
   ```
2. Navigate to your repository's **Settings > Pages**.
3. Under **Build and deployment > Source**, choose **Deploy from a branch**.
4. Select `main` branch and `/ (root)` directory, then click **Save**.
5. Your live app is instantly accessible worldwide at `https://<username>.github.io/<repo-name>/`.

---

## 🛠️ Technology Stack

- **HTML5 Multi-Pass Canvas API** — Hardware-accelerated compositing with `destination-in` alpha masking and precomputed texture buffers.
- **Procedural Quintic C2 Perlin Noise** — Multi-octave continuous gradient noise eliminating all checkerboard and tiling artifacts.
- **MediaPipe Hands (`@mediapipe/hands`)** — Real-time 21-point 3D hand tracking at 60 FPS in WebAssembly.
- **Web Audio API** — Real-time procedural white/pink noise synthesis and resonant bandpass breath simulation.
- **Vanilla Modern JavaScript (ES6+) & CSS3** — Zero framework overhead, zero layout shifts, locked 60 FPS rendering pipeline.

---

## 📄 License

MIT License — Built for creative technology competitions, hackathons, and interactive installations.

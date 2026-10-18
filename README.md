# 🪟 FOGGY MIRROR — Ultimate Tournament Edition

> **A photorealistic, camera-driven interactive foggy mirror powered by computer vision, procedural optical physics, and hardware-accelerated canvas compositing.**

Experience the authentic sensation of drawing on a steamed-up bathroom mirror or rainy car window. Built for hackathons and creative technology showcases, **FOGGY MIRROR — Ultimate Tournament Edition** combines real-time 21-point hand tracking with physical light-scattering simulation, dynamic gravity-driven water droplets, procedural audio synthesis, and an interactive preset engine.

---

## 🔴 Live Interactive Experience

👉 **[abhineet22singh.github.io/foggy-web](https://abhineet22singh.github.io/foggy-web/)**

---

## 🏆 Key Tournament Edition Innovations

| Feature | Category | Description |
|---|---|---|
| 🔬 **Optical Light-Scattering Engine** | *Graphics Physics* | Real physics-based multi-scale condensation: pristine glass has a 16px Gaussian light-scattering blur, while wiped/etched regions reveal a razor-sharp, high-contrast mirror reflection underneath via destination-in alpha masks. |
| ☝️ **Dual-Mode Gesture Tracking** | *Computer Vision* | MediaPipe Hands integration detecting 21 3D landmarks in real time. Point with an index finger (`☝️`) to etch crisp lines; open your palm (`🖐`) to wipe away mist across a broad radius. |
| 🎨 **Mirror Moments Presets** | *Interactive Stencils* | Instant parametric condensation etchings: **Heart**, **Star**, **Smile**, and **Sun** etched with realistic edge feathered strokes. |
| 🧪 **Fog Lab Sandbox** | *Real-Time Shaders* | Customizer modal offering dynamic ambient lighting environments (**Bathroom Warmth**, **Obsidian Studio**, **Sunset Glow**), real-time blur radius tuning (4px–32px), and droplet density controls. |
| 🎬 **Demonstration Mode (Judge Tour)** | *Hackathon Showcase* | 6-stage automated showcase sequence with an on-screen HUD badge demonstrating Draw, Palm Wipe, Stencils, and Optical scattering without manual intervention. |
| 💧 **Physics-Based Water Droplets** | *Simulation* | Glistening water beads with realistic specular highlights that accelerate under gravity down the glass pane, leaving clear trickle trails. |
| ⏳ **Dynamic Delta Re-fogging** | *Atmospheric Lifecycle* | Smooth, frame-rate independent (delta-ms) condensation recovery with 4 selectable speeds: Paused (0x), Slow (0.5x), Normal (1.0x), and Fast (2.5x). |
| 📸 **Snapshot Studio** | *Export Suite* | Composites all canvas layers (reflection + fog + etched paths + active droplets) into a downloadable high-resolution PNG (`foggy-mirror-snapshot-<timestamp>.png`) with an optical shutter flash. |
| ↩️ **Bounded Undo History** | *Productivity* | Reverses the most recent stroke or wipe gesture seamlessly with `Ctrl + Z` / `Cmd + Z`. |
| 🔊 **Procedural Web Audio Steam** | *Audio Synthesis* | Zero-asset soothing ambient steam and wiping impulses synthesized purely through Web Audio API pink/white noise nodes (muted by default). |
| 🖥️ **Studio-Grade Responsive UI** | *Apple/Spotify Aesthetic* | Graphite/charcoal palette with Plus Jakarta Sans typography, refined micro-interactions, full keyboard shortcuts, and responsive layouts across phones, tablets, and desktops. |

---

## ✋ Interaction Guide

### 1. Pointer / Touch / Stylus Input
- **Draw:** Click/touch and drag across the mirror surface to etch crisp transparent lines through the mist.
- **Wipe:** Switch to Palm Wipe mode (`W`) to clear broad regions with soft, feathered edges.
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
| `Ctrl + Z` / `Cmd + Z` | Undo last stroke |
| `R` | Re-fog entire mirror |
| `C` | Wipe mirror clean |
| `F` | Toggle Fullscreen |
| `Esc` | Close open modals (Fog Lab, Help) |

---

## 🚀 How to Run Locally

FOGGY MIRROR is built with zero dependencies, build tools, or bundlers. You can run it instantly from source:

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
   git commit -m "🏆 FOGGY MIRROR — Ultimate Tournament Edition"
   git push origin main
   ```
2. Navigate to your repository's **Settings > Pages**.
3. Under **Build and deployment > Source**, choose **Deploy from a branch**.
4. Select `main` branch and `/ (root)` directory, then click **Save**.
5. Your live app is instantly accessible worldwide at `https://<username>.github.io/<repo-name>/`.

---

## 🛠️ Architecture & Technologies

- **MediaPipe Hands (`@mediapipe/hands`)** — Real-time 21-point 3D hand tracking at 60 FPS in WebAssembly.
- **HTML5 Dual-Canvas Compositing** — Dual-pass rendering using a background reflection canvas and an offscreen alpha masking canvas (`sharpCanvas`) with `globalCompositeOperation = 'destination-in'`.
- **Procedural Multi-Scale Fractal Noise** — Layered per-pixel condensation texture generation with natural variations in moisture density.
- **Web Audio API** — Real-time biquad-filtered noise generation for dynamic steam acoustics.
- **Vanilla Modern JavaScript (ES6+) & CSS3** — Zero framework overhead, zero layout shifts, 60 FPS rendering pipeline.

---

## 📄 License

MIT License — Built with pride for creative technology competitions and hackathons.

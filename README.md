# 🪟 FOGGY MIRROR

> **An interactive, camera-driven foggy mirror with computer-vision gesture etching, dual pointer drawing, and real-time condensation physics.**

Experience the tactile sensation of drawing on a steamed-up bathroom mirror or rainy car window. Powered by computer vision and hardware-accelerated Canvas rendering, **FOGGY MIRROR** tracks your hand in real time to let you sketch with your index finger, wipe away mist with your open palm, or draw directly with high-precision mouse, stylus, and touch input.

---

## 🔴 Live Experience

👉 **[abhineet22singh.github.io/foggy-web](https://abhineet22singh.github.io/foggy-web/)**

---

## ✨ Features & Capabilities

| Feature | Description |
|---|---|
| ☝️ **Draw Mode** | Precision etching with connected stroke interpolation; leaves crisp lines through the condensation |
| 🖐 **Palm Wipe Mode** | Broad surface wipe mimicking an open palm; clears wide, soft-edged windows on the glass |
| ↩️ **Bounded Undo** | Reverses the most recent stroke or wipe action (`Ctrl + Z` / `Cmd + Z`) |
| 🔬 **Photorealistic Fog Engine** | Real physics-based optical light scattering blur; untouched areas display a realistic 16px Gaussian diffusion, while cleared areas reveal the crystal-clear reflection underneath |
| 💧 **Dynamic Water Droplets** | Glistening water beads roll down the mirror with natural gravity acceleration, carving clear trickle trails |
| ⏳ **Dynamic Re-fogging** | Time-based (delta-ms) continuous condensation recovery with 4 selectable speeds: Paused (0x), Slow (0.5x), Normal (1.0x), Fast (2.5x) |
| 🎛️ **Comprehensive Studio Toolbar** | Real-time adjustment for Brush Size (4–44px), Fog Density (65–100%), Stroke Softness (10–100%), and Re-fog Rate |
| 📸 **Snapshot & PNG Export** | Composites all active mirror layers into a downloadable high-resolution image (`foggy-mirror-snapshot.png`) with optical shutter flash |
| 🔊 **Atmospheric Sound Synthesis** | Optional soothing ambient steam atmosphere synthesized via Web Audio API (zero external assets, muted by default) |
| 🖥️ **Fullscreen Mirror Mode** | Expands the mirror to the full viewport with keyboard support (`F` to toggle) |
| 📱 **Responsive Multi-Device Support** | Flawless operation on iPhones, Android phones, iPads, laptops, and ultra-wide desktop monitors |

---

## ✋ Interaction Guide

### 1. Direct Pointer / Touch / Stylus
- **Draw:** Click/touch and drag across the mirror surface to draw crisp lines.
- **Wipe:** Switch to Wipe mode in the toolbar and drag across the surface to clear broad regions.
- **Undo:** Press `Undo` in the control panel or hit `Ctrl + Z` / `Cmd + Z` on your keyboard.

### 2. In-Air Hand Gestures (MediaPipe Hands)
- **☝️ Draw Mode:** Point with only your index finger extended (curl remaining fingers) to draw without touching the screen.
- **🖐 Wipe Mode:** Open all fingers and move your hand across the webcam frame to clear mist.
- **Atmospheric Reflection Mode:** If a webcam is unavailable or permission is denied, the application automatically activates a realistic interior mirror reflection.

---

## 🚀 How to Run Locally

FOGGY MIRROR has **zero build tools, bundlers, or package installations**. It runs directly as a static web application:

1. Clone the repository:
   ```bash
   git clone https://github.com/Abhineet22singh/foggy-web.git
   cd foggy-web
   ```
2. Open `index.html` in any modern web browser (Google Chrome, Microsoft Edge, Safari, Mozilla Firefox):
   - **Windows:** Double-click `index.html` or run `Start-Process index.html`
   - **macOS:** `open index.html`
   - **Linux:** `xdg-open index.html`
3. Allow camera access when prompted by the browser to enable hand tracking.

---

## 🌐 Deploying to GitHub Pages

1. Commit and push your changes to the `main` branch:
   ```bash
   git add .
   git commit -m "Deploy Foggy Mirror"
   git push origin main
   ```
2. On GitHub, navigate to **Settings > Pages**.
3. Under **Build and deployment > Source**, select **Deploy from a branch**.
4. Choose the `main` branch and `/ (root)` folder, then click **Save**.
5. Your live app will be accessible at:
   `https://<username>.github.io/<repository-name>/`

---

## 🛠️ Technology Stack

- **MediaPipe Hands** — Real-time 21-point 3D hand landmark detection running locally at 60 FPS
- **HTML5 Canvas API** — Multi-pass optical compositing, destination-in alpha masking, and per-pixel condensation rendering
- **Web Audio API** — Real-time procedural white/pink noise synthesis for soothing ambient steam
- **Vanilla JavaScript & CSS** — High-performance zero-dependency architecture with Apple/Spotify-inspired dark theme

---

## 📄 License

MIT License — Feel free to use, modify, and share!

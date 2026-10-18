# 🪟 MIST • Studio Glass

> **An interactive, camera-driven foggy mirror with computer-vision gesture etching and real-time condensation physics.**

Experience the tactile sensation of drawing on a steamed-up bathroom mirror or rainy car window. Powered by computer vision, **MIST** tracks your hand in real time to let you sketch with your index finger, wipe away mist with your open palm, and watch as condensation droplets trickle down the dense glass.

---

## 🔴 Live Experience

👉 **[abhineet22singh.github.io/foggy-web](https://abhineet22singh.github.io/foggy-web/)**

---

## ✨ Studio Features

| Feature | Description |
|---|---|
| ☝️ **Gesture Etching** | Point your index finger to etch clear lines, write text, or sketch on the steam |
| 🖐 **Surface Wipe** | Move your open palm in front of the lens to wipe away fog with physical hand dimensions |
| 💧 **Condensation Physics** | Glistening water beads naturally roll down the mirror and physically carve trickle trails |
| 🌫️ **Studio Steam Engine** | Per-pixel frosted condensation with realistic specular light sheen and micro-noise |
| 🎛️ **Floating Control Dock** | Dial in your Tip Radius, Steam Density, and Refog Rate with real-time numeric readouts |
| 📸 **Studio Snapshot** | Capture high-resolution PNG snapshots with a camera shutter flash and toast notification |
| 📱 **Cross-Platform Responsive** | Optimized for mobile touch, tablets, laptops, and ultra-wide displays |

---

## ✋ Hand Gesture Guide

- **☝️ Draw Mode:** Point with only your index finger extended (curl remaining fingers) to write and draw with high precision.
- **🖐 Wipe Mode:** Open all fingers and move your hand across the frame to clear large areas of the mirror surface.
- **📱 Touch Fallback:** On mobile phones and touchscreens, you can also touch and drag directly across the glass.

---

## 🚀 How to Run Locally

No build tools, bundlers, or package installations needed. Simply clone and open `index.html` in any modern web browser:

```bash
git clone https://github.com/Abhineet22singh/foggy-web.git
cd foggy-web
# Open index.html in Chrome, Edge, Safari, or Firefox
```

> **Note:** Grant webcam permissions when prompted by your browser.

---

## 🛠️ Technology Stack

- **MediaPipe Hands** — Real-time 21-point 3D hand landmark detection running locally at 60 FPS
- **HTML5 Canvas API** — Per-pixel alpha compositing, gradient water beads, and dynamic smear buffers
- **Vanilla JavaScript** — High-performance zero-dependency architecture
- **Apple / Spotify-Inspired UI** — Translucent frosted glass materials (`backdrop-filter`), bespoke typography (`Plus Jakarta Sans`), and subtle micro-interactions

---

## 📄 License

MIT — Feel free to explore, customize, and share!

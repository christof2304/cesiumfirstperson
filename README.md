# 🎮 CesiumJS First-Person Navigation with Gamepad Support

Explore Google Photorealistic 3D Tiles like a video game – with keyboard, mouse, or Xbox/PlayStation controller.

![First-Person NYC Demo](screenshot.png)

## ✨ Features

- **First-Person Controls** – WASD + mouse, just like a game
- **Gamepad Support** – Xbox, PlayStation, and compatible controllers
- **Adaptive Quality** – Auto-adjusts to your GPU (Ultra/High/Medium/Low)
- **Real-time Shadows** – Toggle on/off for performance
- **6GB VRAM Optimized** – Tuned for mid-range GPUs
- **FPS & VRAM Monitor** – See performance in real-time

## 🚀 Quick Start (Cesium Sandcastle)

1. Open [Cesium Sandcastle](https://sandcastle.cesium.com/)
2. Delete the default code in the editor
3. Copy the entire content of `first-person-gamepad.js`
4. Paste into Sandcastle
5. Click **Run (F8)**
6. Press **C** to activate first-person mode

> **Note:** You need a [Cesium ion](https://ion.cesium.com/) account (free) to access Google Photorealistic 3D Tiles.

## 🎮 Controls

### Keyboard

| Key | Action |
|-----|--------|
| **C** | Toggle First-Person Mode |
| **WASD** | Move |
| **Space / E** | Up / Down |
| **Shift** | Speed Boost |
| **X** | Toggle Shadows |
| **Q** | Cycle Quality |
| **R** | Reset to Auto Quality |

### Gamepad (Xbox / PlayStation)

| Button | Action |
|--------|--------|
| **A / X** | Toggle First-Person Mode |
| **Left Stick** | Move |
| **Right Stick** | Look |
| **Triggers** | Up / Down |
| **B / Circle** | Speed Boost |
| **X / Square** | Toggle Shadows |

## ⚙️ Configuration

All settings are in the `CONFIG` object at the top of the file:

```javascript
const CONFIG = {
  startPosition: { lon: -74.0170, lat: 40.7033, height: 200 }, // NYC
  
  controls: {
    baseMoveSpeed: 8.0,
    mouseSensitivity: 0.005,
    gamepadDeadzone: 0.15,
    // ...
  },
  
  adaptive: {
    targetFPS: 55,
    // ...
  }
};
```

### Change Starting Location

```javascript
startPosition: { lon: YOUR_LON, lat: YOUR_LAT, height: 200 }
```

### Adjust Movement Speed

```javascript
controls: {
  baseMoveSpeed: 12.0,      // Faster
  speedMultiplier: 6.0,     // Shift boost
}
```

## 📊 Quality Presets

| Preset | SSE | Resolution | VRAM |
|--------|-----|------------|------|
| Ultra | 2.0 | 100% | 2048 MB |
| High | 4.0 | 100% | 2048 MB |
| Medium | 8.0 | 95% | 1536 MB |
| Low | 16.0 | 85% | 1024 MB |

The adaptive system automatically switches between presets based on your FPS.

## 🛠️ Requirements

- Modern browser (Chrome, Edge, Firefox)
- WebGL 2.0 support
- 4-6 GB VRAM recommended
- Cesium ion account (free tier works)

## 💡 Tips

- **Slow loading?** Google 3D Tiles load faster during off-peak hours. First load takes longer – tiles are cached afterwards.
- **Low FPS?** Press **Q** to switch to a lower quality preset, or let the adaptive system handle it automatically.
- **Gamepad not detected?** Press any button on your controller, then click the "Detect" button in the UI.

## 📄 License

MIT License – feel free to use, modify, and share.

## 👤 Author

**Christof Lorenz**

- 💼 [LinkedIn](www.linkedin.com/in/christoflorenz)
- 📧 christof2304@gmail.com

---

*Part of my CesiumJS tips series – follow me on LinkedIn for more!*

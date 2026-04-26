# 🕸️ Cat's Cradle - Neon String System

An interactive real-time hand-tracking art experience built with **MediaPipe Hands** and **p5.js**.  
Hold both hands in front of your webcam and watch glowing laser strings weave between your fingertips. Touch them together to trigger neon particle explosions.

---

## ✨ Features

- 🎥 **Live Webcam Feed** - Uses your browser's camera in real time (no data is sent to any server)
- 🖐️ **Dual Hand Tracking** - Detects and tracks both hands simultaneously using MediaPipe Hands
- 🌈 **Elastic Neon Strings** - Glowing laser-beam strings connect matching fingertips across both hands; color shifts from **cyan → magenta → yellow** as hands stretch apart
- 💥 **Particle Explosions** - Touch any two matching fingertips together to trigger a burst of neon particles
- 🫧 **Glowing Joints** - Every hand landmark is rendered as a glowing neon dot; fingertips are extra bright
- 📺 **CRT Aesthetic** - Scanline overlay, vignette, and flicker animation for a retro-futuristic feel
- 🌌 **Futuristic HUD** - Minimal status bar with live hand-tracking feedback

---

## 🚀 How to Run

### Option 1 — Open Locally
1. Download `cats_cradle.html`
2. Open it in **Google Chrome** or **Microsoft Edge**
3. Allow camera access when prompted
4. Show both hands to the camera and start weaving!

> ⚠️ **Do NOT open the file in Firefox directly from disk** — Firefox blocks camera access for `file://` URLs. Use Chrome/Edge, or serve it locally (see Option 2).

### Option 2 — Serve Locally (any browser)
```bash
# Python 3
python -m http.server 8080

# Then open:
http://localhost:8080/cats_cradle.html
```

### Option 3 — GitHub Pages (live link)
1. Push to your GitHub repo
2. Go to **Settings → Pages → Source → main branch**
3. Visit `https://chirag11365.github.io/Cats-cradle/cats_cradle.html`

---

## 📷 Camera Access

This app **requires webcam access** to work. Here's what you need to know:

| Topic | Details |
|---|---|
| **Permission** | Your browser will ask for camera permission the first time. Click **Allow**. |
| **Privacy** | All processing happens **100% locally in your browser**. No video or data is ever uploaded or stored. |
| **HTTPS required** | Camera access only works on `localhost` or a secure `https://` URL. It will not work on plain `http://` remote URLs. |
| **Best browser** | Google Chrome or Microsoft Edge (latest version recommended) |
| **Camera not working?** | See the Troubleshooting section below |

---

## 🕹️ How to Use

1. **Allow camera** when the browser asks
2. **Show both hands** to the camera — hold them up clearly in the frame
3. **Spread your hands apart** to stretch the glowing strings
4. **Bring fingertips together** (left index → right index, etc.) to trigger particle explosions
5. **Move freely** — the strings update in real time at up to 60fps

> 💡 **Tip:** Works best with good lighting and a plain background behind your hands.

---

## 🛠️ Tech Stack

| Library | Version | Purpose |
|---|---|---|
| [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands) | Latest | Real-time hand landmark detection |
| [p5.js](https://p5js.org/) | 1.9.4 | Canvas rendering and animation |
| [MediaPipe Camera Utils](https://www.npmjs.com/package/@mediapipe/camera_utils) | Latest | Webcam feed management |

All libraries are loaded via **CDN** — no installation or build step needed.

---

## 🔧 Troubleshooting

**Camera permission denied**
- Click the 🔒 lock icon in your browser's address bar → set Camera to **Allow** → refresh the page

**Black screen / no video**
- Make sure you're on `localhost` or an `https://` URL (camera blocked on plain `http://` remote)
- Check that no other app (Zoom, Teams, etc.) is using your camera
- Try a different browser (Chrome recommended)

**Hands not detected**
- Ensure your hands are well-lit and clearly visible
- Keep hands within the camera frame
- Avoid wearing gloves or very dark nail polish that blends with the background

**Laggy performance**
- Close other browser tabs and resource-heavy apps
- Make sure hardware acceleration is enabled in your browser settings
- The app runs best on a machine with a dedicated GPU

---

## 📁 Project Structure

```
Cats-cradle/
├── cats_cradle.html   # The entire application (single file)
└── README.md          # This file
```

---

## 🌐 Browser Support

| Browser | Supported |
|---|---|
| Google Chrome 90+ | ✅ Yes |
| Microsoft Edge 90+ | ✅ Yes |
| Safari 15+ | ⚠️ Limited (may have MediaPipe issues) |
| Firefox | ⚠️ Needs local server (`file://` blocks camera) |

---

## 📜 License

This project is open source and free to use, modify, and share.

---

## 🙌 Credits

Built with ❤️ using [MediaPipe](https://mediapipe.dev/) by Google and [p5.js](https://p5js.org/).

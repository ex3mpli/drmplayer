# DRMPlayer

A lightweight, modern, and responsive HTML5 video player built with [Shaka Player](https://github.com/shaka-project/shaka-player). Designed for seamless playback of HLS (`.m3u8`), DASH (`.mpd`), and DRM-protected streams directly in your web browser.

## Screenshots
<img src="https://ex3mpli.github.io/drmplayer/mobile-ss1.jpg" alt="Website Screenshot" />

<img src="https://ex3mpli.github.io/drmplayer/mobile-ss2.jpg" alt="Website Screenshot" />

---
<a href="https://ex3mpli.github.io/drmplayer/index.html" target="_blank" rel="noopener noreferrer">Demo</a>

---

##  Features

- **Modern UI**: Glassmorphism design with auto-hiding controls and smooth animations.
- **Broad Format Support**: Native support for DASH (`.mpd`) and HLS (`.m3u8`) via Shaka Player.
- **DRM Ready**: Built-in support for **ClearKey** and **Widevine** DRM configurations.
- **Advanced Networking**: Ability to inject custom `User-Agent` and `Referer` headers for restricted streams.
- **Smart Controls**: 
  - Double-tap left/right to seek ±10 seconds.
  - Manual quality selection (Auto, 1080p, 720p, etc.).
  - Picture-in-Picture (PiP) and Fullscreen modes.
- **Persistent Settings**: Saves your last used URL, headers, and volume to `localStorage`.
- **Keyboard Shortcuts**: Full keyboard navigation for desktop users.

## Getting Started

### Option 1: Direct Open (Basic Streams)
1. Save the code as `index.html`.
2. Double-click the file to open it in any modern browser (Chrome, Firefox, Edge, Safari).

### Option 2: Local Server (Recommended for DRM/CORS)
*Note: Some streams and DRM licenses enforce CORS policies that block direct `file://` access.*
1. Install a simple local server (e.g., VS Code "Live Server" extension, or Python: `python -m http.server 8000`).
2. Open `http://localhost:8000` in your browser.

## ⚙️ How to Use

1. **Main URL**: Paste your `.m3u8` or `.mpd` manifest URL in the main input bar and click **▶ Play**.
2. **Advanced Settings**: Click the ⚙️ (gear) icon to expand advanced options:
   - **DRM Type**: Select `None`, `ClearKey`, or `Widevine`.
   - **ClearKey**: Enter key pairs in the format `kid:key` (one per line).
   - **Widevine**: Paste your license server URL.
   - **Custom Headers**: Add a `User-Agent` or `Referer` if the stream blocks default browser requests.
3. **Save Defaults**: Click "💾 Save as Default" to remember your configuration for future sessions.

## Keyboard Shortcuts

| Key | Action |
| :--- | :--- |
| `Space` or `K` | Play / Pause |
| `F` | Toggle Fullscreen |
| `M` | Toggle Mute |
| `←` (Left Arrow) | Seek backward 5 seconds |
| `→` (Right Arrow) | Seek forward 5 seconds |
| `↑` (Up Arrow) | Increase Volume |
| `↓` (Down Arrow) | Decrease Volume |

## Mobile & Touch Support

- **Tap once**: Show/hide controls.
- **Double-tap left side**: Rewind 10 seconds.
- **Double-tap right side**: Fast-forward 10 seconds.
- **Drag progress bar**: Seek to a specific time.

## Disclaimer

This player is provided for **educational, testing, and development purposes only**. Ensure you have the legal right and proper authorization to access and decrypt any DRM-protected content you test with this tool. The developer is not responsible for any misuse of this software.

## Tech Stack

- **Core**: HTML5, CSS3, Vanilla JavaScript
- **Player Engine**: Shaka Player v4.7.0
- **Styling**: Custom CSS with Backdrop Filter (Glassmorphism)
- **Fonts**: Inter (via Google Fonts)

---
*Built for seamless streaming.*

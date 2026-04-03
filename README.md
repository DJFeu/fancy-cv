# Fancy CV

A cyberpunk-themed interactive resume built as a single HTML file. Features a Matrix-style terminal interface with typing animations, 3D effects, and sound design.

## Demo

Open `index.html` in any modern browser — no build tools or server required.

## Features

- **Matrix Rain** — 3D falling characters rendered with Three.js (r128)
- **Terminal UI** — Retro terminal window with typing animation and blinking cursor
- **Trading Chart** — Animated depth chart with buy/sell buttons
- **Sound System** — Background music, typing SFX, coin/error sounds (Web Audio API)
- **Responsive** — Adapts layout for mobile and desktop
- **Click to Start** — Audio context initializes on user interaction (browser policy compliant)

## How to Customize

All content lives in the `texts` array inside `index.html` (~line 1761):

```javascript
const texts = [
  { id: 'name', text: 'Your Name', speed: 120 },
  { id: 'title', text: 'Your Title', speed: 60 },
  { id: 'bio', text: 'Your bio...', speed: 30 },
  { id: 'skills', text: '## Technical Skills\n> ...', speed: 20 },
  { id: 'experience', text: '## Professional Experience\n• ...', speed: 25 },
  { id: 'current', text: '## Current Focus\n→ ...', speed: 30 },
  { id: 'contact', text: '## Contact\nmailto:you@example.com\nhttps://...', speed: 40 },
];
```

- `speed` — typing delay in ms (lower = faster)
- `isWrong` / `correctText` — type-then-delete-and-retype effect
- `isChart` / `isFormula` — triggers trading chart or Kelly formula display

## Tech Stack

| Layer | Technology |
|-------|------------|
| 3D Graphics | Three.js (CDN, r128) |
| Fonts | Google Fonts — Fira Code, Share Tech Mono, VT323, Space Mono |
| Audio | Web Audio API (oscillator-based, no external files) |
| Styling | Embedded CSS with keyframe animations |
| Logic | Vanilla JavaScript, no frameworks |

## Project Structure

```
fancy-cv/
└── index.html    # Everything — HTML, CSS, JS in one file
```

## Browser Support

Works in all modern browsers (Chrome, Firefox, Safari, Edge). Safari users may need an extra click to activate audio.

## License

MIT

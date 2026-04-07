# 🎵 Web Harmonium

A fully functional, browser-based harmonium instrument with authentic reed synthesis — no plugins, no dependencies, just open and play.

---

## Features

### Sound Engine
- **Custom reed synthesis** — 15-harmonic overtone series tuned to real harmonium reed spectra
- **Triple-oscillator voicing** per note for warmth, depth, and natural chorus
- **Convolution reverb** with synthetic impulse response
- **Adjustable tremolo** via LFO modulation

### Reed Stops (like a real harmonium)
| Stop | Description |
|------|-------------|
| BASS | Full warm low register |
| MAIN | Primary reed voice |
| HIGH | Octave-up reed |
| CHORUS | Slightly detuned shimmer |
| SUB | Sub-octave bass reed |

Mix and match stops to sculpt your sound.

### Controls
- **Volume** slider
- **Reverb** depth slider
- **Tremolo** rate slider
- **Octave** selector (range: 1–6)
- **Transpose** (±6 semitones)

### Keyboard
- 3 playable octaves with mouse and touch support
- **Computer keyboard mapping** (see below)
- Live "notes playing" display
- Animated bellows that pulse while notes sound

---

## Keyboard Shortcuts

### White Keys
```
A  S  D  F  G  H  J  K  L  ;  '
C  D  E  F  G  A  B  C  D  E  F
```

### Black Keys
```
W  E     T  Y  U     O  P
C# D#    F# G# A#    C# D#
```

### Other
| Key | Action |
|-----|--------|
| `Z` | Octave down |
| `X` | Octave up |

---

## Getting Started

No build step. No dependencies. Just a single HTML file.

```bash
git clone https://github.com/your-username/web-harmonium.git
cd web-harmonium
open harmonium.html   # or just double-click
```

Or serve it locally:

```bash
npx serve .
# then open http://localhost:3000
```

---

## How It Works

The audio engine is built entirely on the **Web Audio API**:

1. **Oscillators** — each note spins up 3 oscillators with a custom `PeriodicWave` modelling harmonium reed harmonics
2. **Stops** — each reed stop adds another layer of oscillators at different octaves/detune amounts
3. **Envelope** — a fast attack (25ms) with slight decay mimics the bellows-driven reed response
4. **Reverb** — a synthetic impulse response is generated procedurally (no audio files needed)
5. **Tremolo** — a low-frequency oscillator modulates the master gain node

All audio is created on first interaction to comply with browser autoplay policies.

---

## Browser Support

Works in any modern browser with Web Audio API support:

- Chrome / Edge 66+
- Firefox 76+
- Safari 14.1+
- Mobile Chrome & Safari

---

## License

MIT — do whatever you like with it.

---

## Acknowledgements

Inspired by the original [Web Harmonium](https://rajaramaniyer.github.io/webharmonium.html) by Rajaraman Iyer. Built from scratch with a focus on sound quality, playability, and visual design.
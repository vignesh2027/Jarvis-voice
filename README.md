# J.A.R.V.I.S — Just A Rather Very Intelligent System

A JARVIS-style AI voice assistant with 42 particle simulations, British voice, and Groq-powered intelligence.

---

## Setup

### 1. Clone the repo

```bash
git clone https://github.com/vignesh2027/Jarvis-voice.git
cd Jarvis-voice
```

### 2. Add your Groq API key

```bash
cp config.example.js config.js
```

Open `config.js` and replace `gsk_YOUR_GROQ_API_KEY_HERE` with your real key from [console.groq.com](https://console.groq.com/).

```js
const GROQ_CONFIG = {
  apiKey: "gsk_your_real_key_here",
  model: "llama3-8b-8192",
  endpoint: "https://api.groq.com/openai/v1/chat/completions"
};
```

> `config.js` is in `.gitignore` — your key will never be committed.

### 3. Run locally

Open `index.html` directly in Chrome or Edge — no server needed.

Or use a simple server:
```bash
python3 -m http.server 8080
# then open http://localhost:8080
```

---

## How to use

| Action | Result |
|---|---|
| Click mic button | Start voice input |
| Press `SPACE` | Toggle voice listening |
| Press `ESC` | Stop listening / stop speech |
| Say a sim name | Switch particle simulation instantly |
| Keys `1`–`0` | Quick switch: vortex, galaxy, neural, fire, matrix, aurora, heartbeat, disco, nebula, wormhole |
| Click `SIM PANEL` | Open simulation selector |

---

## Deploy to GitHub Pages

1. Push to GitHub (make sure `config.js` is NOT committed):
```bash
git add -A
git commit -m "deploy JARVIS"
git push origin main
```

2. Go to your repo → **Settings** → **Pages** → set source to `main` branch, root folder.

3. Your site will be live at `https://vignesh2027.github.io/Jarvis-voice/`

> **Note:** GitHub Pages serves the site without `config.js`. Visitors must supply their own key — or you can fork the repo and embed the key in a private deployment.

---

## Particle Simulations (42 modes)

vortex, dna, galaxy, neural, wave, sphere, orbit, rain, fire, matrix, spiral, explode, flow, constellation, wormhole, reactor, storm, network, aurora, clock, repel, attract, fountain, chaos, grid, morph, laser, bounce, rings, tunnel, comet, mist, shockwave, disco, weave, magneto, nebula, crystal, heartbeat, swarm, pulse, snowflake

Activate any by **saying the name aloud** or clicking in the SIM PANEL.

---

## Tech Stack

- **AI**: Groq API (`llama3-8b-8192`)
- **Voice Input**: Web Speech API (SpeechRecognition)
- **Voice Output**: Web Speech API (SpeechSynthesis)
- **Graphics**: Canvas API (custom particle engine)
- **Stack**: Vanilla HTML, CSS, JS — zero dependencies

---

## Browser Support

| Browser | Voice | Particles |
|---|---|---|
| Chrome | Full | Full |
| Edge | Full | Full |
| Safari | Partial | Full |
| Firefox | No voice input | Particles only |

---

*"I was designed to be helpful, not agreeable." — J.A.R.V.I.S*

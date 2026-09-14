# Hughes Memorial Stadium — 3D Model & Interactive Simulations

An interactive **three.js** model of [Hughes Memorial Stadium](https://en.wikipedia.org/wiki/Hughes_Memorial_Stadium) (Morgan State University, Baltimore, MD) built to its official dimensions — **120 yds × 160 ft (57,600 sq ft)** — including the 8-lane running track, turf field, press boxes, seating and the scoreboard. Fully self-contained in a single HTML file (three.js via CDN; no build step).

## 🐻 Project Statement

**@Morgan State University — Hughes Stadium 3D Modeling, Renovation Project Simulation & Football Game Replay**

- **Agentic AI Setup:** Hermes Desktop + Ollama + Qwen3.8 27B (Reasoning: Medium) · RTX 5090 eGPU · AMD 395+
- **Vibe Coding & 3D Modeling:** three.js

Qwen is a multimodal model — it reads text **and** vision — so beyond the text prompt, the following materials were fed to the AI agent:

| Input | Description | Source |
|-------|-------------|--------|
| 🖼 Images | Drone and ground views of Hughes Stadium, manually searched from the web | e.g. [Morgan State Facebook post](https://www.facebook.com/morganstateu/posts/its-bear-family-weekend-and-the-morgan-state-bears-are-ready-for-kickoff-bring-t/1475242091317320/) |
| 📄 PDF | 11/9/2019 game NC A&T vs MSU — official box score | https://ncataggies.com/football/2019/boxscore/at-morgan-state/2499/pdf |
| 🎬 Video | @Beynon Sports — construction timelapse video | https://app.oxblue.com/open/benyon/morganstate |
| 🌐 Webpages | Additional webpages searched by the AI agent | e.g. the 2019 rosters for the Bears and the Aggies |

## 🎬 Demo Video

Full walkthrough — 3D stadium showcase, the complete renovation simulation (3× speed), and the football game with highlight REPLAY close-up (1× speed):

<video controls width="100%">
  <source src="https://dtl-ai.github.io/hughes-stadium-3d/video/hughes-stadium-demo.mp4" type="video/mp4">
  <source src="https://dtl-ai.github.io/hughes-stadium-3d/video/hughes-stadium-demo.webm" type="video/webm">
  Your browser does not support embedded videos —
  <a href="https://dtl-ai.github.io/hughes-stadium-3d/video/hughes-stadium-demo.mp4">open the demo video</a>.
</video>

[Direct download / open](https://github.com/DTL-AI/hughes-stadium-3d/blob/main/video/hughes-stadium-demo.webm)

## What's inside

### 🏟 Stadium model
- Accurate field geometry: 100-yd playing field, 30-ft end zones, goalposts, **MORGAN** end-zone wordmark and the bear logo
- 8-lane track with Beynon BSS 2000 base + MSU Bears color finish (orange/peach straights, navy turns)
- Four-sided bowl seating, press boxes and a 3D electronic scoreboard
- Day/evening lighting (floodlight towers auto-on for the evening kickoff)

### 🏗 Stadium Construction & Renovation simulation
Eight-phase animated build (May 28 → Oct 17, 2019, $2.5M): demolition and strip-out → grading and sub-base → field trench/irrigation → infield turf → line painting and logo → track base coat → track finish and lane lines → final inspection and handover.
- Animated 3D equipment and crews at every phase
- Gantt chart + phase log synchronized to the animated timeline
- **EVM budget tracking** (PV / EV / AC, SPI, CPI, SV, CV, EAC, VAC) live-updating
- Per-phase stills pulled from the renovation timelapse in the video window
- 1× / 3× / 8× speed controls

### 🏈 Game Day — MSU vs NC A&T (Sat, Nov 9, 2019)
Full 11-on-11 animated simulation of the 195-event game (final: **MSU 22 · NC A&T 16**):
- Live play-by-play feed driven from the official game sheet
- NFL-style kickoff formations and special teams
- Ball locked to the carrier; correct end-zone touchdowns and field goals
- **Broadcast-style REPLAY close-up window** on every MSU score (TD / FG) with a top-down mini-scene
- Confetti + celebration on the scoreboard
- Scorebox, date line, and evening auto-lights

## Run it

No build step. Just open:

```
index.html
```

or serve locally if you prefer:

```
python -m http.server 8000
# → http://localhost:8000
```

Controls: `R` reset view · `V` cycle camera views · 1×/3×/8× speed buttons affect both sims · the two simulations are mutually exclusive (starting one closes the other).

## Files

| Path | Purpose |
|------|---------|
| `index.html` | The whole app (three.js scene + both sims + replays), ~900 KB |
| `vid/phase1-8.png` | One representative still from each renovation phase |

## Build data

Event feed and rosters were extracted from the official MSU Athletics / MPA football game sheet for the **Nov 9, 2019** MSU @ NC A&T game. See `src/` for the extraction scripts and `shot/` in the private workspace for the raw feed/frames used during build.

## License

Project by Dr. Yuhan Jiang (Morgan State University) — 2026. For educational / research use in AEC, BIM and sports visualization.

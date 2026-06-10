# VOID RUNNER

> *"Before you were born, it knew your name."*

A psychological horror endless runner — browser-based, zero dependencies, one file.

![preview](img.)

## Play

Just open `index.html.HTML` in any modern browser. No install, no server, no dependencies.

## Controls

| Input | Action |
|---|---|
| `← / A` | Move left |
| `→ / D` | Move right |
| `↑ / Space` | Jump |
| `↓` | Slide / crawl |
| `P` | Pause |
| `Esc` | Return to menu |
| Swipe | Touch / mobile controls |

## Features

- **3 difficulty modes** — Easy / Normal / Hard (different initial speed and obstacle density)
- **5 obstacle types** — walls, spike traps, swarms, gap formations, double/triple threats
- **Persistent high score** — saved to `localStorage`, survives browser restarts
- **Psychological atmosphere** — whisper messages, shadow entities (standard / tall / crawling), heartbeat line, vignette darkening, screen shake
- **Settings panel** — toggle screen shake, whispers, scanlines, difficulty; clear high score
- **Invincibility frames** — brief immunity after being hit, prevents chain deaths
- **Near-miss detection** — flash indicator when you narrowly dodge an obstacle
- **Pause menu** — `P` to pause, `Esc` to quit to menu
- **Touch support** — swipe left/right/up/down for mobile

## File structure

```
void-runner/
├── index.html    ← entire game, self-contained
├── README.md
└── LICENSE
```

## Customisation

All tuneable values are near the top of the `<script>` block:

```js
const DIFF_PRESETS = {
  easy:   { initSpeed: 3.0, accelRate: 180, spawnBase: 100 },
  normal: { initSpeed: 3.8, accelRate: 150, spawnBase:  80 },
  hard:   { initSpeed: 5.0, accelRate: 100, spawnBase:  60 },
};
```

- `initSpeed` — starting scroll speed
- `accelRate` — frames between each speed increment
- `spawnBase` — base frame interval between obstacle spawns (lower = harder)

Add your own whisper lines to the `WHISPERS` array.
Add your own death messages to the `DEATH_MSGS` array.

## Tech

Pure vanilla HTML + Canvas API. No frameworks, no build step, no external assets.
Works in Chrome, Firefox, Edge, Safari (desktop and mobile).

## License

MIT — do whatever you want with it.

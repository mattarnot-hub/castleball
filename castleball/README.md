# 🏰 Castle Ball — Rules Configurator

> *"Hold the castle. Own the diamond."*

An interactive rules configurator for **Castle Ball** — a new hybrid sport played on a baseball diamond where batters defend a soccer-sized goal net using a tennis racket.

**[→ Play with it live](https://castleball.pages.dev)** *(URL live once deployed to Cloudflare Pages)*

---

## What is Castle Ball?

Castle Ball is played on a standard baseball diamond with one key addition: a **soccer-sized Castle Gate net** installed behind home plate. The batter defends the net with a **tennis racket** while also trying to hit and run bases.

### Core mechanics
- **Pitcher** tries to throw past the batter and score through the Castle Gate
- **Batter** defends the net and hits into play
- **Base runners** can carry rackets and deflect teammate shots within a 6ft zone around each base (into the outfield only)
- **Defense** can smash the ball back through the Gate to end the inning
- **Mixed league**: 50% men / 50% women on the field at all times

### Scoring
| Event | Default Points |
|---|---|
| Score at Home (full circuit) | 1,000 |
| 3rd Base | 80 |
| 2nd Base | 40 |
| 1st Base | 10 |
| Home Run (stands) | 100 |
| No Man's Land hit | 50 |
| Gate Goal (defense) | 50 |

---

## The Configurator

This app lets you toggle every optional rule and adjust every scoring value. The field diagram updates live. You can export a plain-text spec sheet for any variant.

**Configurable:**
- Ball type: Dodgeball Jr. / Pickleball / Tennis / Baseball / Nerf / Golf / Blitzball
- Castle Gate size: Small (4m) / Soccer (7.32m) / XL (10m)
- Defense rackets on/off
- Offense rackets on base on/off
- 6ft deflection zones on/off
- Net smash = inning over on/off
- All scoring values (sliders)
- Mixed league format on/off

**Fixed (immutable):**
- Baseball diamond geometry
- Base distances (90ft)
- Pitcher's mound position (60.5ft)
- Outfield dimensions (LF 415ft · CF 450ft · RF 415ft)

---

## Deploy

This is a single `index.html` file — no build step, no dependencies, no framework.

### Cloudflare Pages (recommended)

1. Fork or clone this repo to your GitHub account
2. Go to [Cloudflare Pages](https://pages.cloudflare.com)
3. Connect your GitHub account → select this repo
4. Build settings: **leave everything blank** (no build command, no output directory)
5. Deploy → you get `yourproject.pages.dev` instantly

Every `git push` to `main` triggers an automatic redeploy.

### Local development

Just open `index.html` in a browser. No server needed.

```bash
open index.html        # macOS
start index.html       # Windows
xdg-open index.html    # Linux
```

---

## File structure

```
castleball/
├── index.html    ← the entire app (self-contained)
├── _headers      ← Cloudflare Pages security headers
└── README.md     ← this file
```

---

## Roadmap

- [ ] Shareable URLs (encode variant config in URL hash)
- [ ] Save/load named variants
- [ ] Printable rulebook PDF export
- [ ] Animated pitch trajectory overlay
- [ ] Team roster builder
- [ ] YouTube broadcast overlay mode

---

*Castle Ball is an original sport concept. All rights reserved.*

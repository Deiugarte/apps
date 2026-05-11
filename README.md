# 📚 Apps Educativas

A suite of interactive educational web apps designed for a 6-year-old child. Built with pure HTML5, CSS3, and Vanilla JS — no frameworks, no build tools, no dependencies. Each app is a single self-contained `.html` file that runs directly in any modern browser, optimized for iPad use.

**Live site:** [GitHub Pages](https://deividugarte.github.io/apps) *(update with your actual URL)*

---

## Apps

### ✍️ Escritura

| App | File | Description |
|-----|------|-------------|
| Caligrafía | `caligrafia.html` | Handwriting practice — trace uppercase letters, lowercase letters, and numbers on an on-screen canvas with adjustable brush size and color |
| Sílabas | `silabas.html` | Syllable learning — explore word divisions, tap syllables in order, count them, and race the clock in a timed challenge |

### 🔢 Matemáticas

| App | File | Description |
|-----|------|-------------|
| Unidades, Decenas y Centenas | `unidades-decenas.html` | Place value visualizer — build numbers 0–999 using unit cubes, ten-bars, and hundred-squares; enter C/D/U digits for a shown number |
| Suma y Resta | `suma-resta.html` | Addition and subtraction 0–20 with visual circle counters; circles get crossed out for subtraction |
| Tablas | `tablas.html` | Multiplication tables for ×2 and ×5 with dot-array visualizations and a timed practice mode |

### 🧩 Juegos y Lógica

| App | File | Description |
|-----|------|-------------|
| Memoria | `memoria.html` | 4×4 card flip memory game with animal emoji pairs; tracks time and number of moves |
| Secuencias | `secuencias.html` | Pattern recognition — complete sequences of shapes, numbers, and emojis with 4-choice answers |

### 🎨 Arte y Ciencias

| App | File | Description |
|-----|------|-------------|
| Colorear | `colorear.html` | Tap-to-color SVG scenes (Sol, Casa, Mariposa, Pez) with a 10-color palette |
| Cuerpo Humano | `cuerpo-humano.html` | Interactive body map — tap any of 17 body parts to learn its name and description; includes a quiz mode |

### 🌍 Idiomas

| App | File | Description |
|-----|------|-------------|
| Inglés | `ingles.html` | English vocabulary across 4 topics (Numbers 1–20, Colors, Animals, Phrases) with Spanish phonetic pronunciations and a mixed challenge mode |

---

## Design System

All apps share a consistent design language:

- **Fonts:** [Nunito](https://fonts.google.com/specimen/Nunito) (UI text) + [Baloo 2](https://fonts.google.com/specimen/Baloo+2) (numbers/display) via Google Fonts
- **Layout:** `#app` flex column at 100vh, fixed 56px top nav, `flex:1` scrollable content area
- **Navigation:** Per-app color theme, tab switching via `style.display`, active tab gets `.active` class; every app has a 🏠 home button
- **On-screen numpad:** Always-visible 3×4 grid; inputs use `inputmode="none" readonly` to prevent the system keyboard from appearing
- **Score chips:** Global ✓/✗ counters in the nav header, updated via `addScore(correct)`
- **Timed challenges:** 60-second countdown with a color-shifting timer bar (green → amber at 30s → red at 15s), streak bonus system (+10 + streak×2 points), result overlay at end
- **Touch optimization:** `touch-action: manipulation`, `-webkit-tap-highlight-color: transparent`, pointer events throughout
- **Viewport:** `maximum-scale=1.0` to prevent accidental zoom on iPad

---

## Tech Stack

- Pure HTML5 + CSS3 + Vanilla JS
- No frameworks, no bundler, no npm
- Single `.html` file per app (styles and scripts inline)
- Hosted on GitHub Pages

---

## Ideas for Future Apps

- **Reloj** — analog clock face, set-the-time exercises
- **Figuras geométricas** — shapes, properties, sorting game
- **Abecedario** — animated letter strokes + tap-to-hear phonics
- **Lectura** — fill-in-the-blank sentences with simple words
- **Los planetas** — solar system overview with fun facts
- **Sopa de letras** — themed 6×6 word search
- **Ahorcado** — hangman with category hints and on-screen keyboard
- **Los alimentos** — food groups drag-and-drop activity

---

## Development

No build step needed. Open any `.html` file directly in a browser, or serve locally:

```bash
# Python
python3 -m http.server 8080

# Node
npx serve .
```

To deploy, push to the `main` branch — GitHub Pages serves automatically from the repo root.

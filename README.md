# Pappus — Generative Art

> A seed-based generative system for fractal tree compositions.  
> A reproducible catalogue of computational branching studies.

---

## What is this?

**Pappus** is a generative design system built on fractal branching. A tree grows from a single seeded point, splitting at each generation into one to eleven sub-branches — each scaled by the golden ratio, each turned by a bounded angle, until the field is filled with an organic, natural form.

Every artwork in this catalogue is defined by a single numeric seed. The same seed always produces the identical composition — making each piece **traceable, reproducible, and licensable** across textile, print, and apparel applications.

Named for the seed-bearing tuft of a flower — the small, feathered structure carried on the wind — **Pappus** reframes branching growth as a textile.

---

## Live

🌐 **[View the catalogue →](https://reyrove.github.io/Pappus/)**

---

## The System

The generator is a single-layer system — a recursive tree whose branches, angles, and colours are all seeded:

| Layer | Description |
|-------|-------------|
| **Ground** | One of 12 pastel background tones, chosen per seed. |
| **Tree** | A recursive branching structure grown from a seeded point, split 1–11 ways per node, 9 levels deep. |

Both layers are driven by the same seed, ensuring deterministic output.

### Parameters

- **Recursion depth** — 9 levels
- **Sub-branches per node** — 1 to 11
- **Length scale per level** — × 0.618 (golden ratio)
- **Width scale per level** — × 0.618
- **Max angle deviation** — 2π/6 (60°)
- **Start position** — seeded within the lower half of the canvas
- **Start angle** — `-11π/20` plus a small seeded deviation
- **Initial length** — `canvas width / 4`
- **Initial width** — `canvas width / 100`
- **Colour assignment** — hair colour for tip branches (depth ≤ 1), body colour for interior branches

---

## Structure

```
Pappus/
├── index.html              ← Full catalogue (single-file)
├── images/
│   ├── fav.svg
│   ├── pappus-tote.png
│   ├── pappus-cushion.png
│   └── ...
├── Pappus.jpg              ← Apparel mockup
└── README.md
```

The entire project is contained in a single `index.html` — no build step, no dependencies, no framework. Open it in any modern browser.

---

## Features

- **Seed-based generation** — every composition is deterministic and reproducible
- **Live catalogue** — cover, statement, plate, surfaces, process, archive, commission sections
- **Multiple surfaces** — print, scarf, textile, wallpaper — all rendered from the same seed
- **Archive of 8 seeds** — click any plate to load it into the main view
- **PNG export** — download any composition directly from the browser
- **Keyboard shortcuts** — `R` for new seed, `S` to save
- **Legal modal** — licensing, terms, and credits built in
- **Responsive** — works on desktop, tablet, and mobile
- **Mobile-first navbar** — horizontally scrollable with fade hint

---

## Usage

### Generate a new composition

Click **New Seed** or press `R`.

### Download the current composition

Click **Download** or press `S`.

### Load a seed from the archive

Click any plate in the **Archive** section.

---

## Color System

Every composition is drawn from three curated palettes, each seeded independently:

**Background — 12 pastel tones**

| Hex | Name |
|-----|------|
| `#FFF8DC` | Cornsilk |
| `#F5DEB3` | Wheat |
| `#F5F5DC` | Beige |
| `#DCDCDC` | Gainsboro |
| `#FFFAFA` | Snow |
| `#E0FFFF` | Light Cyan |
| `#FFE4C4` | Bisque |
| `#FFF0F5` | Lavender Blush |
| `#FFE4E1` | Misty Rose |
| `#DDA0DD` | Plum |
| `#F0F8FF` | Alice Blue |
| `#D5D6EA` | Pastel Light Blue |

**Body — 12 saturated tones**

| Hex | Name |
|-----|------|
| `#A0522D` | Sienna |
| `#556B2F` | Dark Olive Green |
| `#4682B4` | Steel Blue |
| `#8B4513` | Saddle Brown |
| `#800000` | Maroon |
| `#D2691E` | Chocolate |
| `#571B7E` | Purple Iris |
| `#D291BC` | Pastel Violet |
| `#F8B88B` | Pastel Orange |
| `#8B8000` | Dark Yellow |
| `#FFFF33` | Neon Yellow |
| `#6AFB92` | Dragon Green |

**Hair — 12 bright / neutral tones**

| Hex | Name |
|-----|------|
| `#00FA9A` | Medium Spring Green |
| `#5F9EA0` | Cadet Blue |
| `#B0E0E6` | Powder Blue |
| `#F4A460` | Sandy Brown |
| `#C0C0C0` | Silver |
| `#F0FFF0` | Honeydew |
| `#BC8F8F` | Rosy Brown |
| `#16E2F5` | Bright Turquoise |
| `#FDBD01` | Neon Gold |
| `#C04000` | Mahogany |
| `#800517` | Deep Red |
| `#E56E94` | Blush Red |

Because all three axes and the branching itself are seeded, no two compositions share the same rhythm of branch and hue.

---

## Technical Notes

- Pure vanilla JavaScript — no libraries
- Canvas 2D rendering
- Custom xorshift random generator for deterministic seeds
- Device-pixel-ratio aware rendering
- Fully static rendering — one seed produces one composition, no animation loops
- Single `renderStatic()` function drives the cover, plate, framed print, all four surfaces, and all eight archive thumbnails
- Recursive fractal tree with golden-ratio scaling (0.618) at every level
- `prefers-reduced-motion` respected

---

## About

**Pappus** is a project by [Reyhaneh Daneshdoost](https://reyrove.github.io/) — an Iranian-born artist working at the intersection of classical textile logic and generative systems.

The work begins with a simple observation: the woven surface — repetitive, mathematically structured, infinitely variable — has always been a form of computation, long before computers.

**Pappus** is an attempt to render that logic visible.

> *A tree is a single stroke that remembers every branch it has ever grown.*

---

## Licensing

All compositions are seed-documented and available for licensing across textile, surface, and apparel applications.

For commercial use, custom editions, or exclusive rights:

📧 **reyhanehdaneshdoost@gmail.com**

See the **Licensing** section in the live catalogue for details.

---

## Links

- 🌐 [Website](https://reyrove.github.io/)
- 📷 [Instagram](https://www.instagram.com/rey._.rove/)
- 💼 [LinkedIn](https://www.linkedin.com/in/reyhaneh-daneshdoost-730481160/)
- 🐦 [X](https://x.com/reyrove)

---

## Credits

**Design & Generative System**  
Reyhaneh Daneshdoost

**Typefaces**  
Cormorant Garamond · DM Mono

**Edition**  
Pappus — Autumn 2026

---

<p align="center">
  <em>Generative Fractal Tree</em><br />
  <sub>© Reyrove Studio · All compositions reproducible by seed</sub>
</p>
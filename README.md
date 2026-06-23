# Storia dell'Arte 1400–1800

**Timeline interattiva e flashcard game per lo studio della storia dell'arte italiana dal Primo Rinascimento al Neoclassicismo.**

![Preview](storia_arte_1400_1800.html)

---

## Scope

A comprehensive study companion for Italian art history exams covering the period 1400–1800. Includes **159 artworks** by **46 artists** across **9 periods**:

| Period | Works |
|--------|-------|
| Primo Rinascimento (1400–1490) | 45 |
| Verso il Rinascimento Maturo (1450–1520) | 16 |
| Rinascimento Maturo (1490–1520) | 31 |
| Alto Rinascimento / Manierismo (1490–1576) | 5 |
| Manierismo (1520–1580) | 16 |
| Scuola Veneta (1540–1600) | 6 |
| Barocco (1580–1680) | 20 |
| Rococò e Settecento (1700–1780) | 10 |
| Neoclassicismo (1770–1800) | 10 |

Each artwork entry includes: title, artist, date, type (painting/sculpture/architecture), description, and location.

### Features

- **Timeline View** — Expandable accordion sections organized by period, with artist cards and artwork thumbnails
- **Flashcard Game** ("Gioca") — 9 levels (one per period), flip-card mechanics with progress tracking via localStorage
- **Visual Design** — Warm sophisticated palette with period-specific accent colors, hover effects, and responsive layout
- **Image-First** — Every artwork has a corresponding image, shown inline in the timeline and as the front of each flashcard

---

## Design

### Color System

Each of the 9 periods has a dedicated accent color used for section headers, progress badges, and game UI:

- Primo Rinascimento — #C8922C (gold)
- Verso il Rinascimento Maturo — #D4894A (amber)
- Rinascimento Maturo — #C0392B (crimson)
- Alto Rinascimento / Manierismo — #8E44AD (purple)
- Manierismo — #6C3483 (deep purple)
- Scuola Veneta — #00897B (teal)
- Barocco — #2E7D32 (green)
- Rococò e Settecento — #1E6B9E (blue)
- Neoclassicismo — #5D6D7E (slate)

### Aesthetic

- Warm off-white background (#f6f4ef)
- Inter font throughout
- Card-based layout with soft shadows and rounded corners (16px)
- Smooth CSS transitions (450ms cubic-bezier)
- Color-coded period dots with glow halos
- Sticky top navigation bar
- Hero section with gold accent and gradient divider
- Fully responsive (adapts to mobile and print)

---

## Dev Stack

### Pure frontend — zero build tools, zero dependencies, zero frameworks

| Layer | Technology |
|-------|-----------|
| **Markup** | HTML5 |
| **Styling** | CSS3 (custom properties, grid, flexbox, transitions) |
| **Logic** | Vanilla JavaScript (no libraries, no frameworks) |
| **Fonts** | Google Fonts — Inter (400–900) |
| **Icons** | Unicode characters (no icon library) |
| **Persistence** | localStorage for game progress |
| **Image assets** | 159 JPEG files, self-hosted in repo |

### Rationale

The entire application is a **single self-contained HTML file** with zero external runtime dependencies. This was a deliberate choice:

1. **Portability** — Open locally from any filesystem, no server needed
2. **Deploy anywhere** — Static file hosts (Vercel, Netlify, GitHub Pages, S3)
3. **Offline-capable** — Once loaded, all images and data are local
4. **Exam-ready** — No build step, no node_modules, no complexity
5. **Print-friendly** — CSS @media print rules strip interactive elements

### File Structure

```
storia-arte-repo/
├── storia_arte_1400_1800.html   ← Single-page application (181KB)
├── ARTWORKS_1400_1800/          ← 159 artwork images
│   ├── BRUNELLESCHI/
│   ├── DONATELLO/
│   ├── LEONARDO_DA_VINCI/
│   ├── MICHELANGELO_BUONARROTI/
│   ├── CARAVAGGIO/
│   ├── BERNINI/
│   └── ... (40 more artist folders)
├── vercel.json                  ← Vercel deployment config
├── .gitignore
└── README.md
```

---

## Deployment

The project is Vercel-ready. Connect the GitHub repo and Vercel will auto-detect `vercel.json`. No build command required — the HTML file is served as-is with all routes rewritten to `storia_arte_1400_1800.html`.

Or deploy anywhere that serves static files: GitHub Pages, Netlify, Cloudflare Pages, or just open the HTML file locally.

---

## Credits

All artwork data, descriptions, and image collection curated for university-level art history study. 46 artists, 159 works, 300 years of Italian art.

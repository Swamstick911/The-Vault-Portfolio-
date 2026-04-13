# 🎹 Portfolio — Swastik Bajpai

> A cinematic dark-mode portfolio built around the **"Keys"** theme — where every project is a keycap on a custom mechanical keyboard. Designed in Figma, built with Astro, animated with GSAP.

***

## ✨ Concept

The portfolio identity is built around the **Forxa mechanical keyboard** — a keyboard designed and engineered from scratch (PCB, switches, CAD). Each project is presented as a keycap: hover to press it down, click to explore. The hero features an isometric render of the Forxa board with the builder's name set in large serif type.

**Core feel:** Cinematic. Theatrical. Dark. Not too minimal, not too loud — the sweet spot.

***

## 🛠 Tech Stack

| Layer | Tool |
|---|---|
| Framework | [Astro](https://astro.build) |
| Styling | [Tailwind CSS v4](https://tailwindcss.com) |
| Animations | [GSAP](https://gsap.com) + ScrollTrigger |
| 3D / Hero | Three.js (optional, hero particle/glow) |
| Fonts | Instrument Serif (display) · General Sans (body) |
| Deployment | [Vercel](https://vercel.com) |

***

## 🎨 Design System

### Color Palette

| Token | Hex | Usage |
|---|---|---|
| `bg` | `#0e0f13` | Page background |
| `surface` | `#161820` | Section backgrounds |
| `surface-2` | `#1e2028` | Cards, keycap backs |
| `keycap-cream` | `#e8e0d0` | Keycap legends, headlines |
| `keycap-shadow` | `#c4bbaa` | Keycap side faces (3D depth) |
| `accent-red` | `#e03c31` | Enter key, CTAs, active states |
| `text-muted` | `#7a7d8a` | Subtitles, metadata |
| `text-faint` | `#3e4050` | Dividers, placeholders |

### Typography

- **Display:** `Instrument Serif` — name, section titles, keycap legends
- **Body:** `General Sans` — all body copy, UI elements

***

## 📁 Project Structure

```
portfolio/
├── public/
│   └── assets/
│       ├── forxa-render.png       ← Forxa keyboard isometric render
│       └── noise.png              ← Noise texture overlay (4% opacity)
├── src/
│   ├── components/
│   │   ├── Navbar.astro
│   │   ├── Hero.astro
│   │   ├── KeycapCard.astro       ← Reusable project keycap component
│   │   ├── ProjectsGrid.astro
│   │   ├── About.astro
│   │   └── Contact.astro
│   ├── layouts/
│   │   └── BaseLayout.astro
│   ├── pages/
│   │   └── index.astro
│   └── styles/
│       ├── base.css               ← Reset + design tokens
│       └── global.css             ← Typography, utilities
├── astro.config.mjs
├── tailwind.config.mjs
└── package.json
```

***

## 🎹 The Keycap Card

The signature component. Every project = a keycap on the board.

```
┌──────────────────┐  ← top face (#e8e0d0, 12px radius)
│                  │
│  Project Name ↗  │  ← legend (Instrument Serif, dark)
│  Short tagline   │  ← sublabel (General Sans, small)
│                  │
└──────────────────┘
  ████████████████   ← side face (#c4bbaa, 8px tall) — creates 3D depth
```

**Hover interaction (GSAP):** Side face disappears, top face shifts down `8px` — the key presses in.

### Keyboard Grid Layout

Projects are arranged like real keycap rows — irregular widths based on project scope:

```
[ GazePilot ——— 2u ]  [ Forxa — 1u ]  [ Shelby OS — 1u ]

[ LifeSync — 1.5u ]   [ Attendance — 1.5u ]  [ AgentPilot — 1u ]
```

***

## 🚀 Sections

| Section | Description |
|---|---|
| **Hero** | Forxa keyboard render · serif name · tagline · CTA |
| **About** | Bio · hardware + software dual identity |
| **Projects** | Keycap grid — all featured projects |
| **Stack** | Tech I build with |
| **Contact** | Email · GitHub · Hack Club |

***

## ⚡ Getting Started

```bash
# Clone the repo
git clone https://github.com/swastikbajpai/portfolio
cd portfolio

# Install dependencies
npm install

# Start dev server
npm run dev

# Build for production
npm run build
```

***

## 🎞 Animation Plan (GSAP)

| Moment | Animation |
|---|---|
| Page load | Keyboard assembles key by key → last key placed spells your name |
| Hero text | SplitText reveal — characters drop in staggered |
| Scroll reveal | `clip-path` wipe per section, triggered by ScrollTrigger |
| Keycap hover | Key press — top face translates Y+8px, side face fades |
| Project click | Card expands with smooth clip-path transition |

***

## 📌 Roadmap

- [x] Figma design — Hero, About, Projects, Contact
- [ ] Astro project setup + Tailwind config
- [ ] Base layout + design tokens in CSS
- [ ] Hero section with keyboard render
- [ ] KeycapCard component + grid layout
- [ ] GSAP animations (load sequence + scroll reveals)
- [ ] Keycap press interaction
- [ ] Mobile responsive pass
- [ ] Replace placeholder keyboard with Forxa render (on completion)
- [ ] Deploy to Vercel

***

## 🔗 Related Projects

- **[Forxa](https://github.com/swastikbajpai/forxa)** — The mechanical keyboard this portfolio is built around. Full PCB design, custom switches, CAD in OnShape, layout in KiCAD.
- **[GazePilot](https://github.com/swastikbajpai/gazepilot)** — AI-powered eye tracking and gesture control system.
- **[Shelby OS](https://github.com/swastikbajpai/shelby)** — Desk companion firmware for Hack Club Sprig Console.

***

## 📄 License

MIT — feel free to take inspiration, but make it your own.

***

*Built by Swastik Bajpai · Kanpur, India*

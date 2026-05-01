# The Vault (Portfolio)

My personal portfolio, built with Astro, designed around PCB/circuit board theme. Designed it in Figma, and animated it using GSAP.

live at: https://the-vault-portfolio.vercel.app/

---
## What's inside?

- **Home** - Hero section with animated circuit traces running
- **About** - a bit about me, what I build and what I am into
- **Works** - some projects displayed as a mechanical keyboard grid and a hackatime stats card. (A PCB trace tree too!!)
- **Contact** - Email and Github Link, not complexing it
- **Footer** - a small one
---

## Tech Stack:

- [Astro](https://astro.build) - site framework
- GSAP - all the animation (trace pulsing, dots, keycap press effect)
- Vanilla CSS - nothing just simple clean CSS
- SVG - hand-drawn circuit traces, pads and the PCB tree

---

## The Design
The whole thing is built around a PCB theme, the main color was #0ea5c9 (electric blue) for traces and animation on a near-black background. The animated dots that travel along the traces are the main visual motif, showing up in every section.

Projects are displayed as mechanical keycaps that physically press down on hover. The SVG tree in the Works section is made entirely of `<polyline>` elements with pads at branch tips.

---

## Runnin Locally

```bash
npm install
npm run dev
```

open `http://localhost:4321` and you're good to go.

---

## Projects Featured

| Project | What it is |
|---|---|
| **Forxa** | Custom 68-key mechanical keeb, PCB, switches and case designed from scratch |
| **Shelby OS** | desk companion firmware for Hack Club Sprig (clock, github, etc) |
| **GazePilot** | control your PC with your hands gestures |
| **Grindline** | comeback planner for students- pomodoro, XP, tasks, streaks |

---

## Project Structure

```
src/
├── components/
│ ├── Navbar.astro
│ ├── Hero.astro
│ ├── About.astro
│ ├── Works.astro
│ ├── Contact.astro
│ └── Footer.astro
├── layouts/
│ └── Layout.astro
└── pages/
└── index.astro
```
---

Built By [Swastik Bajpai](https://github.com/Swamstick911)
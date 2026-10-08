# Naman Garg - First-Year B.Tech CSE Interactive 3D Portfolio

An ultra-premium, dark-aesthetic personal portfolio website engineered for **Naman Garg**, first-year B.Tech Computer Science and Engineering student at **JECRC University, Jaipur**.

Built with modern UI/UX design standards: interactive 3D face avatar with mouse parallax and continuous nod/float animation, a "Design Trends" 3D orbiting software bracelet centerpiece around an open hand, a structured 400-word flowing engineering skills statement, an interactive hardware logic mini-lab, and direct contact integration.

---

## ✨ Centerpiece Highlights & Architecture

### 1. "HI, I'M NAMAN" 3D Avatar Hero Section
- **Giant Headline**: Bold wide grotesque typography (`Archivo Black`) with a vertical gradient (`#d9d9d9` to `#ffffff`) spanning the viewport.
- **Overlapping 3D Face Cutout**:
  - Uses the authentic portrait cutout from the user's image with feathered alpha transparency.
  - Sits directly in front of the giant headline, overlapping the middle letters by ~40%.
  - **Animation Loop**: Continuous subtle 3D nodding (`rotateX` 0°–6° and `translateY` 0–6px), natural sway (`rotateZ` ~1.5°), and gentle floating bob.
  - **Interactive Cursor Parallax**: Tracks cursor movement across the viewport with smooth lerp interpolation, rotating the head up to ±8° along X and Y axes.
  - **Accessibility**: Full compliance with `prefers-reduced-motion` to smoothly disable transforms for users who prefer reduced motion.
- **Top Navigation**: Spread-out uppercase links (`ABOUT`, `CUSTOMERS`, `PROJECTS`, `CONTACT`) with animated hover underline.
- **Pill CTA Button**: Dark pill with a multi-stop gradient border (`#7b2ff7` &rarr; `#ff2bb1` &rarr; `#ff8a3d`) and ambient glowing hover lift.

### 2. "DESIGN TRENDS" 3D Orbiting Software Ring Poster
- **Poster Aesthetic**: Centered 4:5 aspect ratio card on desktop with deep red corner radial glows (`#b30000` to transparent) and an authentic 8% film grain overlay.
- **Headline**: Condensed bold uppercase sans-serif (`Anton` / `Bebas Neue` style) reading `CORE SKILLS` with dual vertical gradients (white-to-pink and pink-to-red).
- **Tilted Pill Badge**: Bold white `"SOFTWARE"` on vivid red, rotated -8° over the headline edge.
- **Centerpiece Hand**:
  - Open-palm hand with dramatic red rim lighting and a gentle 6px floating bob.
- **3D Orbiting Bracelet**:
  - 5 glossy 3D glass/chrome rounded-square tiles: **Claude**, **Visual Studio**, **Git**, **MS Office**, and **AutoCAD**.
  - True 3D orbit (perspective 1200px) continuously rotating every 35 seconds.
  - Counter-rotation: Each tile's face always points toward the viewer.
  - Depth ordering: Tiles behind the hand are dimmed (`opacity: 0.35–0.7`) and blurred (`z-index: 10–19`), while front tiles are crisp, illuminated, and elevated (`z-index: 30–39`).
  - Interactive pause on hover and right arrow navigation button to advance the orbit.
  - Synchronized bottom pagination dots and `@naman_cse` badge.

### 3. Professional Engineering Narrative & Skills Matrix (~325 Words)
- A flowing, articulate curriculum statement strictly under the 400-word limit.
- **Technical & Coding Skills**: Procedural Programming, Memory Management in C, Scripting & Automation in Python, Hardware Fundamentals.
- **Analytical & Mathematical Skills**: Algorithmic Thinking, Calculus & Linear Algebra, Scientific Analysis.
- **Professional & Tools Skills**: Technical Communication, Engineering Drawing / CAD, Basic IT Literacy.
- **Interactive Hardware Logic Mini-Lab**: Live boolean gate simulator (AND, OR, XOR, NAND) with interactive toggle switches and real-time illuminated diode output.

### 4. Academic Showcase & Contact Hub
- Academic journey at **JECRC University, Jaipur**.
- Direct email (`namangarg0700@gmail.com`) with one-click copy toast notification.
- Client-side validated contact form simulation.

---

## 🚀 How to Run Locally

Because the project is built with clean, zero-dependency static web standards, no compilation or `npm install` is required!

### Option 1: Direct Double-Click
Simply open `index.html` in any web browser (Chrome, Edge, Firefox, Safari).

### Option 2: Local Python Server (Recommended)
Open PowerShell or your terminal in this directory and run:

```bash
python -m http.server 8000
```

Then open:
```
http://localhost:8000
```

---

## 🛠️ Project File Structure

```
naman-portfolio/
├── index.html                   # Zero-dependency, standalone production website
├── README.md                    # Documentation & guide
├── assets/
│   ├── css/
│   │   └── style.css            # 3D transforms, keyframe loops, glassmorphism, grain
│   ├── images/
│   │   ├── avatar-face-neutral.png # Transparent head cutout from user image
│   │   └── hand-cutout.png         # Attached hand cutout with red rim light
│   └── js/
│       ├── canvas.js            # Interactive particle network background
│       └── main.js              # 3D head parallax, 3D orbit engine, logic mini-lab
└── src/
    ├── App.jsx                  # Main React orchestrator
    ├── config/
    │   └── portfolioConfig.js   # Single source of truth (name, skills, tiles, links)
    └── components/
        ├── HeroSection.jsx      # "HI, I'M NAMAN" with 3D face & cursor tracking
        ├── OrbitSkillsHero.jsx  # "DESIGN TRENDS" 3D orbiting software ring poster
        ├── SkillsMatrix.jsx     # 400-word narrative & interactive logic lab
        ├── AboutSection.jsx     # Academic journey & JECRC University
        └── ContactSection.jsx   # Contact hub & copy toast
```

---

© 2026 Naman Garg &bull; JECRC University, Jaipur

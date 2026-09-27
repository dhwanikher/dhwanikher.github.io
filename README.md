# Dhwani Kherawat — Personal Portfolio Website

A personal portfolio website built for **Builders Day** in **WebDev 101 (Group C)** at Scaler School of Technology.

- 🌐 **Live Website**: [https://dhwanikher.github.io](https://dhwanikher.github.io)
- 📦 **GitHub Repository**: [https://github.com/dhwanikher/dhwanikher.github.io](https://github.com/dhwanikher/dhwanikher.github.io)

---

## 👨‍💻 About Me

I am a Computer Science undergraduate student at **Scaler School of Technology** in Bengaluru, with my degree awarded by **BITS Pilani** (Class of 2026–2029).

My primary focus is engineering robust systems and frontend web applications where resilience, concurrency, and accessibility meet. I specialize in building parts of a system that only fail under subtle conditions nobody arranges on purpose — a crash mid-write, two clients modifying the same record, or an engineering drawing symbol that arrives as the wrong character.

---

## 🛠️ Technologies Used

- **HTML5**: Semantic document structuring (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<figure>`, `<figcaption>`, `<aside>`, `<footer>`, `<form>`, `<label>`, `<input>`, `<textarea>`, `<button>`).
- **CSS3**:
  - **Layout Engines**: CSS Flexbox and CSS Grid (Bento grid, project inspection cards, responsive split layouts).
  - **Box Model**: Strict box-sizing calculations, consistent padding, margins, borders, and rounded corners.
  - **Design System**: CSS Custom Properties (`:root` variables) for both light and dark mode support with automatic `prefers-color-scheme` adaptation.
  - **Interactivity**: Pure CSS transitions (`transform`, `box-shadow`, `border-color`), hover states, and keyframe animations (`pulse-status`).
  - **Responsive Design**: Mobile-first media queries supporting Mobile (<680px), Tablet (680px–960px), and Desktop (>960px).
  - **Print Optimization**: Dedicated `@media print` stylesheet for clean resume/portfolio printing.
- **Zero JavaScript**: Completed entirely using pure HTML and CSS as specified by the Builders Day guidelines.

---

## 🚀 Featured Projects

### 1. Kin — Shared Medication Schedule for Family Caregivers
- **Technologies**: React, Node.js, MongoDB, WebSockets, Vitest
- **Description**: Real-time care coordination web application built so two family members caring for the same relative never give the same dose twice. Every client watching a care circle updates over a WebSocket the moment a dose is logged. When two requests land simultaneously, an atomic `findOneAndUpdate` ensures exactly one write wins.
- **Verification**: Swapping the atomic update for a naive read-then-write fails concurrency race tests; restoring it cleanly passes both tests.
- **Link**: [https://github.com/dhwanikher/kin](https://github.com/dhwanikher/kin)

### 2. balloon — Engineering Drawing to Inspection Sheet Generator
- **Technologies**: Go, pdf.js, AS9102 / GD&T, Regex
- **Description**: Automatically parses toleranced dimensions from engineering drawing PDFs and generates numbered First Article Inspection (FAI) sheets. Recovers corrupted diameter symbols and stitches baseline text runs.
- **Verification**: Standalone Go binary with vendored pdf.js — runs 100% offline with zero network calls, protecting proprietary engineering IP.
- **Link**: [https://github.com/dhwanikher/balloon](https://github.com/dhwanikher/balloon)

### 3. stow — Embedded Key-Value Store Tested by Simulated Power Loss
- **Technologies**: Go, Write-Ahead Log (WAL), Memtable, VFS Crash Injection
- **Description**: An embedded key-value store in Go tested by simulating power cuts at every single durability-relevant operation. Models 43 crash points with clean crashes and torn-write variants (~170 recovery scenarios verified per test run).
- **Verification**: Strict durability contract verification holding the engine to zero data loss after atomic syncs.
- **Link**: [https://github.com/dhwanikher/stow](https://github.com/dhwanikher/stow)

### 4. WebDev Component Lab & Design System
- **Technologies**: HTML5 Semantic Elements, CSS3 Flexbox & Grid, CSS Keyframes, CSS Variables
- **Description**: Pure HTML & CSS interactive portfolio and design system demonstrating modern web standards, editorial typography, translucent sticky navigation, responsive bento grids, and accessible forms without client-side JavaScript.
- **Link**: [https://github.com/dhwanikher/dhwanikher.github.io](https://github.com/dhwanikher/dhwanikher.github.io)

---

## 📁 Project Structure

```text
dhwanikher.github.io/
│
├── index.html              # Main semantic HTML5 webpage
├── style.css               # Complete external stylesheet (responsive, animations, tokens)
├── resume.pdf              # Downloadable resume document
│
├── images/                 # Optimized image assets
│   ├── kin-preview.jpg     # Project 1 screenshot
│   ├── balloon-preview.jpg # Project 2 screenshot
│   ├── stow-preview.svg    # Project 3 architecture diagram (SVG)
│   └── webdev-preview.svg  # Project 4 layout diagram (SVG)
│
└── README.md               # Project documentation and submission details
```

---

## 🎯 Concepts Demonstrated & TA Review Guide

When evaluating this portfolio during Builders Day review, the following key concepts can be verified:

1. **Semantic HTML**: Proper landmarks (`<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<figure>`, `<footer>`) used across the entire page for accessibility and SEO.
2. **Where Flexbox is used**:
   - Navigation bar (`.navbar`): Space-between alignment, centered links, and CTA button grouping.
   - Hero buttons and social links: Wrapping flex layout with gap spacing.
   - Card headers, badges, and status pills: Centered icon and text alignment with `gap`.
   - Footer: Responsive flex wrap layout.
3. **Where CSS Grid is used**:
   - Hero section (`.hero-grid`): Split layout between copy and interactive terminal card.
   - Skills section (`.skills-bento`): 3-column bento grid with 2-column spans (`grid-column: span 2`).
   - Project cards (`.project-card`): Asymmetric 2-column inspection ticket layout with alternating visual figure positions.
   - Contact layout (`.contact-grid`): Split grid separating contact details from the interactive form.
4. **CSS Transitions & Hover States**:
   - Card elevation on hover (`transform: translateY(-4px)` with enhanced shadow).
   - Navigation link animated underline using `::after` pseudo-element and `transition: width`.
   - Skill chips background and border color shifts.
5. **CSS Animations**:
   - `@keyframes pulse-status`: Smooth glowing breathing effect on the "Available for Summer 2026 Internships" status indicator dot.
6. **Responsive Design**:
   - Fluid typography with `clamp()`.
   - Media queries at `960px` and `680px` adjusting grid columns, padding, and navigation stacking for mobile screens.
7. **Box Model Discipline**:
   - Global `box-sizing: border-box` to avoid layout overflow.
   - Consistent padding, margins, and borders aligned with design tokens.

---

## 👤 Author

**Dhwani Kherawat**  
- Email: [dhwanikherawat@gmail.com](mailto:dhwanikherawat@gmail.com)  
- GitHub: [@dhwanikher](https://github.com/dhwanikher)  
- LinkedIn: [dhwani-kherawat](https://www.linkedin.com/in/dhwani-kherawat-720461418/)  
- Institution: Scaler School of Technology (BITS Pilani), Bengaluru, India

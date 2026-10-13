# Project Handoff: Architectural Poster Generator Web App

## 1. Project Goal
Develop a web application that programmatically generates design variations of an iconic late-1970s / 1980s architectural exhibition poster (reference: *Columbia University Graduate School of Architecture and Planning - Master of Science in Historic Preservation*)[cite: 1].

---

## 2. Completed Milestones

1. **Typographic & Historical DNA Analysis:**
   * Style identified: Late Modernist Swiss / Weingartian New Wave hybrid[cite: 1].
   * Type family class: High x-height, zero-contrast neo-grotesque sans-serif (Inter, Instrument Sans, Cabinet Grotesk)[cite: 1].
   * Hierarchy scales established: Primary vertical anchor (`~5x`), secondary horizontal hook (`~3x`), and 3-column academic body grid (`1x`)[cite: 1].

2. **Structural Breakdown & Natural Language Specification:**
   * Full stream-of-consciousness architectural analysis covering grid collision (rational 3-column base vs. asymmetric upper field), spatial tension, tactile paper/drafting marks, and emotional tone[cite: 1].

3. **Core Prototype Code:**
   * Fully responsive HTML/CSS blueprint built implementing the `1:2` canvas, `vertical-rl` text orientation, CSS `clip-path` wave separator, registration notch accents, and CSS grid columns[cite: 1].

4. **Design Rules Extracted:**
   * Consolidated mathematical constraints, color restrictions, and typographic scales committed to `skills.md`.

---

## 3. Current Architecture & Tech Choices
* **Core Font:** Inter (via Google Fonts) or Instrument Sans.
* **Layout Engine:** Standard CSS Grid & Flexbox, hardware-accelerated CSS `clip-path` for organic breaks, `writing-mode: vertical-rl` for vertical text running rails[cite: 1].
* **Color Logic:** Monochromatic ink + 1 swappable institutional pastel spot tone (sage, slate, terracotta, ochre)[cite: 1].

---

## 4. Immediate Next Steps for the Next Session

* [ ] **Generator Controls UI:** Build a front-end control panel (sliders/inputs) for:
  * Poster headline inputs (H1, H2, 3-column body content).
  * Spot color picker (locking strictly to historical tint presets).
  * Custom image uploader with automatic CSS grayscale and contrast filtering[cite: 1].
* [ ] **Variation Engine:** Implement procedural randomized layout shifts:
  * Alternating between wave, geometric wedge, or stepped transition dividers.
  * Toggling registration marks and film cadence lines (top vs. bottom vs. side placements)[cite: 1].
  * Shifting image square position across column tracks 3 through 12[cite: 1].
* [ ] **Export Pipeline:** Integrate client-side export to high-res SVG or print-ready PDF/PNG (via `html-to-image` or canvas rasterization).
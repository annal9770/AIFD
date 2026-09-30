# Architectural Poster Design System: Rules, Grid & Typographic Engine

This document defines the mathematical foundations, layout constraints, and styling logic for automated poster generation based on late-modernist/early New Wave architectural exhibition posters.

---

## 1. Canvas Dimensions & Aspect Ratio

* **Aspect Ratio:** Strictly `1:2` (tall vertical format)[cite: 1].
* **Base Virtual Grid:** 12-column fluid grid system across all layouts[cite: 1].
* **Canvas Reference Units:** Default digital render canvas: `600px × 1200px` (or standard print proportion `12" × 24"` / `50cm × 100cm`).

---

## 2. Color System & Rules

* **Rule 1 (Palette Cap):** Strictly 3 colors total: Base Background, Deep Carbon Ink, and exactly ONE Spot Tint[cite: 1].
* **Background:** High-key neutral `#FFFFFF` (or unbleached archival warm white `#FBFBF9`).
* **Primary Ink:** `#111111` to `#1C1C1C` (Carbon black, high contrast against background)[cite: 1].
* **Muted Spot Patina (Single Accent per poster variation):**
  * Sage/Copper Patina: `#B5C7BC`[cite: 1]
  * Slate Blue: `#9BB0BC`
  * Drafting Ochre: `#D8C29D`
  * Industrial Terracotta: `#C69D8E`
* **Forbidden:** Multi-color accents, saturated primary hues, gradients, or soft drop shadows.

---

## 3. Typographic Scale & Ratios

Base Unit: $1.0\text{rem} = 10\text{px}$ (at $600\text{px}$ canvas width).

* **Display 1 (H1 Anchor — Rotated 90° CCW):**
  * Scale: `4.8x – 5.2x` body base (~`48px – 52px`)[cite: 1].
  * Weight: `800` (Extra Bold / Heavy)[cite: 1].
  * Leading: `0.95em – 1.0em` (Solid leading, no loose vertical spacing)[cite: 1].
  * Tracking: `-0.035em` (Tight, locked word bounding box)[cite: 1].
  * Orientation: `writing-mode: vertical-rl; transform: rotate(180deg);`[cite: 1]
* **Display 2 (H2 Hook — Horizontal):**
  * Scale: `2.8x – 3.2x` body base (~`28px – 32px`)[cite: 1].
  * Weight: `700` (Bold)[cite: 1].
  * Leading: `1.05em – 1.1em`[cite: 1].
  * Tracking: `-0.025em`.
* **Body / Footnotes (3-Column Text Grid):**
  * Scale: `1.0x` base (~`9.5px – 10.5px`)[cite: 1].
  * Weight: `400` (Book / Regular) with `700` headers[cite: 1].
  * Leading: `1.35em – 1.4em` (Open, legible, Swiss functionalist spacing)[cite: 1].
  * Tracking: `-0.005em`.

---

## 4. Grid Math & Structural Rhythm

### Upper Section (Asymmetric Field)
* **Horizontal Split:**
  * Left Vertical Rail (Columns 1–3, ~`24%` width): Reserved for vertical H1 text anchor and baseline alignment[cite: 1].
  * Primary Visual Canvas (Columns 4–12, ~`76%` width): Houses the square image, layered stepped shapes, and H2 text[cite: 1].
* **Image Proportion:** Square `1:1` aspect ratio, monochrome/grayscale, placed offset to the right edge with a small margin[cite: 1].
* **Stepped Backdrop Plane:** A rectilinear color-block layer that partially underlaps the image and bleeds into the left rail[cite: 1].

### Intermediate Transition Section (Organic Break)
* **Wave Height:** ~`10% – 12%` of total canvas height[cite: 1].
* **Clip-Path/Vector Geometry:** Asymmetric curve/ellipse bridging the upper visual canvas and lower body grid[cite: 1].
* **Unit Punch Marks:**
  * Left Edge: Circular punch-outs (`2x` circles, diameter ~`32px`, one solid punch white, one ghost tint)[cite: 1].
  * Right Edge: Three stacked horizontal knockout rules (`width: 60px–80px`, `height: 2px–3px`, `gap: 8px`)[cite: 1].

### Lower Section (Modular Information Grid)
* **Columns:** Strictly 3 equal columns (`1fr 1fr 1fr`), separated by `20px` gutters[cite: 1].
* **Alignment:** Flush-left / ragged-right or crisp architectural justification[cite: 1].

### Peripheral Architectural Registration Elements
* **Top-Left Margin:** Solid black unit bar with 3–4 vertical calibration tick knockouts[cite: 1].
* **Top-Right Margin:** Bleed indicator bar (`10px–14px` wide, extending downward)[cite: 1].
* **Bottom-Left Margin:** Solid baseline weight tab anchored to grid column lines[cite: 1].
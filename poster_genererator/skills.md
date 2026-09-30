# Architectural Poster Design System: Rules, Grid & Typographic Engine

This document defines the mathematical foundations, layout constraints, and styling logic for automated poster generation based on late-modernist/early New Wave architectural exhibition posters[cite: 1].

---

## 1. Canvas Dimensions & Aspect Ratio

* **Aspect Ratio:** Strictly `1:2` (tall vertical format)[cite: 1].
* **Base Virtual Grid:** 6-column modular grid across the canvas with uniform column widths and gutters[cite: 1].
* **Canvas Reference Units:** Default digital render canvas: `600px × 1200px` (or standard print proportion `12" × 24"` / `50cm × 100cm`).
* **Outer Margins:**
  * Top / Left / Right margins: Fluid architectural margins (~`20px–30px`)[cite: 1].
  * Bottom Margin: **Strictly reserved** (`~90px–110px` at 1200px height); body text must never bleed to or touch the bottom edge[cite: 1].

---

## 2. Strict Datum Alignment Invariant (The Primary Vertical Axis)

* **Single Common Baseline Axis (Column Line 3 / ~33.33% X-offset):**
  * The **left edge of the photographic image**, the **left edge of the H2 title block** ("Master of Science..."), and the **left edge of the bottom informational body text field** MUST all share the exact same rigid vertical alignment axis[cite: 1].
  * None of these three elements may deviate, indent, or float offset from one another; they anchor flush against the primary vertical boundary separating the left running rail from the content field[cite: 1].

---

## 3. Lower Section: Strict Uniform Columns & Spatial Clearance

* **Macro Grid Division (6 Equal Columns):**
  * The canvas is divided into **6 identical column tracks of equal width and equal gap/gutter** across the full width[cite: 1].
  * **Columns 1–2 (Left 2 Columns):** Entirely vacant negative white space below the wave, preserving the vertical breathing corridor beneath the rotated H1 rail[cite: 1].
  * **Active Text Field (Columns 3–6):** Informational copy populates the remaining 4 columns[cite: 1].
* **Equal Width & Spacing Rule:**
  * All active text columns within the grid must have **identical widths** (`width: 100%` of their respective grid track) and **identical column gutters** (`column-gap`)[cite: 1].
  * Individual columns must not be arbitrarily compressed to fractional percentages (e.g., no 50% or 60% widths inside the track)[cite: 1].
  * Text blocks flow naturally into uniform column lanes across Columns 3, 4, 5, and 6[cite: 1].
* **Vertical Grounding & Margin Reservation:**
  * The body copy terminates well above the bottom border, leaving an uncluttered negative space band before the baseline registration tab[cite: 1].

---

## 4. Wave Transition & Cutout Clearance Rules

* **Vertical Layer Clearance (Zero Overlap with Text):**
  * All decorative graphic cutouts—including the circular punch elements and the horizontal knock-out rules—must be strictly self-contained within the boundary of the green wave form[cite: 1].
  * The lower perimeter of the wave and its punch cutouts must terminate with clear vertical clearance above the body text block[cite: 1].
  * Under no circumstances may punch circles, tints, or wave forms extend downward into or overlay the body typography[cite: 1].
* **Integrated Knockouts Geometry:**
  * Left Flank: 2 circular punch-outs (one opaque white knockout, one ghosted translucent) contained fully within the upper crest of the wave[cite: 1].
  * Right Flank: 3 thin horizontal white rules cut cleanly into the upper right flank of the form[cite: 1].

---

## 5. Color System & Rules

* **Palette Limit:** Strictly 3 tones: Base White/Cream background, Deep Carbon Ink, and exactly ONE Muted Spot Patina[cite: 1].
* **Zero Drop Shadows:** Absolute ban on drop shadows, elevations, blurs, or glow effects (`box-shadow: none !important; filter: none !important; text-shadow: none !important;`)[cite: 1]. Every element is flush with the paper plane[cite: 1].
* **Spot Tints:**
  * Sage / Copper Patina: `#B5C7BC`[cite: 1]
  * Slate Blue: `#9BB0BC`
  * Drafting Ochre: `#D8C29D`
  * Industrial Terracotta: `#C69D8E`

---

## 6. The Monolithic Spot Form

* **Singular Connected Mass:** The spot color form is one continuous polygon/vector plane[cite: 1].
* **Anatomy:**
  1. **Upper Stepped Notch:** Backs the rotated H1 text and underlaps the photographic plate[cite: 1].
  2. **Trunk:** Runs continuously beneath the photo and behind the H2 header[cite: 1].
  3. **Undulating Sinusoidal Wave:** Terminates at the base in true alternating S-curves (crests and troughs), spanning the width without detaching into isolated shapes[cite: 1].

---

## 7. Typographic Scale & Hierarchy

Base Unit: $1.0\text{rem} = 10\text{px}$ (at $600\text{px}$ canvas width).

* **Display 1 (H1 Anchor — Rotated 90° CCW):**
  * Scale: `4.8x – 5.2x` (~`48px – 52px`)[cite: 1].
  * Weight: `800` (Extra Bold)[cite: 1].
  * Leading: `0.95em – 1.0em` (Solid leading)[cite: 1].
  * Tracking: `-0.035em`[cite: 1].
  * Orientation: `writing-mode: vertical-rl; transform: rotate(180deg);`[cite: 1]
* **Display 2 (H2 Hook — Horizontal):**
  * Scale: `2.8x – 3.2x` (~`28px – 32px`)[cite: 1].
  * Weight: `700` (Bold)[cite: 1].
  * Leading: `1.05em – 1.1em`[cite: 1].
  * Tracking: `-0.025em`.
  * Alignment: Strictly flush-left to Primary Datum Line (snapped to photo left edge)[cite: 1].
* **Body Text (Columns 3–6):**
  * Scale: `1.0x` (~`9.5px – 10px`)[cite: 1].
  * Weight: `400` (Regular) with `700` subheaders[cite: 1].
  * Leading: `1.35em – 1.4em`[cite: 1].
  * Tracking: `-0.005em`.
  * Alignment: Flush-left, uniform track widths across active columns[cite: 1].
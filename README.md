# Semantic Architecture Landing Page

A structurally pure, semantic, and highly performant landing page built according to strict architectural guidelines. 

This project demonstrates the separation of layout mechanics—using **CSS Grid** for two-dimensional macro-layouts and **Flexbox** for one-dimensional micro-alignments—packaged inside a fully accessible, zero-comment HTML5 document outline.

---

## 🏗️ Architectural Blueprint

### 1. Document Architecture & Landmarks
The DOM hierarchy avoids non-semantic structural wrappers ("div soup") by utilizing distinct HTML5 landmark tags:
*   `<header>`: Anchors the top logo and navigation system.
*   `<nav>`: Encapsulates the main site navigation with accessible labeling (`aria-label`).
*   `<main>`: Standardizes the primary content flow.
*   `<article>`: Houses self-contained contents, such as the Hero Section (`.here-container`) and product Cards.
*   `<aside>`: Encapsulates the modular content grid (`.hont-cooles`).
*   `<footer>`: Anchors contact information within a structured `<address>` block.

### 2. Layout Distribution Systems
*   **CSS Grid (2D Macro Layout)**: 
    *   Manages the global 3-row layout flow of the page (`body`).
    *   Powers the responsive **12-column content grid** (`.hont-cooles__grid`) with a `24px` gutter and `60px` vertical row margin.
*   **Flexbox (1D Micro Alignment)**:
    *   Directs elements inside the header navigation.
    *   Aligns headline and button components inside the Hero Section.
    *   Structures vertical stacking and micro-spacing inside individual Cards and the Footer.

### 3. CSS Engineering Principles
*   **Separation of Concerns**: Styling is completely handled externally by [master.css](file:///Users/ekanshshrotriya/Documents/DecodeProjects/Project-1/master.css).
*   **No IDs for Styling**: Classes are utilized exclusively to ensure selector specificity remains flat and predictable.
*   **BEM Methodology**: Naming conventions follow a clean Block-Element-Modifier structure (e.g., `.button`, `.button--primary`, `.card__content`).

### 4. Accessibility (A11Y) & Core Web Vitals (CLS)
*   **CLS Prevention**: Explicit `width` and `height` attributes are declared directly on `<img />` tags, prompting modern browsers to compute and reserve correct aspect ratios before image assets download.
*   **Modern Image Formats**: The `<picture>` element serves lightweight `.webp` images to supporting browsers, falling back cleanly to `.jpg`.
*   **Accessible Naming**: Interactive items use descriptive `aria-label` labels for screen reader clarity.

---

## 🚀 Getting Started

### Local Development
To run this project locally, run a static server from the project root:

```bash
python3 -m http.server 8080 --bind 127.0.0.1
```

Once running, navigate to:
👉 **[http://localhost:8080](http://localhost:8080)**

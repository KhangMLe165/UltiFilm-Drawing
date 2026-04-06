[README-4.md](https://github.com/user-attachments/files/26521488/README-4.md)
# Ultifilm – 2D Drawing Prototype

**Author:** Khang Le  
**Team:** Khang Le, McKenna Parker, Gabriel Thiessen  
**Course:** CIS 5120 Spring 2026 | Assignment 5  
**Project Mentor:** Alice Liu  
**Mentor meeting date:** 03/27/2026

---

## How to Run

1. Clone or download this repo
2. Open `ultifilm-drawing.html` directly in any modern browser (Chrome, Firefox, Safari)
3. No installation, build step, npm, or internet connection required — it runs as a single self-contained file

---

## Technical Requirement

**2D Drawing (Annotation Layer).** Ultifilm requires coaches to draw freehand strokes, shapes, and text directly on top of game footage to highlight player positions and movements. To confirm this is satisfied, I need to show: (1) a transparent canvas rendered over a field/video frame that captures mouse input, (2) freehand drawing with at least two distinct pen styles, (3) shape tools (circle, arrow, rectangle, triangle), (4) an eraser with adjustable size that shows a visible cursor, (5) working undo and redo across all drawing actions, and (6) the canvas resetting and a new player formation loading when switching between plays in the sidebar.

---

## Evidence

📹 **[YouTube video link here]**

The screen capture shows:
1. Opening `ultifilm-drawing.html` in a browser
2. Selecting the **pen** tool and drawing freehand strokes over player dots
3. Switching to **marker**, **dashed**, **calligraphy**, and **spray** pen styles
4. Drawing a **circle** around a player and an **arrow** pointing to the disc
5. Typing a **text annotation** directly on the field
6. Adjusting the **eraser size slider** and erasing strokes — the eraser circle cursor is visible
7. Pressing **Cmd+Z** to undo and **Cmd+Y** to redo multiple steps
8. Clicking **Infinity** in the sidebar — the formation updates and the canvas clears
9. Clicking **Wall** — a different horizontal formation loads

---

## Code

**Repository:** https://github.com/KhangMLe165/UltiFilm-Drawing

| Feature | Link |
|---|---|
| Canvas setup and resize | https://github.com/KhangMLe165/UltiFilm-Drawing/blob/eedee067b99e98984bd235dd55cc77f18773570b/ultifilm-drawing.html#L764 |
| `applyStyle()` — all pen types | https://github.com/KhangMLe165/UltiFilm-Drawing/blob/eedee067b99e98984bd235dd55cc77f18773570b/ultifilm-drawing.html#L894 |
| `onDown / onMove / onUp` — pointer events | https://github.com/KhangMLe165/UltiFilm-Drawing/blob/eedee067b99e98984bd235dd55cc77f18773570b/ultifilm-drawing.html#L935 |
| `drawShape()` — arrow, circle, rect, triangle | https://github.com/KhangMLe165/UltiFilm-Drawing/blob/eedee067b99e98984bd235dd55cc77f18773570b/ultifilm-drawing.html#L1013 |
| Eraser cursor overlay + size scaling | https://github.com/KhangMLe165/UltiFilm-Drawing/blob/eedee067b99e98984bd235dd55cc77f18773570b/ultifilm-drawing.html#L799 |
| `saveUndo / undo / redo` — snapshot history | https://github.com/KhangMLe165/UltiFilm-Drawing/blob/eedee067b99e98984bd235dd55cc77f18773570b/ultifilm-drawing.html#L858 |
| `renderFormation()` — play formations | https://github.com/KhangMLe165/UltiFilm-Drawing/blob/eedee067b99e98984bd235dd55cc77f18773570b/ultifilm-drawing.html#L1145 |

---

## AI Attribution

This prototype was built with the assistance of **Claude** (Anthropic, claude.ai). Claude generated all HTML, CSS, and JavaScript in `ultifilm-drawing.html`, including:

- The full canvas drawing system (`applyStyle`, pointer event handlers, shape rendering)
- All five pen tool behaviors (pen, marker, dashed, calligraphy, spray)
- The eraser with adjustable size and visual cursor overlay
- The undo/redo system using `ImageData` snapshots
- The SVG field with three switchable player formations (Barnyard, Infinity, Wall)
- The annotation toolbar UI, color swatches, stroke size slider, and Ultifilm styling

## AI Attribution

This prototype was built with the assistance of **Claude** (Anthropic, claude.ai). Claude generated all HTML, CSS, and JavaScript in `ultifilm-drawing.html`, including:

- The full canvas drawing system (`applyStyle`, pointer event handlers, shape rendering)
- All five pen tool behaviors (pen, marker, dashed, calligraphy, spray)
- The eraser with adjustable size and visual cursor overlay
- The undo/redo system using `ImageData` snapshots
- The SVG field with three switchable player formations (Barnyard, Infinity, Wall)
- The annotation toolbar UI, color swatches, stroke size slider, and Ultifilm styling


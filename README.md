# Ultifilm – 2D Drawing Prototype

**Khang Le** | CIS 4120 Spring 2026 | Assignment 5

---

## Technical Requirement

**2D Drawing (Annotation Layer)**

To prove that Ultifilm can support freehand drawing and shape annotation directly on top of game footage, I need to show that:

- A transparent canvas can be rendered and positioned over a video/field frame
- A user can draw freehand strokes, shapes (circle, rectangle, triangle, arrow), and text on that canvas using mouse input
- Multiple pen styles are available (pen, marker, dashed, calligraphy, spray)
- An eraser with adjustable size can clear parts of the canvas
- Undo/redo history works across all drawing actions
- The canvas clears and resets when switching between plays

---

## Evidence

> 📹 **[Video demo – YouTube link here]**  
> *(Record a short screen capture showing: selecting a pen, drawing on the field, switching tools, using the eraser, undoing, and switching plays to see the formation change)*

The video shows:
1. Selecting different pen tools and drawing on the field
2. Drawing shapes (circle, arrow) over player positions
3. Adjusting eraser size and erasing strokes
4. Undo/redo working
5. Clicking a different play (Infinity → Wall) and seeing the formation update

---

## Code

**File:** [`ultifilm-drawing.html`](./ultifilm-drawing.html)

Key sections:
- **Canvas setup & resize** – lines ~760–772
- **`applyStyle()` function** – handles all pen types (pen, marker, dashed, calligraphy, spray)
- **`onDown / onMove / onUp`** – pointer event handlers for freehand and shape drawing
- **`drawShape()`** – renders arrow, circle, rectangle, triangle
- **Eraser cursor** – visual circle cursor that tracks mouse and scales with stroke size slider
- **`saveUndo()` / `undo()` / `redo()`** – ImageData snapshot-based undo/redo stack (40 steps)
- **`renderFormation()`** – swaps player dot positions on the SVG field per play

---

## How to Run

1. Clone or download this repo
2. Open `ultifilm-drawing.html` in any browser
3. No installation, build step, or internet connection required

---

## AI Attribution

This prototype was built with the assistance of **Claude** (Anthropic). Claude was used to:

- Write all HTML, CSS, and JavaScript for the drawing canvas prototype
- Implement the pen tool logic (`applyStyle`, `onMove`, spray/calligraphy/dashed stroke behaviors)
- Implement the eraser cursor overlay and size-scaling logic
- Build the SVG field with switchable player formations per play
- Set up the undo/redo ImageData snapshot system

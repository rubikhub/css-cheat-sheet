# CSS 2026 & Beyond

> 8 features

Emerging and experimental CSS features arriving through 2026.

---

## margin-trim

**Syntax:** `margin-trim: none | block | inline | block-start | block-end | inline-start | inline-end`

Removes the outer margins of child elements along container edges.

**Values:**
- `none` — no trimming (default)
- `block` — trim margins at the block start and end
- `inline` — trim margins at the inline start and end

**Use Cases:**
- Remove the last item's bottom margin in a list
- Simplify spacing in flex and grid stacks

**Example:**
```css
.stack {
  margin-trim: block;
}
```

---

## masonry()

**Syntax:** `grid-template-columns: masonry;` | `masonry-auto-flow: next | definite-first`

Native masonry layout as a grid value.

**Values:**
- `grid-template-columns: masonry;` — masonry along the row axis
- `grid-template-rows: masonry;` — masonry along the column axis
- `masonry-auto-flow: next` — items flow like a packing algorithm
- `masonry-auto-flow: definite-first` — place definite items first

**Use Cases:**
- Pinterest-style masonry galleries
- Mixed-height card grids without JS

**Example:**
```css
.masonry {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  grid-template-rows: masonry;
}
```

---

## shape-morphing

**Syntax:** `clip-path: shape(round ...);` + transition of shape() functions

Morphs elements between different geometric shapes.

**Values:**
- Combine `shape()` with `clip-path` and `transition`
- Smoothly animate between rounded, beveled, and rectangular forms
- Pairs with `corner-shape` for squircle morphing

**Use Cases:**
- Animate UI elements between shapes
- Interactive buttons that morph on hover

**Example:**
```css
.button {
  clip-path: shape(round 8px) from border-box;
  transition: clip-path 0.3s;
}

.button:hover {
  clip-path: shape(round 50%) from border-box;
}
```

---

## gap-decoration

**Syntax:** `gap-decoration-line: <line-style> <color>;`

Decorates the gaps between columns of multi-column layout.

**Values:**
- `gap-decoration-line: solid #ccc;` — a solid divider
- `gap-decoration-line: dashed #999;` — a dashed divider
- `gap-decoration-line: none;` — no decoration

**Use Cases:**
- Style dividers between text columns
- Replace border hacks for column gaps

**Example:**
```css
.columns {
  columns: 3;
  gap-decoration-line: solid #ccc;
}
```

---

## text-autospace

**Syntax:** `text-autospace: normal | no-autospace | ideograph-alpha`

Controls automatic spacing between ideographic and Latin text.

**Values:**
- `normal` — browser applies spacing (default)
- `no-autospace` — no automatic spacing
- `ideograph-alpha` — space between ideographs and Latin

**Use Cases:**
- Fix cramped CJK + Latin mixed text
- Polish localized UI copy

**Example:**
```css
body {
  text-autospace: ideograph-alpha;
}
```

---

## line-fit-edge

**Syntax:** `line-fit-edge: <edge> <edge>`

Trims the fit of a line box to the content edges of its font.

**Values:**
- `line-fit-edge: top bottom` — fit to ascent/descent
- `line-fit-edge: center` — center the line box
- `none` — default line fitting

**Use Cases:**
- Tighten line boxes around display type
- Precise vertical centering of text

**Example:**
```css
.badge {
  line-fit-edge: top bottom;
}
```

---

## Anchored Container Queries

**Syntax:** `container-type: anchored-size;`

Sizes containers based on a position-anchor's size.

**Values:**
- `container-type: anchored-size;` — size by the anchor
- `container-type: normal` — default (no size containment)
- Used with anchor-name and container queries together

**Use Cases:**
- Size popovers to their trigger
- Build anchor-sized dropdowns

**Example:**
```css
.popover {
  position: fixed;
  position-anchor: --trigger;
  container-type: anchored-size;
  width: 100cqw;
}
```

---

## interest

**Syntax:** `interest: auto | none;`

Declares an element interest area that also receives :interest when hovered or focused.

**Values:**
- `interest: auto` — the element becomes an interest target
- `:interest` — matches while the interest area is hovered or focused

**Use Cases:**
- Hover on the popover without leaving the trigger
- Keep tooltips open while moving toward them

**Example:**
```css
.tooltip-trigger {
  interest: auto;
}

.tooltip-trigger:interest .tooltip {
  opacity: 1;
}
```

---

**[View Example](../examples/advanced/32-css-2026-and-beyond/index.html)**

← **Previous Topic:** [Paged Media & Print](../advanced/31-paged-media.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Container & Modern Units](../advanced/33-container-and-modern-units.md) →

# Relative & Viewport Units

> 12 units

Advanced relative and viewport-based units for responsive sizing, typography, and layout.

> Source: [web.dev/learn/css/sizing](https://web.dev/learn/css/sizing)

---

## Font-Relative Units

### ex — X-Height

**Syntax:** `<length>ex`

Relative to the **x-height** of the current font — the height of a lowercase "x". Roughly half the font-size.

**Values:**
- `1ex` — x-height of the current font
- `0.5ex` — half the x-height

**Use Cases:**
- Aligning inline elements to the text baseline
- Superscripts and subscripts

**Example:**
```css
sub {
  font-size: 0.75ex;
  vertical-align: sub;
}
```

---

### ch — Character Width

**Syntax:** `<length>ch`

Relative to the width of the "0" (zero) glyph in the current font. Useful for monospace-aligned measurements.

**Values:**
- `1ch` — width of one "0"
- `80ch` — typical readable line length
- `60ch` — comfortable paragraph measure

**Use Cases:**
- Set readable text column widths
- Size inputs to match typed characters

**Example:**
```css
.article {
  max-width: 65ch;   /* ideal line length */
}

input {
  width: 20ch;       /* fits ~20 characters */
}
```

---

### lh and rlh — Line Height Units

**Syntax:** `<length>lh` | `<length>rlh`

`lh` is relative to the element's **line-height**; `rlh` is relative to the **root** line-height.

**Values:**
- `1lh` — one line of the current element
- `2lh` — two lines (fixed-height line boxes)
- `1rlh` — root line-height unit

**Use Cases:**
- Truncate text to a fixed number of lines
- Size decorations to match line rhythm

**Example:**
```css
.clamp {
  max-height: 3lh;              /* show 3 lines */
  overflow: hidden;
}

.text {
  min-height: 1rlh;             /* at least one root line */
}
```

---

## Viewport Units

### vmin and vmax

**Syntax:** `<length>vmin` | `<length>vmax`

`1vmin` = 1% of the **smaller** viewport dimension; `1vmax` = 1% of the **larger** viewport dimension.

**Values:**
- `100vmin` — always the shorter side of the viewport
- `100vmax` — always the longer side
- `50vmin` — half the shorter side

**Use Cases:**
- Square elements that fit any screen
- Diagonal scaling regardless of orientation

**Example:**
```css
.square {
  width: 80vmin;    /* fits portrait AND landscape */
  height: 80vmin;
}
```

---

### svh / lvh / dvh — Small, Large, Dynamic Viewport

Modern units that replace `vh` on mobile, where the URL bar hides and shows.

| Unit | Meaning |
|------|---------|
| `svh` | **small** viewport height — URL bar visible |
| `lvh` | **large** viewport height — URL bar hidden |
| `dvh` | **dynamic** viewport height — changes as the bar shows/hides |

**Use Cases:**
- `100dvh` for sticky bottom bars that stay visible
- `100svh` when content must fit without scrolling
- `100lvh` for full-screen sections

**Example:**
```css
.bottom-bar {
  height: 100dvh;   /* always fits the visible area */
}

.hero {
  height: 100svh;   /* never taller than the small viewport */
}
```

> **Note:** `vh` on mobile often means the *large* viewport — content can be cut off when the URL bar is visible.

---

### vi and vb — Viewport Inline / Block

**Syntax:** `<length>vi` | `<length>vb`

Viewport units based on the **writing direction**: `vi` = 1% of the viewport size in the inline direction, `vb` = 1% of the viewport size in the block direction.

**Values:**
- `100vi` — full viewport along the inline axis
- `100vb` — full viewport along the block axis
- `50vi` — half the inline viewport size

**Use Cases:**
- Direction-agnostic full-screen layouts
- Vertical writing modes (Japanese, etc.)

**Example:**
```css
.panel {
  inline-size: 100vi;   /* full width in LTR, height in vertical mode */
  block-size: 100vb;
}
```

---

## Fractional Units

### fr — Fraction of Available Space

**Syntax:** `<number>fr`

Used in **grid tracks** — divides free space proportionally among tracks. Only valid in `grid-template-*`.

**Values:**
- `1fr` — one share of the free space
- `2fr` — twice the share of `1fr`
- `minmax(0, 1fr)` — track that can shrink below content

**Use Cases:**
- Equal-width grid columns
- Sidebar + content layouts that share remaining space

**Example:**
```css
.grid {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;  /* 1 : 2 : 1 */
}

.sidebar-layout {
  display: grid;
  grid-template-columns: 250px 1fr;    /* fixed + flexible */
}
```

---

## Comparison Table

| Unit | Base | Best For |
|------|------|----------|
| `ex` | x-height | baseline-aligned text |
| `ch` | width of "0" | readable line lengths |
| `lh` / `rlh` | line-height | line clamping, rhythm |
| `vmin` / `vmax` | viewport min/max | orientation-safe squares |
| `svh` / `lvh` / `dvh` | mobile viewport | mobile-safe heights |
| `vi` / `vb` | viewport axes | direction-aware sizing |
| `fr` | grid free space | flexible grid tracks |

---

**[View Example](../examples/intermediate/30-relative-and-viewport-units/index.html)**

← **Previous Topic:** [Performance & Rendering](../intermediate/29-performance-and-rendering.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [:has() — The Parent Selector](../advanced/01-has-selector.md) →

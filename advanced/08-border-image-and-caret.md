# Border Image & Caret Color

> 2 properties

Advanced border styling with images and caret customization.

---

## border-image

**Syntax:** `border-image: <source> <slice> / <width> <repeat>`

Uses an image as a border instead of a solid color.

**Values:**
- `none` — no border image (default)
- `url('border.png') 30 round` — image sliced at 30px, tiles to fit
- `url('border.svg') 30 stretch` — image stretched to fill
- `url('border.png') 30 fill` — image also fills the middle area
- `border-image-source: linear-gradient(...)` — gradient as the source
- `border-image-slice: 30` — inset distance to slice the image
- `border-image-slice: 10 20 30 40` — per-edge slice offsets
- `border-image-width: 10px` — border image width
- `border-image-outset: 10px` — distance beyond the border box
- `border-image-repeat: repeat` — tiles repeated without resizing
- `border-image-repeat: round` — tiles scaled to fit evenly
- `border-image-repeat: space` — tiles with space between
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create image-based borders and frames
- Build decorative buttons and cards

**Example:**
```css
.button {
  border: 30px solid transparent;
  border-image: url('border.png') 30 round;
}
```

---

## caret-color

**Syntax:** `caret-color: <color> | auto`

Sets the color of the text insertion caret in inputs and textareas.

**Values:**
- `auto` — browser picks a color for contrast (default)
- `red` — any CSS color
- `#333` — hex color
- `currentColor` — matches the text color
- `transparent` — hides the caret
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Match the caret to a brand color
- Make the caret stand out in input fields

**Example:**
```css
.custom-caret {
  caret-color: #ff6b6b;
  border: 2px solid #333;
}
```

---

**[View Example](../examples/advanced/08-border-image-and-caret/index.html)**

← **Previous Topic:** [Typography 2024+](../advanced/07-typography-2024.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [CSS Counters — Complex Patterns](../advanced/09-css-counters-complex.md) →

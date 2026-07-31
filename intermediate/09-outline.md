# Outline

> 6 properties

Focus indicators and outline styling that do not affect layout.

---

## outline

**Syntax:** `outline: <width> <style> <color>`

Outline — a line drawn outside the border edge that doesn't affect layout.

**Values:**
- `1px` — width only
- `solid` — style only
- `red` — color only
- `1px solid` — width and style
- `1px solid red` — full outline
- `2px dashed blue 3px` — outline with offset
- `inherit` — inherits from parent
- `initial` — sets to default (medium none currentColor)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Highlight focused elements
- Draw focus indicators without layout shift

**Example:**
```css
button:focus {
  outline: 2px solid #6c5ce7;
}
```

---

## outline-width

**Syntax:** `outline-width: <length> | thin | medium | thick`

Outline thickness — controls how thick the outline is.

**Values:**
- `thin` — thin outline
- `medium` — medium outline
- `thick` — thick outline
- `2px` — pixel-based width
- `0` — no outline
- `inherit` — inherits from parent
- `initial` — sets to default (medium)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Make focus indicators more visible
- Control outline thickness independently

**Example:**
```css
:focus-visible {
  outline-style: solid;
  outline-width: 2px;
}
```

---

## outline-style

**Syntax:** `outline-style: auto | none | dotted | dashed | solid | double | groove | ridge | inset | outset`

Outline style — same values as border-style.

**Values:**
- `none` — no outline
- `auto` — browser-defined style
- `dotted` — dotted line
- `dashed` — dashed line
- `solid` — solid line
- `double` — double line
- `groove` — 3D grooved line
- `ridge` — 3D ridged line
- `inset` — 3D inset line
- `outset` — 3D outset line
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Style focus outlines
- Create dashed outlines for debugging

**Example:**
```css
:focus-visible {
  outline-style: dashed;
  outline-color: #fdcb6e;
}
```

---

## outline-color

**Syntax:** `outline-color: <color> | invert`

Outline color — sets the outline's color independently.

**Values:**
- `invert` — inverted color for visibility
- `red` — named color
- `#ff5733` — hex color
- `rgb(255, 0, 0)` — rgb color
- `inherit` — inherits from parent
- `initial` — sets to default (currentColor)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Match outline color to a brand
- Make focus rings stand out

**Example:**
```css
:focus-visible {
  outline-style: solid;
  outline-color: #e17055;
}
```

---

## outline-offset

**Syntax:** `outline-offset: <length>`

Outline gap — distance between the border edge and the outline.

**Values:**
- `3px` — outline pushed outward
- `-2px` — outline drawn inside the border edge
- `0` — outline flush with the border edge (default)
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Separate focus rings from the element
- Draw an outline inside the element

**Example:**
```css
:focus-visible {
  outline: 2px solid #6c5ce7;
  outline-offset: 2px;
}
```

---

## box-decoration-break

**Syntax:** `box-decoration-break: slice | clone`

Controls how borders, backgrounds, and shadows split across line or column breaks.

**Values:**
- `slice` — decorations are cut at the break (default)
- `clone` — decorations repeat on each fragment

**Use Cases:**
- Keep rounded corners on wrapped inline highlights
- Apply padding per line for highlighted text

**Example:**
```css
mark {
  padding: 0.2em 0.4em;
  border-radius: 4px;
  box-decoration-break: clone;
}
```

---

**[View Example](../examples/intermediate/09-outline/index.html)**

← **Previous Topic:** [Border Advanced](../intermediate/08-border-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Border Radius](../intermediate/10-border-radius.md) →


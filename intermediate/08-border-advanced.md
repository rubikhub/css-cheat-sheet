# Border Advanced

> 4 properties

Border styling — width, style, color, and image borders.

---

## Border

---

## border

**Syntax:** `border: <width> <style> <color>`

Shorthand — sets border width, style, and color on all sides.

**Values:**
- `1px` — width only
- `solid` — style only
- `red` — color only
- `1px solid` — width and style
- `1px solid red` — full border
- `1px red` — width and color
- `inherit` — inherits from parent
- `initial` — sets to default (medium none currentColor)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Give elements a visible edge
- Combine width, style, and color in one declaration

**Example:**
```css
.card {
  border: 1px solid #e5e5e5;
}

.error {
  border: 2px solid red;
}
```

---

## border-style

**Syntax:** `border-style: none | hidden | dotted | dashed | solid | double | groove | ridge | inset | outset`

Line style — sets the style of the border on all sides.

**Values:**
- `none` — no border
- `hidden` — no border, hides in table layout
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
- Create dashed or dotted separators
- Add a solid border to elements

**Example:**
```css
.dashed {
  border-style: dashed;
}

.solid {
  border-style: solid;
}
```

---

## border-top / right / bottom / left

**Syntax:** `border-top: <width> <style> <color>` (also `border-right`, `border-bottom`, `border-left`)

Individual sides — sets the border on one edge independently.

**Values:**
- `1px` — width only
- `solid` — style only
- `red` — color only
- `1px solid red` — full top border
- `2px dashed blue` — dashed top border
- `inherit` — inherits from parent
- `initial` — sets to default (medium none currentColor)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Style individual edges of an element
- Create underlines and separators

**Example:**
```css
.section {
  border-top: 3px solid #d63031;
  border-bottom: 3px solid #0984e3;
}
```

---

## border-image

**Syntax:** `border-image: <source> <slice> / <width> / <outset> <repeat>`

Image border — uses an image slice as the border decoration.

**Values:**
- `url('border.png') 30` — image with slice
- `url('border.png') 30 / 10px` — slice with border width
- `url('border.png') 30 / 10px / 5px stretch` — full shorthand with repeat
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create image-based borders
- Add decorative gradient or pattern borders

**Example:**
```css
.badge {
  border: 4px solid;
  border-image: linear-gradient(135deg, #6c5ce7, #fd79a8) 1;
}
```

---

**[View Example](../examples/intermediate/08-border-advanced/index.html)**

← **Previous Topic:** [Text Layout & Wrapping](../intermediate/07-text-layout.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Outline](../intermediate/09-outline.md) →


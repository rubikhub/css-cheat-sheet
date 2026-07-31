# Border Advanced

> 15 properties

Border styling — width, style, color, outlines, rounded corners, and drop shadows.

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

## Outline

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

## Border Radius

---

## border-radius

**Syntax:** `border-radius: <length> | <percentage>`

Rounded corners — curves the border-box corners.

**Values:**
- `10px` — rounded corners
- `50%` — fully rounded, circle or pill shape
- `0` — square corners
- `10px 20px` — two-value radii
- `10px 20px 30px` — three-value radii
- `10px 20px 30px 40px` — all four corners
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Round button and card corners
- Create circular or pill-shaped elements

**Example:**
```css
.button {
  border-radius: 8px;
}

.avatar {
  border-radius: 50%;
}
```

---

## border-top-left-radius / top-right-radius

**Syntax:** `border-<corner>-radius: <length> | <percentage>`

Individual corner — radius for a specific corner.

**Values:**
- `10px` — rounded corner
- `50%` — fully rounded corner
- `10px 20px` — horizontal and vertical radii
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Round individual corners of a card
- Create asymmetric shapes

**Example:**
```css
.card {
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
}
```

---

## border-bottom-left-radius / bottom-right-radius

**Syntax:** `border-<corner>-radius: <length> | <percentage>`

Individual corner — radius for a specific corner.

**Values:**
- `10px` — rounded corner
- `50%` — fully rounded corner
- `10px 20px` — horizontal and vertical radii
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Round bottom corners of a card
- Create pill or squircle shapes

**Example:**
```css
.pill {
  border-bottom-left-radius: 50%;
  border-bottom-right-radius: 50%;
}
```

---

## border-start-radius / border-end-radius

**Syntax:** `border-start-start-radius: <length> | <percentage>` (also `border-start-end-radius`, `border-end-start-radius`, `border-end-end-radius`)

Logical corner radius — maps to physical corners based on writing direction.

**Values:**
- `border-start-start-radius: 16px` — first logical corner
- `border-start-end-radius: 0` — no rounding
- `border-end-start-radius: 0` — no rounding
- `border-end-end-radius: 16px` — last logical corner
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Round corners based on writing direction
- Support RTL layouts with logical properties

**Example:**
```css
.card {
  border-start-start-radius: 16px;
  border-end-end-radius: 16px;
}
```

---

## Shadow

---

## box-shadow

**Syntax:** `box-shadow: none | <offset-x> <offset-y> <blur> <spread> <color>`

Drop shadow — adds one or more shadows behind the element.

**Values:**
- `0 4px 6px rgba(108, 92, 231, 0.4)` — single shadow
- `0 4px 6px rgba(108, 92, 231, 0.4), 0 12px 24px rgba(108, 92, 231, 0.2)` — layered shadows
- `none` — no shadow (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create depth and elevation
- Add soft shadows to cards

**Example:**
```css
.card {
  box-shadow: 0 4px 6px rgba(108, 92, 231, 0.4);
}
```

---

## box-shadow: inset

**Syntax:** `box-shadow: inset <offset-x> <offset-y> <blur> <spread> <color>`

Inset shadows — appear inside the element's border.

**Values:**
- `inset 0 2px 8px rgba(0, 0, 0, 0.6)` — inner shadow
- `inset 0 2px 8px rgba(0, 0, 0, 0.6), 0 4px 12px rgba(0, 0, 0, 0.3)` — inner and outer shadows combined
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create pressed-in button effects
- Add depth to wells and panels

**Example:**
```css
.well {
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.6);
}
```

---

**[View Example](../examples/intermediate/05-border-advanced/index.html)**

← **Previous Topic:** [Typography Advanced](../intermediate/04-typography-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Counters & Markers](../intermediate/06-counters-and-markers.md) →

# Border Basics

> 8 properties

Borders, outlines, and rounded corners for element framing.

---

## Border

---

## border-width

**Syntax:** `border-width: <length> | thin | medium | thick`

Border thickness — controls the width of the border.

**Values:**
- `thin` — thin border
- `medium` — medium border (default)
- `thick` — thick border
- `1px` — pixel width
- `2px` — thicker border
- `0` — no border
- `inherit` — inherits from parent
- `initial` — sets to default (medium)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create subtle 1px borders
- Add emphasis with thicker borders

**Example:**
```css
.card {
  border-width: 1px;
  border-style: solid;
}

.emphasis {
  border-width: 3px;
  border-style: solid;
}
```

---

## border-style

**Syntax:** `border-style: none | solid | dashed | dotted | double | groove | ridge | inset | outset`

Border pattern — solid, dashed, dotted, double, groove, ridge, inset, outset.

**Values:**
- `none` — no border (default)
- `solid` — solid line
- `dashed` — dashed line
- `dotted` — dotted line
- `double` — double line
- `groove` — 3D grooved effect
- `ridge` — 3D ridged effect
- `inset` — 3D inset effect
- `outset` — 3D outset effect
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create solid borders for cards
- Use dashed borders for secondary elements

**Example:**
```css
.card {
  border-style: solid;
}

.secondary {
  border-style: dashed;
}
```

---

## border-color

**Syntax:** `border-color: <color>`

Border color — sets the color of the border.

**Values:**
- `currentColor` — matches text color
- `#ccc` — hex color
- `rgb(0, 0, 0)` — RGB color
- `red` — named color
- `transparent` — invisible border
- `inherit` — inherits from parent
- `initial` — sets to default (user agent)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create subtle gray borders
- Add colored accent borders

**Example:**
```css
.card {
  border-color: #e0e0e0;
}

.accent {
  border-color: #0066cc;
}
```

---

## border

**Syntax:** `border: <width> <style> <color>`

Shorthand — sets width, style, and color in one declaration.

**Values:**
- `1px solid #ccc` — width style color
- `2px dashed red` — thick dashed border
- `none` — no border (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none medium none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add simple borders to cards
- Create visual separation between sections

**Example:**
```css
.card {
  border: 1px solid #e0e0e0;
}

.highlight {
  border: 2px solid #0066cc;
}
```

---

## Border Radius

---

## border-radius

**Syntax:** `border-radius: <length> | <percentage>`

Rounded corners — rounds the corners of the outer border edge.

**Values:**
- `4px` — slight rounding
- `8px` — moderate rounding
- `50%` — fully round (circle/ellipse)
- `1rem` — rem-based rounding
- `4px 8px` — top-left/bottom-right | top-right/bottom-left
- `4px 8px 12px 16px` — top-left | top-right | bottom-right | bottom-left
- `0` — no rounding (default)
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create rounded buttons and cards
- Make circular avatars

**Example:**
```css
.card {
  border-radius: 8px;
}

.avatar {
  border-radius: 50%;
  width: 48px;
  height: 48px;
}
```

---

**[View Example](../examples/beginner/10-border-basics/index.html)**

← **Previous Topic:** [Typography Basics](../beginner/09-typography-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Lists Basics](../beginner/11-lists-basics.md) →


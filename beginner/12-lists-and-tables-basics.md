# Lists & Tables Basics

> 10 properties

Styling for ordered/unordered lists and table layouts.

---

## Lists

---

## list-style-type

**Syntax:** `list-style-type: disc | circle | square | decimal | none | <string>`

Bullet/number style — controls the marker appearance.

**Values:**
- `disc` — filled circle (default)
- `circle` — hollow circle
- `square` — filled square
- `decimal` — numbers (1, 2, 3)
- `decimal-leading-zero` — zero-padded (01, 02, 03)
- `lower-roman` — lowercase roman (i, ii, iii)
- `upper-roman` — uppercase roman (I, II, III)
- `lower-alpha` — lowercase letters (a, b, c)
- `upper-alpha` — uppercase letters (A, B, C)
- `none` — no marker
- `inherit` — inherits from parent
- `initial` — sets to default (disc)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create numbered steps
- Remove default bullets

**Example:**
```css
ol {
  list-style-type: decimal;
}

.steps {
  list-style-type: decimal-leading-zero;
}

.no-bullets {
  list-style-type: none;
}
```

---

## list-style-position

**Syntax:** `list-style-position: inside | outside`

Marker placement — inside or outside the content flow.

**Values:**
- `outside` — marker outside content (default)
- `inside` — marker inside content
- `inherit` — inherits from parent
- `initial` — sets to default (outside)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Indent markers inside content
- Create tight list layouts

**Example:**
```css
ul {
  list-style-position: inside;
}
```

---

## list-style-image

**Syntax:** `list-style-image: none | <image>`

Custom marker image — replaces default bullets with images.

**Values:**
- `none` — use default marker (default)
- `url('bullet.png')` — custom image
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Use custom icons as bullets
- Brand list markers

**Example:**
```css
ul {
  list-style-image: url('checkmark.png');
}
```

---

## list-style

**Syntax:** `list-style: <type> <position> <image>`

Shorthand — combines type, position, and image.

**Values:**
- `disc inside` — type position
- `decimal url('bullet.png')` — type image
- `none` — no styling
- `inherit` — inherits from parent
- `initial` — sets to default (disc outside none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Simplify list declarations
- Set multiple list properties at once

**Example:**
```css
ul {
  list-style: square inside;
}

.steps {
  list-style: decimal-leading-zero outside;
}
```

---

## Tables

---

## border-collapse

**Syntax:** `border-collapse: separate | collapse`

Border model — separate or collapse adjacent borders.

**Values:**
- `separate` — borders are separate (default)
- `collapse` — borders collapse into one
- `inherit` — inherits from parent
- `initial` — sets to default (separate)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create clean table borders
- Remove double borders

**Example:**
```css
table {
  border-collapse: collapse;
}
```

---

## border-spacing

**Syntax:** `border-spacing: <length>`

Cell spacing — space between table cells (separate mode only).

**Values:**
- `0` — no spacing (default)
- `4px` — small spacing
- `8px 12px` — vertical horizontal
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add breathing room between cells
- Create visual separation

**Example:**
```css
table {
  border-spacing: 8px;
}
```

---

## table-layout

**Syntax:** `table-layout: auto | fixed`

Algorithm — automatic or fixed-width columns.

**Values:**
- `auto` — column width based on content (default)
- `fixed` — column width based on first row
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Speed up table rendering
- Create consistent column widths

**Example:**
```css
table {
  table-layout: fixed;
  width: 100%;
}
```

---

## caption-side

**Syntax:** `caption-side: top | bottom`

Caption position — above or below the table.

**Values:**
- `top` — above table (default)
- `bottom` — below table
- `inherit` — inherits from parent
- `initial` — sets to default (top)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Position table titles
- Create accessible table labels

**Example:**
```css
caption {
  caption-side: bottom;
}
```

---

## empty-cells

**Syntax:** `empty-cells: show | hide`

Empty cell visibility — show or hide borders/backgrounds.

**Values:**
- `show` — show empty cells (default)
- `hide` — hide empty cells
- `inherit` — inherits from parent
- `initial` — sets to default (show)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Hide empty table cells
- Create cleaner table layouts

**Example:**
```css
table {
  empty-cells: hide;
}
```

---

## vertical-align

**Syntax:** `vertical-align: baseline | sub | super | text-top | text-bottom | middle | top | bottom`

Vertical alignment — aligns inline/table cell content.

**Values:**
- `baseline` — align to baseline (default)
- `sub` — subscript
- `super` — superscript
- `text-top` — align to text top
- `text-bottom` — align to text bottom
- `middle` — vertical middle
- `top` — align to top
- `bottom` — align to bottom
- `inherit` — inherits from parent
- `initial` — sets to default (baseline)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Align icons with text
- Position table cell content

**Example:**
```css
.icon {
  vertical-align: middle;
}

td {
  vertical-align: top;
}
```
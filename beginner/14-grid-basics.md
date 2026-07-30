# Grid Basics

> 12 properties

Two-dimensional layout for rows and columns simultaneously.

---

## Container

---

## display: grid

**Syntax:** `display: grid | inline-grid`

Grid container — enables grid layout for children.

**Values:**
- `grid` — block-level grid container
- `inline-grid` — inline-level grid container
- `inherit` — inherits from parent
- `initial` — sets to default (inline)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create complex page layouts
- Build responsive card grids

**Example:**
```css
.container {
  display: grid;
}
```

---

## grid-template-columns

**Syntax:** `grid-template-columns: <track-list>`

Column tracks — defines column widths and number.

**Values:**
- `1fr 1fr 1fr` — three equal columns
- `200px 1fr` — fixed sidebar, flexible main
- `repeat(3, 1fr)` — three equal columns
- `repeat(auto-fit, minmax(200px, 1fr))` — responsive grid
- `100px auto 1fr` — mixed sizing
- `none` — no explicit columns (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create responsive card layouts
- Build magazine-style layouts

**Example:**
```css
.grid {
  grid-template-columns: repeat(3, 1fr);
}

.sidebar-layout {
  grid-template-columns: 250px 1fr;
}
```

---

## grid-template-rows

**Syntax:** `grid-template-rows: <track-list>`

Row tracks — defines row heights and number.

**Values:**
- `100px 1fr 100px` — header, main, footer
- `repeat(3, minmax(100px, auto))` — minimum row heights
- `auto 1fr auto` — content-based rows
- `none` — no explicit rows (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create fixed-height headers and footers
- Ensure minimum row heights

**Example:**
```css
.layout {
  grid-template-rows: auto 1fr auto;
}
```

---

## gap

**Syntax:** `gap: <length> | <percentage>`

Spacing between tracks — adds space between grid items.

**Values:**
- `16px` — small gap
- `1rem` — rem-based gap
- `0` — no gap (default)
- `16px 24px` — row-gap column-gap
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create consistent spacing in grids
- Replace margins on grid children

**Example:**
```css
.grid {
  display: grid;
  gap: 20px;
}
```

---

## justify-items

**Syntax:** `justify-items: start | end | center | stretch`

Horizontal alignment — aligns items within their grid cells.

**Values:**
- `stretch` — stretch to fill cell (default)
- `start` — align to cell start
- `end` — align to cell end
- `center` — center in cell
- `inherit` — inherits from parent
- `initial` — sets to default (stretch)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center content in grid cells
- Align items to one side of cells

**Example:**
```css
.centered {
  justify-items: center;
}
```

---

## align-items

**Syntax:** `align-items: start | end | center | stretch`

Vertical alignment — aligns items within their grid cells.

**Values:**
- `stretch` — stretch to fill cell (default)
- `start` — align to cell start
- `end` — align to cell end
- `center` — center in cell
- `inherit` — inherits from parent
- `initial` — sets to default (stretch)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Vertically center content
- Align items to bottom of cells

**Example:**
```css
.vertically-centered {
  align-items: center;
}
```

---

## Items

---

## grid-column

**Syntax:** `grid-column: <start> | <start> / <end>`

Column placement — positions item in grid columns.

**Values:**
- `1 / 3` — span columns 1 to 3
- `span 2` — span 2 columns
- `1` — start at column 1
- `auto` — auto placement (default)
- `-1` — last column
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Span items across multiple columns
- Place items in specific columns

**Example:**
```css
.full-width {
  grid-column: 1 / -1;
}

.wide {
  grid-column: span 2;
}
```

---

## grid-row

**Syntax:** `grid-row: <start> | <start> / <end>`

Row placement — positions item in grid rows.

**Values:**
- `1 / 3` — span rows 1 to 3
- `span 2` — span 2 rows
- `1` — start at row 1
- `auto` — auto placement (default)
- `-1` — last row
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Span items across multiple rows
- Place items in specific rows

**Example:**
```css
.tall {
  grid-row: span 2;
}
```

---


## justify-self

**Syntax:** `justify-self: start | end | center | stretch`

Horizontal item alignment — overrides justify-items for single item.

**Values:**
- `stretch` — stretch to fill cell (default)
- `start` — align to cell start
- `end` — align to cell end
- `center` — center in cell
- `inherit` — inherits from parent
- `initial` — sets to default (stretch)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Override alignment for specific items
- Center individual grid items

**Example:**
```css
.special {
  justify-self: center;
}
```

---

## align-self

**Syntax:** `align-self: start | end | center | stretch`

Vertical item alignment — overrides align-items for single item.

**Values:**
- `stretch` — stretch to fill cell (default)
- `start` — align to cell start
- `end` — align to cell end
- `center` — center in cell
- `inherit` — inherits from parent
- `initial` — sets to default (stretch)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Override alignment for specific items
- Vertically center individual grid items

**Example:**
```css
.special {
  align-self: end;
}
```

---

**[View Example](../examples/beginner/14-grid-basics/index.html)**

← **Previous Topic:** [Flexbox Basics](../beginner/13-flexbox-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Opacity](../beginner/15-opacity.md) →

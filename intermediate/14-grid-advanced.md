# Grid Advanced

> 14 properties

Two-dimensional layout — advanced grid container and item properties.

---

## Container

---

## grid-template-columns

**Syntax:** `grid-template-columns: <track-list>`

Columns — defines the column tracks of a grid container.

**Values:**
- `none` — no explicit columns (default)
- `200px` — single fixed column
- `200px 100px auto` — mixed fixed and auto columns
- `repeat(3, 1fr)` — three equal columns
- `repeat(2, minmax(100px, 1fr))` — two flexible columns
- `repeat(auto-fit, minmax(200px, 1fr))` — responsive grid that grows to fill
- `repeat(auto-fill, minmax(150px, 1fr))` — fills available space with columns
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
  grid-template-columns: 200px 1fr;
}
```

---

## grid-template-rows

**Syntax:** `grid-template-rows: <track-list>`

Rows — defines the row tracks of a grid container.

**Values:**
- `none` — no explicit rows (default)
- `100px` — single fixed row
- `100px 200px auto` — mixed fixed and auto rows
- `repeat(3, 1fr)` — three equal rows
- `minmax(50px, auto)` — minimum height row
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

.card-grid {
  grid-template-rows: repeat(3, minmax(100px, auto));
}
```

---

## grid-template-areas

**Syntax:** `grid-template-areas: <string> | none`

Areas — names grid areas for placement by name.

**Values:**
- `none` — no named areas (default)
- `"header header"` — two-column header row
- `"sidebar main"` — two-column content row
- `"footer footer"` — two-column footer row
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Define named page layouts
- Place items by area name with `grid-area`

**Example:**
```css
.layout {
  display: grid;
  grid-template-columns: 1fr 2fr;
  grid-template-areas:
    "header header"
    "sidebar main"
    "footer footer";
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
.footer { grid-area: footer; }
```

---

## grid-auto-columns

**Syntax:** `grid-auto-columns: <track-size>`

Auto columns — sets the size for auto-placed columns.

**Values:**
- `auto` — auto-sized (default)
- `100px` — fixed size
- `1fr` — flexible size
- `min-content` — smallest content size
- `max-content` — largest content size
- `minmax(100px, 1fr)` — min/max size range
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Size columns created by auto-placement
- Create flexible implicit tracks

**Example:**
```css
.auto-grid {
  display: grid;
  grid-template-columns: 80px;
  grid-auto-columns: 1fr;
  grid-auto-flow: column;
}
```

---

## grid-auto-rows

**Syntax:** `grid-auto-rows: <track-size>`

Auto rows — sets the size for auto-placed rows.

**Values:**
- `auto` — auto-sized (default)
- `100px` — fixed size
- `1fr` — flexible size
- `min-content` — smallest content size
- `max-content` — largest content size
- `minmax(50px, auto)` — min/max size range
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Size rows created by auto-placement
- Ensure minimum row heights

**Example:**
```css
.auto-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-auto-rows: 40px;
}
```

---

## grid-auto-flow

**Syntax:** `grid-auto-flow: row | column | dense`

Auto flow — controls how auto-placed items are inserted.

**Values:**
- `row` — fill by rows (default)
- `column` — fill by columns
- `dense` — backfill gaps left by earlier items
- `row dense` — rows with dense packing
- `column dense` — columns with dense packing
- `inherit` — inherits from parent
- `initial` — sets to default (row)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Control the order auto-placed items fill
- Pack items densely to fill gaps

**Example:**
```css
.masonry {
  display: grid;
  grid-auto-flow: column;
}

.dense {
  grid-auto-flow: row dense;
}
```

---

## Items

---

## grid-column

**Syntax:** `grid-column: <start> | <start> / <end>`

Column span — places an item across grid columns.

**Values:**
- `1 / 3` — from line 1 to line 3
- `1 / span 2` — start at line 1, span 2 columns
- `span 2` — span 2 columns
- `auto` — auto placement (default)
- `auto / 1` — end at line 1
- `header-start / header-end` — place by named lines
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

Row span — places an item across grid rows.

**Values:**
- `1 / 3` — from row line 1 to line 3
- `1 / span 2` — start at line 1, span 2 rows
- `span 2` — span 2 rows
- `auto` — auto placement (default)
- `auto / 1` — end at line 1
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

## grid-area

**Syntax:** `grid-area: <name> | <row-start> / <column-start> / <row-end> / <column-end>`

Area — places an item into a named grid area or by line numbers.

**Values:**
- `header` — place into a named area
- `sidebar` — place into a named area
- `1 / 1 / 3 / 3` — row-start / column-start / row-end / column-end
- `1 / span 2 / 3 / span 2` — line numbers with spans
- `auto` — auto placement (default)
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Place items into named template areas
- Shorthand for full row/column placement

**Example:**
```css
.header {
  grid-area: header;
}

.hero {
  grid-area: 1 / 1 / 3 / 3;
}
```

---

## justify-items

**Syntax:** `justify-items: start | end | center | stretch | left | right`

Justify items — aligns items along the inline (row) axis within their cell.

**Values:**
- `stretch` — stretch to fill cell (default)
- `start` — align to cell start
- `end` — align to cell end
- `center` — center in cell
- `left` — align left
- `right` — align right
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

**Syntax:** `align-items: start | end | center | stretch | baseline | self-start | self-end`

Align items — aligns items along the block (column) axis within their cell.

**Values:**
- `stretch` — stretch to fill cell (default)
- `start` — align to cell start
- `end` — align to cell end
- `center` — center in cell
- `baseline` — align by text baseline
- `self-start` — align to own start edge
- `self-end` — align to own end edge
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

## place-items

**Syntax:** `place-items: <align-items> <justify-items>`

Place items — shorthand for align-items and justify-items together.

**Values:**
- `center` — centered on both axes
- `start` — aligned to start on both axes
- `stretch` — stretched on both axes
- `center start` — center vertically, start horizontally
- `stretch end` — stretch vertically, end horizontally
- `inherit` — inherits from parent
- `initial` — sets to default (stretch)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center content in one declaration
- Combine row and column alignment

**Example:**
```css
.centered {
  place-items: center;
}
```

---

## place-content

**Syntax:** `place-content: <align-content> <justify-content>`

Shorthand — sets align-content and justify-content together for the grid container.

**Values:**
- `center` — centered on both axes
- `start` — aligned to start on both axes
- `space-between` — spread out on both axes
- `center space-between` — center rows, space columns
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center the whole grid in its container
- Control free space around tracks

**Example:**
```css
.center-grid {
  place-content: center;
}

.distributed {
  place-content: space-between;
}
```

---

## place-self

**Syntax:** `place-self: <align-self> <justify-self>`

Shorthand — sets align-self and justify-self together for a grid item.

**Values:**
- `center` — centered in the cell on both axes
- `start` — aligned to cell start on both axes
- `stretch` — stretched in both axes
- `end center` — aligned to the end vertically, center horizontally
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Align a single grid item quickly
- Override container alignment for one item

**Example:**
```css
.badge {
  place-self: end center;
}
```

---

**[View Example](../examples/intermediate/14-grid-advanced/index.html)**

← **Previous Topic:** [Flexbox Advanced](../intermediate/13-flexbox-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Structural Pseudo Classes](../intermediate/15-structural-pseudo-classes.md) →


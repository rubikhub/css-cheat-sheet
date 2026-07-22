# Flexbox Basics

> 12 properties

One-dimensional layout for distributing space and aligning items.

---

## Container

---

## display: flex

**Syntax:** `display: flex | inline-flex`

Flex container — enables flexbox layout for children.

**Values:**
- `flex` — block-level flex container
- `inline-flex` — inline-level flex container
- `inherit` — inherits from parent
- `initial` — sets to default (inline)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create flexible layouts
- Align items in a row or column

**Example:**
```css
.container {
  display: flex;
}
```

---

## flex-direction

**Syntax:** `flex-direction: row | row-reverse | column | column-reverse`

Main axis direction — horizontal or vertical layout.

**Values:**
- `row` — horizontal, left to right (default)
- `row-reverse` — horizontal, right to left
- `column` — vertical, top to bottom
- `column-reverse` — vertical, bottom to top
- `inherit` — inherits from parent
- `initial` — sets to default (row)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create horizontal navigation
- Stack items vertically

**Example:**
```css
.row {
  flex-direction: row;
}

.column {
  flex-direction: column;
}
```

---

## flex-wrap

**Syntax:** `flex-wrap: nowrap | wrap | wrap-reverse`

Wrapping behavior — whether items wrap to new lines.

**Values:**
- `nowrap` — all items on one line (default)
- `wrap` — items wrap to new lines
- `wrap-reverse` — items wrap upward
- `inherit` — inherits from parent
- `initial` — sets to default (nowrap)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create responsive grids
- Prevent items from overflowing

**Example:**
```css
.grid {
  flex-wrap: wrap;
}

.no-overflow {
  flex-wrap: nowrap;
}
```

---

## justify-content

**Syntax:** `justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly`

Main axis alignment — distributes space between and around items.

**Values:**
- `flex-start` — items at start (default)
- `flex-end` — items at end
- `center` — items centered
- `space-between` — items with space between
- `space-around` — items with space around
- `space-evenly` — items with equal space
- `inherit` — inherits from parent
- `initial` — sets to default (flex-start)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center items horizontally
- Create navigation with space between logo and links

**Example:**
```css
.centered {
  justify-content: center;
}

.nav {
  justify-content: space-between;
}
```

---

## align-items

**Syntax:** `align-items: flex-start | flex-end | center | stretch | baseline`

Cross axis alignment — aligns items along the cross axis.

**Values:**
- `stretch` — stretch to fill container (default)
- `flex-start` — items at start
- `flex-end` — items at end
- `center` — items centered
- `baseline` — items aligned by text baseline
- `inherit` — inherits from parent
- `initial` — sets to default (stretch)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center items vertically in a row
- Align items to bottom of container

**Example:**
```css
.centered {
  align-items: center;
}

.bottom {
  align-items: flex-end;
}
```

---

## align-content

**Syntax:** `align-content: flex-start | flex-end | center | space-between | space-around | stretch`

Cross axis spacing — distributes space between wrapped lines.

**Values:**
- `stretch` — stretch to fill (default)
- `flex-start` — lines at start
- `flex-end` — lines at end
- `center` — lines centered
- `space-between` — space between lines
- `space-around` — space around lines
- `space-evenly` — equal space between lines
- `inherit` — inherits from parent
- `initial` — sets to default (stretch)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center wrapped content vertically
- Space out multiple rows evenly

**Example:**
```css
.wrapped-content {
  flex-wrap: wrap;
  align-content: center;
}
```

---

## gap

**Syntax:** `gap: <length> | <percentage>`

Spacing between items — adds space between flex items.

**Values:**
- `8px` — small gap
- `1rem` — rem-based gap
- `0` — no gap (default)
- `16px 24px` — row-gap column-gap
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create consistent spacing between items
- Replace margins on flex children

**Example:**
```css
.container {
  display: flex;
  gap: 16px;
}

.tight {
  gap: 8px;
}
```

---

## Items

---

## flex-grow

**Syntax:** `flex-grow: <number>`

Growth factor — how much item grows relative to siblings.

**Values:**
- `0` — don't grow (default)
- `1` — grow equally
- `2` — grow twice as much
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create equal-width columns
- Make one item fill remaining space

**Example:**
```css
.equal {
  flex-grow: 1;
}

.sidebar {
  flex-grow: 0;
  width: 200px;
}

.main {
  flex-grow: 1;
}
```

---

## flex-shrink

**Syntax:** `flex-shrink: <number>`

Shrink factor — how much item shrinks relative to siblings.

**Values:**
- `0` — don't shrink
- `1` — shrink equally (default)
- `2` — shrink twice as much
- `inherit` — inherits from parent
- `initial` — sets to default (1)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Prevent items from shrinking
- Control which items shrink first

**Example:**
```css
.no-shrink {
  flex-shrink: 0;
}

.sidebar {
  flex-shrink: 0;
  width: 200px;
}
```

---

## flex-basis

**Syntax:** `flex-basis: <length> | <percentage> | auto | content`

Initial size — starting size before growing/shrinking.

**Values:**
- `auto` — use width/height (default)
- `content` — intrinsic content size
- `0` — zero initial size
- `200px` — fixed size
- `50%` — percentage of container
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Set initial width before growth
- Create equal-width items

**Example:**
```css
.item {
  flex-basis: 200px;
  flex-grow: 1;
}
```

---

## flex

**Syntax:** `flex: <grow> <shrink> <basis>`

Shorthand — sets grow, shrink, and basis in one declaration.

**Values:**
- `1` — grow equally, shrink equally, basis 0
- `0 1 auto` — don't grow, shrink, auto basis (default)
- `1 1 0` — grow and shrink equally
- `0 0 200px` — fixed width, no grow/shrink
- `inherit` — inherits from parent
- `initial` — sets to default (0 1 auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Simplify flex item declarations
- Create equal-width columns

**Example:**
```css
.equal {
  flex: 1;
}

.fixed {
  flex: 0 0 200px;
}

.grow-only {
  flex: 1 0 auto;
}
```

---

## order

**Syntax:** `order: <integer>`

Visual order — reorders items without changing DOM.

**Values:**
- `0` — default order
- `1` — first position
- `-1` — last position
- `2` — second position
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Reorder items for mobile layouts
- Put important content first visually

**Example:**
```css
.sidebar {
  order: -1;
}

.main {
  order: 0;
}
```
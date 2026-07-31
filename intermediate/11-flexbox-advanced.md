# Flexbox Advanced

> 14 properties

Advanced flexbox — container and item properties for distributing and aligning items.

---

## Container

---

## display

**Syntax:** `display: flex | inline-flex`

Flex container — enables flex layout on children.

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
.nav {
  flex-direction: row;
}

.sidebar {
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
.card-grid {
  display: flex;
  flex-wrap: wrap;
}
```

---

## justify-content

**Syntax:** `justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly | start | end | left | right | stretch`

Main axis alignment — distributes space along the main axis.

**Values:**
- `flex-start` — items at start (default)
- `flex-end` — items at end
- `center` — items centered
- `space-between` — space between items
- `space-around` — space around items
- `space-evenly` — equal space around items
- `start` — align to the start edge
- `end` — align to the end edge
- `left` — align to the left
- `right` — align to the right
- `stretch` — stretch items to fill
- `inherit` — inherits from parent
- `initial` — sets to default (flex-start)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center content horizontally
- Spread items evenly across a row

**Example:**
```css
.nav {
  display: flex;
  justify-content: space-between;
}

.centered {
  display: flex;
  justify-content: center;
}
```

---

## align-items

**Syntax:** `align-items: flex-start | flex-end | center | baseline | stretch | start | end | self-start | self-end`

Cross axis alignment — aligns items along the cross axis.

**Values:**
- `stretch` — stretch to fill container (default)
- `flex-start` — items at start
- `flex-end` — items at end
- `center` — items centered
- `baseline` — aligned by text baseline
- `start` — align to the start edge
- `end` — align to the end edge
- `self-start` — align to own start edge
- `self-end` — align to own end edge
- `inherit` — inherits from parent
- `initial` — sets to default (stretch)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center items vertically
- Align items to the bottom of a container

**Example:**
```css
.centered {
  display: flex;
  align-items: center;
}

.bottom {
  display: flex;
  align-items: flex-end;
}
```

---

## align-content

**Syntax:** `align-content: flex-start | flex-end | center | space-between | space-around | space-evenly | stretch | start | end`

Multi-line alignment — aligns packed lines in a multi-line flex container.

**Values:**
- `stretch` — stretch lines to fill (default)
- `flex-start` — lines at start
- `flex-end` — lines at end
- `center` — lines centered
- `space-between` — space between lines
- `space-around` — space around lines
- `space-evenly` — equal space between lines
- `start` — align to the start edge
- `end` — align to the end edge
- `inherit` — inherits from parent
- `initial` — sets to default (stretch)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center wrapped content vertically
- Space out multiple rows evenly

**Example:**
```css
.wrapped {
  display: flex;
  flex-wrap: wrap;
  align-content: center;
}
```

---

## gap

**Syntax:** `gap: <length> | <percentage>`

Spacing between items — sets the gutter between flex items.

**Values:**
- `0` — no gap (default)
- `10px` — fixed gap
- `1rem` — rem-based gap
- `5%` — percentage gap
- `10px 20px` — row-gap column-gap
- `1rem 2rem` — rem-based row/column gap
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create consistent spacing between items
- Replace margins on flex children

**Example:**
```css
.toolbar {
  display: flex;
  gap: 1rem;
}
```

---

## Items

---

## order

**Syntax:** `order: <integer>`

Visual order — reorders flex items within the container.

**Values:**
- `0` — default order
- `1` — moved later
- `-1` — moved earlier
- `10` — moved much later
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Reorder items for responsive layouts
- Put key content first visually

**Example:**
```css
.sidebar {
  order: -1;
}

.main {
  order: 0;
}
```

---

## flex-grow

**Syntax:** `flex-grow: <number>`

Growth factor — how much an item grows relative to siblings.

**Values:**
- `0` — don't grow (default)
- `1` — grow equally
- `2` — grow twice as much
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Make one item fill remaining space
- Create proportional columns

**Example:**
```css
.main {
  flex-grow: 1;
}

.sidebar {
  flex-grow: 0;
}
```

---

## flex-shrink

**Syntax:** `flex-shrink: <number>`

Shrink factor — how much an item shrinks when space is limited.

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
- Control which items compress first

**Example:**
```css
.logo {
  flex-shrink: 0;
}

.title {
  flex-shrink: 1;
}
```

---

## flex-basis

**Syntax:** `flex-basis: <length> | <percentage> | auto | content`

Initial main-axis size — starting size before growing/shrinking.

**Values:**
- `auto` — use width/height (default)
- `content` — intrinsic content size
- `0` — zero initial size
- `100px` — fixed length
- `10em` — em-based length
- `50%` — percentage of container
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Set initial size before growth
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

Shorthand — combines grow, shrink, and basis in one declaration.

**Values:**
- `auto` — grow and shrink by 1, basis auto
- `initial` — don't grow, shrink, auto basis (default)
- `none` — fully inflexible
- `1` — grow equally, shrink equally, basis 0
- `0 1 auto` — don't grow, shrink, auto basis
- `1 0 0%` — grow, don't shrink, zero basis
- `inherit` — inherits from parent
- `initial` — sets to default (0 1 auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Simplify flex item declarations
- Create fixed and flexible columns

**Example:**
```css
.sidebar {
  flex: 0 0 200px;
}

.main {
  flex: 1 0 0%;
}
```

---

## align-self

**Syntax:** `align-self: auto | flex-start | flex-end | center | baseline | stretch | start | end | self-start | self-end`

Self alignment — overrides align-items for a single flex item.

**Values:**
- `auto` — follow container's align-items (default)
- `flex-start` — align to start
- `flex-end` — align to end
- `center` — centered
- `baseline` — align by text baseline
- `stretch` — stretch to fill
- `start` — align to the start edge
- `end` — align to the end edge
- `self-start` — align to own start edge
- `self-end` — align to own end edge
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Override alignment for a single item
- Align individual elements differently

**Example:**
```css
.item-center {
  align-self: center;
}

.item-end {
  align-self: flex-end;
}
```

---

## place-items

**Syntax:** `place-items: <align-items> <justify-items>`

Placement shorthand — sets align-items and justify-items together.

**Values:**
- `center` — centered on both axes
- `stretch` — stretched on both axes (default)
- `center stretch` — center vertically, stretch horizontally
- `inherit` — inherits from parent
- `initial` — sets to default (stretch)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center content in one declaration
- Combine cross and inline alignment

**Example:**
```css
.centered {
  display: flex;
  place-items: center;
}
```

---

**[View Example](../examples/intermediate/11-flexbox-advanced/index.html)**

← **Previous Topic:** [Background Advanced](../intermediate/10-background-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Grid Advanced](../intermediate/12-grid-advanced.md) →

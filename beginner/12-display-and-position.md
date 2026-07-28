# Display & Position

> 10 properties

Controls how elements are rendered and positioned in the document flow.

---

## Display

---

## display

**Syntax:** `display: inline | block | flex | grid | none | inline-block | inline-flex | inline-grid | contents | list-item | table`

Specifies rendering type — block, inline, flex, grid, or none for layout control.

**Values:**
- `inline` — element flows within text
- `block` — element takes full width
- `flex` — block-level flex container
- `grid` — block-level grid container
- `none` — element is removed from layout
- `inline-block` — inline with block-level sizing
- `inline-flex` — inline-level flex container
- `inline-grid` — inline-level grid container
- `contents` — element box is omitted, children inherit
- `list-item` — element displays as list item
- `table` — element behaves as `<table>`
- `inherit` — inherits from parent
- `initial` — sets to default (inline)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create flex or grid containers for modern layouts
- Hide elements without removing from DOM

**Example:**
```css
.container {
  display: flex;
  gap: 8px;
}
```

---

## visibility

**Syntax:** `visibility: visible | hidden | collapse`

Controls element visibility — hidden elements still occupy space in the layout.

**Values:**
- `visible` — element is visible (default)
- `hidden` — element is invisible but keeps space
- `collapse` — collapses table rows/columns
- `inherit` — inherits from parent
- `initial` — sets to default (visible)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Hide elements while preserving layout space
- Show/hide elements on hover for interactive effects

**Example:**
```css
.hidden {
  visibility: hidden;
}
```

---

## overflow

**Syntax:** `overflow: visible | hidden | scroll | auto | clip`

Handles content overflow — clip, scroll, or allow content to spill outside the box.

**Values:**
- `visible` — overflow is visible (default)
- `hidden` — overflow is clipped
- `clip` — overflow is clipped without scroll
- `scroll` — always shows scrollbars
- `auto` — shows scrollbars when needed
- `hidden auto` — horizontal hidden, vertical auto
- `inherit` — inherits from parent
- `initial` — sets to default (visible)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Clip long text in cards or buttons
- Create scrollable containers

**Example:**
```css
.container {
  overflow: hidden;
  width: 140px;
  height: 70px;
}
```

---

## overflow-wrap

**Syntax:** `overflow-wrap: normal | break-word | anywhere`

Controls word wrapping — break long words to prevent horizontal overflow.

**Values:**
- `normal` — breaks only at allowed break points (default)
- `break-word` — breaks long words to prevent overflow
- `anywhere` — breaks at any character if needed
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Prevent long URLs or words from overflowing containers
- Wrap long text in narrow columns

**Example:**
```css
.text {
  overflow-wrap: break-word;
}
```

---

## Position

---

## position

**Syntax:** `position: static | relative | absolute | fixed | sticky`

Positions element relative to context — static, relative, absolute, fixed, or sticky.

**Values:**
- `static` — default, follows normal flow
- `relative` — positioned relative to its normal position
- `absolute` — positioned relative to nearest positioned ancestor
- `fixed` — positioned relative to viewport
- `sticky` — toggles between relative and fixed on scroll
- `inherit` — inherits from parent
- `initial` — sets to default (static)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create modals and overlays with `position: fixed`
- Build sticky navigation headers

**Example:**
```css
.parent {
  position: relative;
}

.child {
  position: absolute;
  top: 8px;
  right: 8px;
}
```

---

## top / right / bottom / left

**Syntax:** `top: <length> | <percentage> | auto`

Offsets from edges — pushes element from the edge of its positioning context.

**Values:**
- `auto` — no offset (default)
- `10px` — pixel offset
- `2em` — em-based offset
- `50%` — percentage of containing block
- `0` — flush with edge
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Position elements absolutely within a container
- Center elements with top/left 50% and transforms

**Example:**
```css
.element {
  position: absolute;
  top: 10px;
  left: 10px;
}
```

---

## z-index

**Syntax:** `z-index: <integer> | auto`

Controls stacking order — higher values appear in front of lower values on positioned elements.

**Values:**
- `auto` — default stacking order
- `1` — low stacking order
- `9999` — high stacking order
- `-1` — behind other elements
- `0` — base stacking level
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Layer overlapping elements in modals or dropdowns
- Bring elements in front of pseudo-elements

**Example:**
```css
.overlay {
  z-index: 10;
}

.content {
  z-index: 1;
}
```

---

## float

**Syntax:** `float: none | left | right | inline-start | inline-end`

Floats element to side — wraps text around floated elements in document flow.

**Values:**
- `none` — element is not floated (default)
- `left` — element floats to the left
- `right` — element floats to the right
- `inline-start` — floats to start of inline direction
- `inline-end` — floats to end of inline direction
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Wrap text around images in articles
- Create multi-column layouts (legacy)

**Example:**
```css
.image {
  float: left;
  margin-right: 10px;
}
```

---

## clear

**Syntax:** `clear: none | left | right | both | inline-start | inline-end`

Prevents float overlap — pushes element below floated elements on specified sides.

**Values:**
- `none` — allows floats on both sides (default)
- `left` — clears left floats
- `right` — clears right floats
- `both` — clears both left and right floats
- `inline-start` — clears start-side floats
- `inline-end` — clears end-side floats
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Prevent elements from wrapping around floats
- Clear floats after a floated sidebar

**Example:**
```css
.clearfix {
  clear: both;
}
```

---

**[View Example](../examples/beginner/12-display-and-position/index.html)**

← **Previous Topic:** [Lists & Tables Basics](../beginner/11-lists-and-tables-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Flexbox Basics](../beginner/13-flexbox-basics.md) →

# Display Basics

> 4 properties

Controls how elements are rendered in the document flow.

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

**[View Example](../examples/beginner/13-display-basics/index.html)**

← **Previous Topic:** [Tables Basics](../beginner/12-tables-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Positioning Basics](../beginner/14-positioning-basics.md) →


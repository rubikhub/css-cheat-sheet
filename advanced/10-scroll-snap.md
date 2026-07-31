# Scroll Snap & Touch Interaction

> 4 properties

Snap scrolling behavior and touch gesture control.

---

## scroll-snap-type

**Syntax:** `scroll-snap-type: none | [x | y | both] [mandatory | proximity]`

Defines how the browser should snap to scroll positions.

**Values:**
- `none` — no snapping (default)
- `x mandatory` — snap along x axis, always
- `y mandatory` — snap along y axis, always
- `x proximity` — snap along x axis when close
- `y proximity` — snap along y axis when close
- `both mandatory` — snap on both axes
- `both proximity` — snap on both axes when close
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create image carousels
- Build snap-scroll galleries

**Example:**
```css
.snap-container {
  scroll-snap-type: x mandatory;
  overflow-x: auto;
}
```

---

## scroll-snap-align

**Syntax:** `scroll-snap-align: none | start | end | center`

Sets the snap alignment point within the snap container.

**Values:**
- `none` — no snap alignment (default)
- `start` — align start edge to the container
- `end` — align end edge to the container
- `center` — center the item in the container
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center cards when snapping
- Align items to container edges

**Example:**
```css
.snap-container {
  display: flex;
  overflow-x: auto;
  scroll-snap-type: x mandatory;
}

.snap-item {
  min-width: 100%;
  scroll-snap-align: center;
}
```

---

## overscroll-behavior

**Syntax:** `overscroll-behavior: auto | contain | none`

Controls what happens when the scroll boundary is reached.

**Values:**
- `auto` — default overscroll chaining (default)
- `contain` — prevents scroll chaining to parent elements
- `none` — prevents any overscroll behavior
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Stop scroll chaining to the page
- Disable pull-to-refresh on modal scroll areas

**Example:**
```css
.modal-scroll {
  overscroll-behavior: contain;
}

.chat-list {
  overscroll-behavior: none;
}
```

---

## touch-action

**Syntax:** `touch-action: auto | none | pan-x | pan-y | pinch-zoom | manipulation`

Defines touch gestures allowed on the element.

**Values:**
- `auto` — browser determines allowed gestures (default)
- `none` — no touch gestures allowed
- `pan-x` — horizontal panning only
- `pan-y` — vertical panning only
- `pan-x pan-y` — panning in both directions
- `pinch-zoom` — allow pinch zooming
- `manipulation` — panning and pinch-zoom, disables double-tap zoom
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Enable custom touch gestures
- Prevent double-tap zoom on interactive elements

**Example:**
```css
.drag-handle {
  touch-action: none;
}

.button {
  touch-action: manipulation;
}
```

---

**[View Example](../examples/advanced/10-scroll-snap/index.html)**

← **Previous Topic:** [CSS Counters — Complex Patterns](../advanced/09-css-counters-complex.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [:has() — The Parent Selector](../advanced/11-has-selector.md) →

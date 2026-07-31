# Scroll Snap & Touch Interaction

> 9 properties

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

## scroll-start-target

**Syntax:** `scroll-start-target: auto | <element-id> | none`

Sets the initial scroll position of a scroll container.

**Values:**
- `auto` — scroll container decides the start position (default)
- `none` — no scroll-start target
- `#item-3` — start scrolled to that element

**Use Cases:**
- Open a carousel on a specific item
- Preserve scroll position across navigations

**Example:**
```css
.gallery {
  scroll-start-target: #item-3;
}
```

---

## scroll-initial-target

**Syntax:** `scroll-initial-target: auto | <element-id> | none`

Declares the default scroll target of a scroll container (used with scroll-target-group).

**Values:**
- `auto` — use the first focusable or scroll-start target
- `#item-5` — default target element
- `none` — no initial target

**Use Cases:**
- Pick the default item in a snap carousel
- Pair with :target-current for the selected state

**Example:**
```css
.gallery {
  scroll-initial-target: #item-5;
}
```

---

## ::scroll-marker & ::scroll-marker-group

**Syntax:** `::scroll-marker` | `::scroll-marker-group`

Carousel navigation markers shown in the scrollbar or a marker group.

**Values:**
- `::scroll-marker` — a marker for each scroll-snap item
- `::scroll-marker-group` — the container of the markers
- Works with `scroll-marker-group: after | before` on the container

**Use Cases:**
- Build dot indicators for carousels without JS
- Style the active marker with :target-current

**Example:**
```css
.gallery {
  scroll-marker-group: after;
}

.gallery::scroll-marker {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: #ccc;
}

.gallery::scroll-marker:target-current {
  background: #667eea;
}
```

---

## ::scroll-button() & ::selecteditem

**Syntax:** `::scroll-button(<direction>)` | `::selecteditem`

Navigation arrows and the selected item of a scrollable carousel.

**Values:**
- `::scroll-button(left)` — a left arrow
- `::scroll-button(right)` — a right arrow
- `::selecteditem` — the currently selected (target-current) item

**Use Cases:**
- Add prev/next arrows with pure CSS
- Style the active slide

**Example:**
```css
.gallery::scroll-button(left) {
  content: "‹";
}

.gallery::scroll-button(right) {
  content: "›";
}

.gallery::selecteditem {
  opacity: 1;
}
```

---

## scroll-target-group

**Syntax:** `scroll-target-group: <custom-ident> | none`

Names a group so :target-current can match items scrolled by different containers.

**Values:**
- `auto` — groups by the scroll container
- `--hero-carousel` — a custom named group
- `none` — no group (default)

**Use Cases:**
- Sync selection across multiple carousels
- Group scroll containers that share a selection state

**Example:**
```css
.gallery {
  scroll-target-group: --gallery;
}

.gallery-item:target-current {
  border-color: #667eea;
}
```

---

**[View Example](../examples/advanced/22-scroll-snap/index.html)**

← **Previous Topic:** [CSS Masks](../advanced/21-css-masks.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [CSS At-Rules — Advanced](../advanced/23-at-rules.md) →


# UI & Scroll

> 11 properties

Control cursor, selection, overflow, and scrollbar appearance.

---

## UI

---

## user-select

**Syntax:** `user-select: auto | none | text | all | contain`

User select — controls whether the user can select text.

**Values:**
- `auto` — default selection behavior (default)
- `none` — prevent text selection
- `text` — allow text selection
- `all` — select all content on click
- `contain` — selection stays within the element
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Prevent selecting UI labels
- Make code blocks select-all

**Example:**
```css
.label {
  user-select: none;
}

.code {
  user-select: all;
}
```

---

## scroll-behavior

**Syntax:** `scroll-behavior: auto | smooth`

Scroll behavior — defines smooth or instant scrolling.

**Values:**
- `auto` — instant jump (default)
- `smooth` — animated scrolling
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Smooth anchor navigation
- Smooth scrolling on long pages

**Example:**
```css
html {
  scroll-behavior: smooth;
}
```

---

## overflow

**Syntax:** `overflow: visible | hidden | clip | scroll | auto`

Overflow — specifies how content is handled when it overflows the element's box.

**Values:**
- `visible` — content overflows the box (default)
- `hidden` — clip overflowing content
- `clip` — clip without creating a scroll container
- `scroll` — always show scrollbars
- `auto` — show scrollbars when needed
- `inherit` — inherits from parent
- `initial` — sets to default (visible)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create scrollable areas
- Clip overflowing content in cards

**Example:**
```css
.scrollable {
  overflow: auto;
}

.card {
  overflow: hidden;
}
```

---

## scrollbar-width

**Syntax:** `scrollbar-width: auto | thin | none`

Scrollbar width — controls the scrollbar thickness.

**Values:**
- `auto` — default thickness (default)
- `thin` — thin scrollbar
- `none` — hide the scrollbar while keeping scrolling
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Slim down scrollbars in panels
- Hide scrollbars for carousels

**Example:**
```css
.panel {
  scrollbar-width: thin;
}
```

---

## scrollbar-color

**Syntax:** `scrollbar-color: auto | <thumb> <track>`

Scrollbar color — sets the thumb and track colors of the scrollbar.

**Values:**
- `auto` — default colors (default)
- `#888 #f1f1f1` — thumb and track colors
- `#333 transparent` — thumb with transparent track
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Match scrollbars to the theme
- Style dark-mode scrollbars

**Example:**
```css
.dark {
  scrollbar-color: #333 #e5e5e5;
}
```

---

## scrollbar-gutter

**Syntax:** `scrollbar-gutter: auto | stable | stable both-edges`

Reserves space for a scrollbar to prevent layout shift.

**Values:**
- `auto` — no reserved gutter (default)
- `stable` — reserve space for a classic scrollbar
- `stable both-edges` — reserve space on both sides

**Use Cases:**
- Prevent content shifting when scrollbars appear

**Example:**
```css
html {
  scrollbar-gutter: stable;
}
```

---

## scroll-padding

**Syntax:** `scroll-padding: <length-percentage> ...`

Defines the visible snap viewport inside the scroll container.

**Values:**
- `scroll-padding-top: 80px` — offset for fixed headers
- `scroll-padding: 1rem` — uniform padding
- `scroll-padding-block-start: 2rem` — logical property

**Use Cases:**
- Stop anchor jumps hiding under sticky headers

**Example:**
```css
html {
  scroll-padding-top: 72px;
}
```

---

## scroll-margin

**Syntax:** `scroll-margin: <length> ...`

Sets the offset applied to a scroll-snap or anchor target.

**Values:**
- `scroll-margin-top: 80px` — offset for a target
- `scroll-margin: 1rem` — uniform margin
- `scroll-margin-block: 2rem` — logical property

**Use Cases:**
- Give snap targets breathing room

**Example:**
```css
section {
  scroll-margin-top: 72px;
}
```

---

## resize

**Syntax:** `resize: none | both | horizontal | vertical`

Controls whether the user can resize an element.

**Values:**
- `none` — not resizable (default)
- `both` — resize in both axes
- `horizontal` / `vertical` — resize one axis only

**Use Cases:**
- Enable resizable panels and textareas

**Example:**
```css
textarea {
  resize: vertical;
}
```

---

## appearance

**Syntax:** `appearance: none | auto | <control>`

Controls the native styling of form controls.

**Values:**
- `none` — remove native control styling
- `auto` — native control appearance (default)
- `checkbox`, `radio`, `menulist-button` — restore specific controls

**Use Cases:**
- Build custom checkboxes and selects

**Example:**
```css
input[type='checkbox'] {
  appearance: none;
  width: 18px;
  height: 18px;
  border: 2px solid #888;
  border-radius: 4px;
}
```

---

## pointer-events

**Syntax:** `pointer-events: auto | none`

Controls whether an element can be the target of pointer events.

**Values:**
- `auto` — normal pointer behavior (default)
- `none` — element is invisible to the pointer
- SVG values — `visiblePainted`, `visibleFill`, `bounding-box`

**Use Cases:**
- Let clicks pass through overlays
- Disable interactions on locked content

**Example:**
```css
.overlay {
  pointer-events: none;
}

.close-button {
  pointer-events: auto;
}
```

---

**[View Example](../examples/intermediate/17-ui-and-scroll/index.html)**

← **Previous Topic:** [Filter & Clip Path](../intermediate/16-filter-and-clip-path.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Animation](../intermediate/18-animation.md) →

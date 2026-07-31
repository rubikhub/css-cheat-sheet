# UI & Scroll

> 17 properties

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

## field-sizing

**Syntax:** `field-sizing: fixed | content`

Controls whether form controls size to fixed or content dimensions.

**Values:**
- `fixed` — control keeps a fixed size (default)
- `content` — control grows/shrinks to fit its content

**Use Cases:**
- Auto-growing textareas
- Inputs that shrink to fit their value

**Example:**
```css
textarea {
  field-sizing: content;
  max-width: 300px;
}
```

---

## accent-color

**Syntax:** `accent-color: auto | <color>`

Sets the accent color for native form controls like checkboxes, radios, and range inputs.

**Values:**
- `auto` — use the browser default accent (default)
- `#667eea` — brand accent color
- `currentColor` — follow the text color

**Use Cases:**
- Theme checkboxes and radio buttons without rebuilding them
- Match range sliders to brand colors

**Example:**
```css
input {
  accent-color: #667eea;
}
```

---

## forced-color-adjust

**Syntax:** `forced-color-adjust: auto | none`

Controls whether an element's colors are adjusted in forced-colors mode.

**Values:**
- `auto` — browser may override colors in forced-colors mode (default)
- `none` — keep author colors in forced-colors mode

**Use Cases:**
- Preserve brand colors in Windows High Contrast mode
- Keep charts and maps readable under forced colors

**Example:**
```css
.logo {
  forced-color-adjust: none;
}
```

---

## zoom

**Syntax:** `zoom: normal | reset | <number> | <percentage>`

Scales an element and its layout (unlike transform: scale) as of the 2024 standardization.

**Values:**
- `normal` — no zoom (default)
- `1.5` — 150% scale
- `150%` — percentage scale
- `reset` — reset zoom to 1 for the subtree

**Use Cases:**
- Zoom widget content in and out
- Scale layout including dimensions and font sizes

**Example:**
```css
.dashboard {
  zoom: 1.25;
}

.reset {
  zoom: reset;
}
```

---

## overflow-clip-margin

**Syntax:** `overflow-clip-margin: <length>`

Sets how far content can overflow before being clipped when overflow: clip is used.

**Values:**
- `0px` — clip at the padding box edge (default)
- `20px` — let content overflow 20px before clipping
- `content-box` — clip relative to the content box

**Use Cases:**
- Let box shadows and drop-shadows show beyond a clip
- Clip layout without cutting off visual effects

**Example:**
```css
.carousel {
  overflow: clip;
  overflow-clip-margin: 16px;
}
```

---

## empty-cells

**Syntax:** `empty-cells: show | hide`

Controls whether empty table cells render borders and backgrounds.

**Values:**
- `show` — render empty cells (default)
- `hide` — hide empty cells

**Use Cases:**
- Remove borders from blank table cells
- Keep calendars and grids visually clean

**Example:**
```css
table {
  empty-cells: hide;
}
```

---

**[View Example](../examples/intermediate/23-ui-and-scroll/index.html)**

← **Previous Topic:** [Filter & Clip Path](../intermediate/22-filter-and-clip-path.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Animation](../intermediate/24-animation.md) →


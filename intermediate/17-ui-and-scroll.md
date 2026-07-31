# UI & Scroll

> 5 properties

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

**[View Example](../examples/intermediate/17-ui-and-scroll/index.html)**

← **Previous Topic:** [Typography Advanced](../intermediate/16-typography-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Animation](../intermediate/18-animation.md) →

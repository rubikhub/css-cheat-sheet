# Scrollbar Styling

> 2 properties

Customize scrollbar appearance and width.

---

## scrollbar-color

**Syntax:** `scrollbar-color: <thumb-color> <track-color> | auto`

Sets the track and thumb colors of the scrollbar.

**Values:**
- `auto` — browser default colors (default)
- `#888 #f1f1f1` — thumb then track color
- `#333 transparent` — visible thumb, transparent track
- `currentColor transparent` — thumb matches text color
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Match the scrollbar to a theme
- Customize scrollbar colors for dark mode

**Example:**
```css
.custom-scrollbar {
  overflow-y: scroll;
  scrollbar-color: #888 #f1f1f1;
}
```

---

## scrollbar-width

**Syntax:** `scrollbar-width: auto | thin | none`

Controls the thickness of the scrollbar.

**Values:**
- `auto` — default scrollbar width (default)
- `thin` — narrow scrollbar
- `none` — hides the scrollbar while keeping scroll
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Slim down scrollbars for a cleaner look
- Hide scrollbars without disabling scrolling

**Example:**
```css
.custom-scrollbar {
  height: 200px;
  overflow-y: scroll;
  scrollbar-width: thin;
}
```

---

**[View Example](../examples/advanced/17-scrollbar-styling/index.html)**

← **Previous Topic:** [View Transitions](../advanced/16-view-transitions.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [3D Transforms](../advanced/18-3d-transforms.md) →


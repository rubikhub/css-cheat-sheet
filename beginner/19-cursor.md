# Cursor

> 1 property

Controls the mouse cursor appearance.

---

## cursor

**Syntax:** `cursor: <keyword> | <url>`

Mouse pointer style — changes cursor on hover.

**Values:**
- `default` — default arrow (default)
- `pointer` — hand pointer (links)
- `text` — text selection cursor
- `wait` — busy/loading
- `help` — help available
- `move` — move/drag
- `not-allowed` — prohibited action
- `grab` — grabbable element
- `grabbing` — currently grabbing
- `crosshair` — precision selection
- `zoom-in` — zoom in
- `zoom-out` — zoom out
- `col-resize` — horizontal resize
- `row-resize` — vertical resize
- `none` — invisible cursor
- `url('custom.png'), auto` — custom image
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Indicate clickable elements
- Show loading states
- Provide resize handles

**Example:**
```css
a, button {
  cursor: pointer;
}

.disabled {
  cursor: not-allowed;
}

.draggable {
  cursor: grab;
}

.loading {
  cursor: wait;
}
```
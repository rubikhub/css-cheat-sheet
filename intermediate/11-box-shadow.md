# Box Shadows

> 2 properties

Drop shadows and inset shadows for depth and elevation.

---

## box-shadow

**Syntax:** `box-shadow: none | <offset-x> <offset-y> <blur> <spread> <color>`

Drop shadow — adds one or more shadows behind the element.

**Values:**
- `0 4px 6px rgba(108, 92, 231, 0.4)` — single shadow
- `0 4px 6px rgba(108, 92, 231, 0.4), 0 12px 24px rgba(108, 92, 231, 0.2)` — layered shadows
- `none` — no shadow (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create depth and elevation
- Add soft shadows to cards

**Example:**
```css
.card {
  box-shadow: 0 4px 6px rgba(108, 92, 231, 0.4);
}
```

---

## box-shadow: inset

**Syntax:** `box-shadow: inset <offset-x> <offset-y> <blur> <spread> <color>`

Inset shadows — appear inside the element's border.

**Values:**
- `inset 0 2px 8px rgba(0, 0, 0, 0.6)` — inner shadow
- `inset 0 2px 8px rgba(0, 0, 0, 0.6), 0 4px 12px rgba(0, 0, 0, 0.3)` — inner and outer shadows combined
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create pressed-in button effects
- Add depth to wells and panels

**Example:**
```css
.well {
  box-shadow: inset 0 2px 8px rgba(0, 0, 0, 0.6);
}
```

---

**[View Example](../examples/intermediate/11-box-shadow/index.html)**

← **Previous Topic:** [Border Radius](../intermediate/10-border-radius.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Counters & Markers](../intermediate/12-counters-and-markers.md) →


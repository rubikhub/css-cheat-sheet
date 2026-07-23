# Opacity

> 1 property

Controls the transparency of elements.

---

## opacity

**Syntax:** `opacity: <number>`

Transparency level — 0 (invisible) to 1 (opaque).

**Values:**
- `1` — fully opaque (default)
- `0` — fully transparent (invisible)
- `0.5` — 50% transparent
- `0.25` — 75% transparent
- `0.75` — 25% transparent
- `inherit` — inherits from parent
- `initial` — sets to default (1)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Fade elements on hover
- Create disabled state appearances
- Add subtle transparency effects

**Example:**
```css
.disabled {
  opacity: 0.5;
}

.card:hover {
  opacity: 0.9;
}

.overlay {
  background: rgba(0, 0, 0, 0.5);
  opacity: 0.8;
}
```
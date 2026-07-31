# Motion Path

> 5 properties

Move elements along a defined path — useful for animation and creative layouts.

---

## offset-path

**Syntax:** `offset-path: none | <basic-shape> | path(<string>)`

Defines the path an element travels along.

**Values:**
- `none` — no motion path (default)
- `path('M 0 0 L 100 100')` — SVG path data
- `circle(50px at 50% 50%)` — circular path
- `polygon(0 0, 100% 0, 100% 100%)` — polygonal path
- `ray(<angle>)` — a straight ray at an angle

**Use Cases:**
- Animate objects along a curve
- Position decorative elements on a path

**Example:**
```css
.rocket {
  offset-path: path('M 50 300 C 150 100 350 100 450 300');
}
```

---

## offset-distance

**Syntax:** `offset-distance: <length-percentage>`

How far along the path the element is placed.

**Values:**
- `0%` — at the start of the path
- `100%` — at the end of the path
- `offset-distance: 40px` — a fixed distance along the path

**Use Cases:**
- Animate travel along the path with transitions
- Pin an element at a point on the path

**Example:**
```css
.rocket {
  offset-path: path('M 50 300 C 150 100 350 100 450 300');
  animation: fly 4s linear infinite;
}

@keyframes fly {
  from { offset-distance: 0%; }
  to { offset-distance: 100%; }
}
```

---

## offset-rotate

**Syntax:** `offset-rotate: auto | reverse | <angle>`

Controls how the element rotates as it moves along the path.

**Values:**
- `auto` — rotate to follow the path direction (default)
- `reverse` — follow the path opposite to its direction
- `offset-rotate: 0deg` — keep a fixed orientation
- `auto 45deg` — path direction plus a fixed offset angle

**Use Cases:**
- Keep labels upright while moving
- Tilt elements to match the path curvature

**Example:**
```css
.dot {
  offset-rotate: 0deg;
}

.arrow {
  offset-rotate: auto;
}
```

---

## offset-anchor

**Syntax:** `offset-anchor: auto | <position>`

The point on the element that is aligned to the path.

**Values:**
- `auto` — aligns the element's center (default)
- `offset-anchor: top left` — use the top-left corner
- `offset-anchor: 50% 100%` — percentage-based anchor

**Use Cases:**
- Pin a specific corner to the path
- Align text baselines with a path

**Example:**
```css
.pin {
  offset-path: circle(60px at center);
  offset-anchor: top left;
}
```

---

## offset

**Syntax:** `offset: <offset-position> || <offset-path> || <offset-distance> || <offset-rotate> || <offset-anchor>`

Shorthand for all motion path properties.

**Values:**
- `offset: path('M 0 0 L 100 100') 50%` — path with distance
- `offset: circle(80px at 50% 50%) 0deg` — path with rotation
- `offset: auto` — resets all offset properties

**Use Cases:**
- Define a full motion path in one declaration
- Reset motion path settings quickly

**Example:**
```css
.badge {
  offset: path('M 50 300 C 150 100 350 100 450 300') 0% auto;
}
```

---

**[View Example](../examples/advanced/30-motion-path/index.html)**

← **Previous Topic:** [Multi-column Layout](../advanced/29-multi-column-layout.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Paged Media & Print](../advanced/31-paged-media.md) →


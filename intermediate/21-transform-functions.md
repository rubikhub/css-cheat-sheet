# Transform Functions

> 6 features

Transform functions — move, rotate, resize, skew, and add depth to elements.

---

## Functions

---

## translate()

**Syntax:** `translate(<x>, <y>)`

Moves an element from its current position.

**Values:**
- `translate(100px, 50px)` — moves 100px right and 50px down
- `translate(100px)` — moves on the X axis only
- `translateX(100px)` — moves horizontally
- `translateY(50px)` — moves vertically
- `translate(50%, 50%)` — percentage-based move
- `translate3d(100px, 50px, 200px)` — 3D move
- `translateZ(200px)` — moves toward or away from the viewer

**Use Cases:**
- Position elements without affecting layout
- Animate elements sliding in

**Example:**
```css
.card:hover {
  transform: translateY(-10px);
}

.badge {
  transform: translate(50%, 50%);
}
```

---

## rotate()

**Syntax:** `rotate(<angle>)`

Rotates an element clockwise or counter-clockwise.

**Values:**
- `rotate(45deg)` — rotates 45 degrees clockwise
- `rotate(-45deg)` — rotates counter-clockwise
- `rotate(0.5turn)` — half turn
- `rotate(3.14rad)` — angle in radians
- `rotateX(45deg)` — rotates around the X axis
- `rotateY(45deg)` — rotates around the Y axis
- `rotateZ(45deg)` — rotates around the Z axis
- `rotate3d(1, 1, 1, 45deg)` — rotates around a 3D axis

**Use Cases:**
- Tilt elements for visual flair
- Build spinner and loader animations

**Example:**
```css
.icon:hover {
  transform: rotate(45deg);
}

.badge {
  transform: rotate(-45deg);
}
```

---

## scale()

**Syntax:** `scale(<x>, <y>)`

Resizes an element.

**Values:**
- `scale(2)` — doubles the size
- `scale(0.5)` — halves the size
- `scale(2, 0.5)` — different X and Y factors
- `scaleX(2)` — scales horizontally
- `scaleY(0.5)` — scales vertically
- `scale3d(1, 1, 2)` — 3D scale
- `scaleZ(2)` — scales along the Z axis

**Use Cases:**
- Enlarge elements on hover
- Create zoom effects

**Example:**
```css
.card:hover {
  transform: scale(1.05);
}

.button:active {
  transform: scale(0.95);
}
```

---

## skew()

**Syntax:** `skew(<x-angle>, <y-angle>)`

Skews an element on the X and Y axes.

**Values:**
- `skew(20deg)` — skews on the X axis
- `skew(20deg, -10deg)` — skews on both axes
- `skewX(20deg)` — skews horizontally
- `skewY(-10deg)` — skews vertically

**Use Cases:**
- Create angled or distorted elements
- Make ribbon or parallax effects

**Example:**
```css
.ribbon {
  transform: skewX(-20deg);
}

.ribbon span {
  transform: skewX(20deg);
}
```

---

## perspective()

**Syntax:** `perspective(<length>)`

Defines a perspective view for 3D transforms on the element itself.

**Values:**
- `perspective(200px) rotateY(45deg)` — strong depth
- `perspective(500px) rotateX(30deg)` — moderate depth
- `perspective(1000px) rotateY(-20deg) translateZ(100px)` — combined with other transforms

**Use Cases:**
- Add depth to individual 3D transforms
- Create card flip effects without a parent stage

**Example:**
```css
.card {
  transform: perspective(500px) rotateY(45deg);
}
```

---

## Individual transform properties

**Syntax:** `translate: <length-percentage> ...` | `rotate: <angle> ...` | `scale: <number> ...`

Standalone properties for translating, rotating, and scaling — independent of the transform property.

**Values:**
- `translate: 50% 20px` — move the element
- `rotate: 45deg` — rotate the element
- `scale: 1.5` — scale the element
- Apply in the order translate, rotate, scale

**Use Cases:**
- Animate one transform axis independently
- Separate transform concerns in components

**Example:**
```css
.card {
  translate: 0 -4px;
  rotate: 2deg;
  scale: 1.05;
}
```

---

**[View Example](../examples/intermediate/21-transform-functions/index.html)**

← **Previous Topic:** [Transform](../intermediate/20-transform.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Filter & Clip Path](../intermediate/22-filter-and-clip-path.md) →


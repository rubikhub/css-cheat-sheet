# Filter & Clip Path

> 2 properties

Graphical effects — filters for image manipulation and clip paths for custom shapes.

---

## Effects

---

## filter

**Syntax:** `filter: none | <filter-function>*`

Applies graphical effects like blur, brightness, and contrast to an element.

**Values:**
- `none` — no filter
- `blur(5px)` — gaussian blur
- `brightness(1.5)` — brightness multiplier
- `contrast(200%)` — contrast adjustment
- `grayscale(100%)` — removes color
- `hue-rotate(90deg)` — rotates the hue
- `invert(100%)` — inverts colors
- `opacity(50%)` — opacity level
- `saturate(200%)` — color saturation
- `sepia(100%)` — sepia tone
- `drop-shadow(2px 2px 4px rgba(0, 0, 0, 0.3))` — shadow following the element shape
- `url("filter.svg")` — SVG filter reference
- `blur(2px) brightness(1.2)` — multiple filters combined
- `grayscale(50%) contrast(1.5) brightness(1.1)` — combined photo effect
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Blur modals or backgrounds
- Create grayscale hover effects
- Add shadows to transparent images

**Example:**
```css
.modal-backdrop {
  filter: blur(4px);
}

img:hover {
  filter: grayscale(100%) contrast(1.2);
}
```

---

## clip-path

**Syntax:** `clip-path: <basic-shape> | path(<string>) | url(<url>) | none`

Defines a visible region of an element using shapes.

**Values:**
- `none` — no clipping
- `circle(50%)` — circle clip
- `circle(30% at 50% 50%)` — circle positioned with at
- `ellipse(50% 30% at 50% 50%)` — ellipse clip
- `inset(10px 20px 30px 40px round 10px)` — inset rectangle with rounded corners
- `polygon(50% 0%, 100% 100%, 0% 100%)` — triangle
- `polygon(0% 0%, 100% 0%, 100% 100%, 0% 100%)` — rectangle
- `polygon(50% 0%, 61% 35%, 98% 35%, 68% 57%, 79% 91%, 50% 70%, 21% 91%, 32% 57%, 2% 35%, 39% 35%)` — star polygon
- `path("M 0 0 L 100 0 L 100 100 L 0 100 Z")` — SVG path
- `url("clip.svg")` — SVG clip reference
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create triangular or polygonal shapes
- Mask images into circles
- Build star or decorative silhouettes

**Example:**
```css
.avatar {
  clip-path: circle(50%);
}

.badge {
  clip-path: polygon(50% 0%, 100% 100%, 0% 100%);
}
```

---

**[View Example](../examples/intermediate/16-filter-and-clip-path/index.html)**

← **Previous Topic:** [Transform Functions](../intermediate/15-transform-functions.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [UI & Scroll](../intermediate/17-ui-and-scroll.md) →

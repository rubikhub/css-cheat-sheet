# Transform

> 6 properties

2D/3D transforms and perspective — movement, rotation, scaling, and depth.

---

## Properties

---

## transform

**Syntax:** `transform: <transform-list> | none`

Transform — applies 2D or 3D transformations to an element.

**Values:**
- `none` — no transform (default)
- `rotate(45deg)` — rotates the element
- `scale(2)` — resizes the element
- `skew(20deg)` — skews the element
- `translate(100px, 50px)` — moves the element
- `perspective(500px) rotateX(45deg)` — 3D rotation with perspective
- `rotate(45deg) scale(1.5)` — multiple transforms combined
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Animate position, scale, or rotation
- Create depth with 3D transforms

**Example:**
```css
.card:hover {
  transform: translateY(-4px) scale(1.02);
}

.flip {
  transform: perspective(500px) rotateY(45deg);
}
```

---

## transform-origin

**Syntax:** `transform-origin: <position>`

Origin — sets the point around which transforms are applied.

**Values:**
- `center` — center of the element (default)
- `top left` — top-left corner
- `bottom right` — bottom-right corner
- `100px 50px` — fixed offset point
- `50% 50%` — percentage point
- `50% 50% 100px` — 3D origin with z-offset
- `inherit` — inherits from parent
- `initial` — sets to default (50% 50% 0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Rotate elements around a specific point
- Flip cards from their edge

**Example:**
```css
.card {
  transform: rotate(45deg);
  transform-origin: top left;
}
```

---

## transform-box

**Syntax:** `transform-box: content-box | border-box | fill-box | stroke-box | view-box`

Box — defines the reference box for transform-origin.

**Values:**
- `content-box` — content box as reference
- `border-box` — border box as reference (default)
- `fill-box` — object bounding box as reference
- `stroke-box` — stroke bounding box as reference
- `view-box` — nearest viewport as reference
- `inherit` — inherits from parent
- `initial` — sets to default (border-box)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Control transform origin on SVG elements
- Align transforms to the content area

**Example:**
```css
.icon {
  transform-box: fill-box;
  transform-origin: center;
}
```

---

## perspective

**Syntax:** `perspective: none | <length>`

Perspective — sets the distance from the viewer to the z=0 plane for children.

**Values:**
- `none` — no perspective (default)
- `200px` — strong perspective
- `500px` — moderate perspective
- `1000px` — subtle perspective
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Give 3D transforms depth
- Create card flip and carousel effects

**Example:**
```css
.stage {
  perspective: 500px;
}

.card {
  transform: rotateY(45deg);
}
```

---

## perspective-origin

**Syntax:** `perspective-origin: <position>`

Perspective origin — sets the vanishing point for perspective.

**Values:**
- `50% 50%` — center vanishing point (default)
- `0 0` — top-left vanishing point
- `100% 100%` — bottom-right vanishing point
- `center top` — keyword position
- `200px 100px` — fixed offset position
- `inherit` — inherits from parent
- `initial` — sets to default (50% 50%)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Shift where 3D scenes converge
- Fine-tune perspective in card stacks

**Example:**
```css
.stage {
  perspective: 500px;
  perspective-origin: center top;
}
```

---

## backface-visibility

**Syntax:** `backface-visibility: visible | hidden`

Back face — determines whether the back face is shown when an element is flipped.

**Values:**
- `visible` — back face shown (default)
- `hidden` — back face hidden
- `inherit` — inherits from parent
- `initial` — sets to default (visible)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Build card flip animations
- Hide the back of rotating elements

**Example:**
```css
.flip-card .back {
  backface-visibility: hidden;
  transform: rotateY(180deg);
}
```

---

**[View Example](../examples/intermediate/20-transform/index.html)**

← **Previous Topic:** [Transition Advanced](../intermediate/19-transition-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Transform Functions](../intermediate/21-transform-functions.md) →


# 3D Transforms

> 3 properties

Properties for creating three-dimensional visual effects.

---

## transform-style

**Syntax:** `transform-style: flat | preserve-3d`

Controls whether child elements are positioned in 3D space or flattened.

**Values:**
- `flat` — children flattened onto the element's plane (default)
- `preserve-3d` — children kept in 3D space
- `inherit` — inherits from parent
- `initial` — sets to default (flat)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Build 3D cubes and card stacks
- Enable nested 3D transforms

**Example:**
```css
.scene {
  perspective: 500px;
}

.cube {
  transform-style: preserve-3d;
  transform: rotateX(45deg);
}
```

---

## perspective

**Syntax:** `perspective: <length> | none`

Sets the distance from the viewer for 3D transformed children.

**Values:**
- `none` — no perspective (default)
- `500px` — short distance, strong depth
- `1000px` — long distance, subtle depth
- `20em` — relative length distance
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add depth to 3D scenes
- Create card flip and tilt effects

**Example:**
```css
.scene {
  perspective: 500px;
}
```

---

## backface-visibility

**Syntax:** `backface-visibility: visible | hidden`

Determines if the back face of an element is visible when rotated.

**Values:**
- `visible` — back face visible (default)
- `hidden` — back face hidden
- `inherit` — inherits from parent
- `initial` — sets to default (visible)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Build card flip animations
- Hide the reverse faces of 3D elements

**Example:**
```css
.card {
  backface-visibility: hidden;
  transform: rotateY(180deg);
}
```

---

**[View Example](../examples/advanced/15-3d-transforms/index.html)**

← **Previous Topic:** [Scrollbar Styling](../advanced/14-scrollbar-styling.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Animation — Direction, Fill Mode & Play State](../advanced/16-animation-fill-and-play-state.md) →

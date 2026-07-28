# 3D Transforms

Properties for creating three-dimensional visual effects.

---

## transform-style
**Type:** keyword | **Initial:** flat

Controls whether child elements are positioned in 3D space or flattened.

```css
transform-style: flat;
transform-style: preserve-3d;

/* Global values */
transform-style: inherit;
transform-style: initial;
```

```html
<div class="scene">
  <div class="cube">
    <div class="face front">Front</div>
    <div class="face back">Back</div>
  </div>
</div>
```

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
**Type:** length | **Initial:** none

Sets the distance from the viewer for 3D transformed children.

```css
perspective: none;
perspective: 500px;
perspective: 1000px;
perspective: 20em;

/* Global values */
perspective: inherit;
perspective: initial;
```

---

## backface-visibility
**Type:** keyword | **Initial:** visible

Determines if the back face of an element is visible when rotated.

```css
backface-visibility: visible;
backface-visibility: hidden;

/* Global values */
backface-visibility: inherit;
backface-visibility: initial;
```

```css
.card {
  backface-visibility: hidden;
  transform: rotateY(180deg);
}
```


---

[Example](../examples/advanced/06-3d-transforms/index.html)

← **Previous Topic:** [Subgrid & Named Grid Lines](../advanced/05-subgrid.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Animation — Direction, Fill Mode & Play State](../advanced/07-animation-fill-and-play-state.md) →

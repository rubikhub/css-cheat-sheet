# Scroll Snap & Touch Interaction

Snap scrolling behavior and touch gesture control.

---

## scroll-snap-type
**Type:** keyword | **Initial:** none

Defines how the browser should snap to scroll positions.

```css
scroll-snap-type: none;
scroll-snap-type: x mandatory;
scroll-snap-type: y mandatory;
scroll-snap-type: x proximity;
scroll-snap-type: y proximity;
scroll-snap-type: both mandatory;
scroll-snap-type: both proximity;

/* Global values */
scroll-snap-type: inherit;
scroll-snap-type: initial;
```

---

## scroll-snap-align
**Type:** keyword | **Initial:** none

Sets the snap alignment point within the snap container.

```css
scroll-snap-align: none;
scroll-snap-align: start;
scroll-snap-align: end;
scroll-snap-align: center;

/* Global values */
scroll-snap-align: inherit;
scroll-snap-align: initial;
```

```html
<div class="snap-container">
  <div class="snap-item">1</div>
  <div class="snap-item">2</div>
  <div class="snap-item">3</div>
</div>
```

```css
.snap-container {
  display: flex;
  overflow-x: auto;
  scroll-snap-type: x mandatory;
  gap: 1rem;
}

.snap-item {
  min-width: 100%;
  scroll-snap-align: center;
}
```

---

## overscroll-behavior
**Type:** keyword | **Initial:** auto

Controls what happens when the scroll boundary is reached.

```css
overscroll-behavior: auto;
overscroll-behavior: contain;
overscroll-behavior: none;

/* Global values */
overscroll-behavior: inherit;
overscroll-behavior: initial;
```

- **contain** — Prevents scroll chaining to parent elements
- **none** — Prevents any overscroll behavior

---

## touch-action
**Type:** keyword | **Initial:** auto

Defines touch gestures allowed on the element.

```css
touch-action: auto;
touch-action: none;
touch-action: pan-x;
touch-action: pan-y;
touch-action: pan-x pan-y;
touch-action: pinch-zoom;
touch-action: manipulation;

/* Global values */
touch-action: inherit;
touch-action: initial;
```

- **manipulation** — Enables panning and pinch-zoom (disables double-tap zoom)


---

[Example](../examples/advanced/10-scroll-snap/index.html)

← **Previous Topic:** [CSS Counters — Complex Patterns](../advanced/09-css-counters-complex.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [:has() — The Parent Selector](../advanced/11-has-selector.md) →

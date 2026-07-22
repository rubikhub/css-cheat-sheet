# Box Model

Everything in CSS is a box. The box model describes how these boxes are sized, spaced, and layered.

> Source: [web.dev/learn/css/box-model](https://web.dev/learn/css/box-model)

---

## The Four Areas

Every element is made up of four concentric areas:

```
+------------------------------------------+
|               MARGIN BOX                 |
|  +------------------------------------+  |
|  |           BORDER BOX               |  |
|  |  +------------------------------+  |  |
|  |  |        PADDING BOX           |  |  |
|  |  |  +------------------------+  |  |  |
|  |  |  |     CONTENT BOX        |  |  |  |
|  |  |  +------------------------+  |  |  |
|  |  +------------------------------+  |  |
|  +------------------------------------+  |
+------------------------------------------+
```

| Area | What It Is | Property |
|------|-----------|----------|
| **Content Box** | Where text and images appear | `width`, `height` |
| **Padding Box** | Space around content (inside border) | `padding` |
| **Border Box** | Wraps padding and content | `border` |
| **Margin Box** | Space outside the border | `margin` |

---

## content-box vs border-box

The `box-sizing` property controls how width/height are calculated.

### content-box (default)

```css
.my-box {
  box-sizing: content-box;
  width: 200px;
  padding: 20px;
  border: 10px solid;
}

/* Total width = 200 + 40 + 20 = 260px */
```

Width/height apply to the **content only**. Padding and border are added on top.

### border-box (recommended)

```css
.my-box {
  box-sizing: border-box;
  width: 200px;
  padding: 20px;
  border: 10px solid;
}

/* Total width = 200px (padding and border are included) */
```

Width/height apply to the **border box**. Padding and border are pushed inward.

### Common Reset

```css
*,
*::before,
*::after {
  box-sizing: border-box;
}
```

---

## The Four Properties

### width / height

Sets the size of the content box (in `content-box` mode).

```css
width: 200px;
width: 50%;
width: auto;         /* Default — fills available space */
width: min-content;  /* Smallest possible width */
width: max-content;  /* Largest possible width */
width: fit-content;  /* Fits content, maxes out at percentage */
```

### padding

Space between content and border.

```css
padding: 1rem;              /* All sides */
padding: 1rem 2rem;         /* Vertical | Horizontal */
padding: 1rem 2rem 1.5rem;  /* Top | Horizontal | Bottom */
padding: 10px 20px 15px 5px; /* Top | Right | Bottom | Left */

padding-top: 1rem;
padding-left: 2rem;
```

### border

A line around the padding box.

```css
border: 1px solid #333;
border-width: 2px;
border-style: solid;
border-color: blue;

/* Individual sides */
border-top: 1px solid red;
border-bottom: 2px dashed green;
```

### margin

Space outside the border. Pushes other elements away.

```css
margin: 1rem;              /* All sides */
margin: 1rem 2rem;         /* Vertical | Horizontal */
margin: 0 auto;            /* Center horizontally */
margin-top: 20px;

/* Negative margins pull elements closer */
margin-top: -10px;
```

---

## Overflow

When content is too big for its box, use `overflow` to control what happens.

```css
overflow: visible;  /* Default — content spills out */
overflow: hidden;   /* Clips the overflowing content */
overflow: scroll;   /* Always shows scrollbars */
overflow: auto;     /* Shows scrollbars only when needed */
overflow-x: auto;   /* Horizontal scroll only */
overflow-y: auto;   /* Vertical scroll only */
```

---

## Extrinsic vs Intrinsic Sizing

- **Extrinsic sizing** — You set the width/height explicitly (`width: 400px`). Content may overflow.
- **Intrinsic sizing** — The browser sizes the box based on content (`width: fit-content`, `width: min-content`).

```css
/* Extrinsic: fixed control */
.card {
  width: 400px;
  height: 300px;
}

/* Intrinsic: adapts to content */
.card {
  width: fit-content;
  min-width: 200px;
}
```

---

## Debugging the Box Model

In browser DevTools, select any element to see a visual diagram of its box model — showing exact values for margin, border, padding, and content dimensions.

---

## Summary

| Concept | Default | Recommendation |
|---------|---------|----------------|
| `box-sizing` | `content-box` | Use `border-box` globally |
| `overflow` | `visible` | Use `auto` or `hidden` when needed |
| `margin` | `0` | Use `0 auto` for centering |

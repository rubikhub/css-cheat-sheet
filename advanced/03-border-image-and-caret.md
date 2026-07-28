# Border Image & Caret Color

Advanced border styling with images and caret customization.

---

## border-image
**Type:** source | **Initial:** none

Uses an image as a border instead of a solid color.

```css
/* Basic usage */
border-image: url('border.png') 30 round;
border-image: url('border.svg') 30 stretch;
border-image: url('border.png') 30 fill;

/* Source */
border-image-source: url('border.png');
border-image-source: linear-gradient(to right, red, blue);

/* Slice */
border-image-slice: 30;
border-image-slice: 30 fill;
border-image-slice: 10 20 30 40;

/* Width */
border-image-width: 10px;
border-image-width: 20;

/* Outset */
border-image-outset: 0;
border-image-outset: 10px;

/* Repeat */
border-image-repeat: stretch;
border-image-repeat: repeat;
border-image-repeat: round;
border-image-repeat: space;

/* Global values */
border-image: inherit;
border-image: initial;
```

---

## caret-color
**Type:** color | **Initial:** auto

Sets the color of the text insertion caret in inputs and textareas.

```css
caret-color: auto;
caret-color: red;
caret-color: #333;
caret-color: currentColor;
caret-color: transparent;

/* Global values */
caret-color: inherit;
caret-color: initial;
```

```html
<input type="text" class="custom-caret" placeholder="Type here...">
```

```css
.custom-caret {
  caret-color: #ff6b6b;
  border: 2px solid #333;
  padding: 0.5rem;
  font-size: 1rem;
}
```


---

[Example](../examples/advanced/03-border-image-and-caret/index.html)

← **Previous Topic:** [Background Blend Mode](../advanced/02-background-blend-mode.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Scrollbar Styling](../advanced/04-scrollbar-styling.md) →

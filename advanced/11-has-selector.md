# :has() — The Parent Selector

Selects elements based on their children or sibling state.

---

## :has()
**Type:** pseudo-class

Selects an element if it contains a descendant matching the argument.

```css
/* Select card that has an image */
.card:has(img) {
  grid-template-rows: 200px 1fr;
}

/* Select form with invalid input */
form:has(:invalid) {
  border-color: red;
}

/* Select section that has an h2 */
section:has(h2) {
  padding-top: 2rem;
}

/* Select label next to checked checkbox */
label:has(+ input:checked) {
  color: green;
}

/* Select li that has a link */
li:has(a) {
  list-style: disc;
}

/* Select div that has both p and img */
div:has(p):has(img) {
  display: grid;
}
```

```html
<div class="card">
  <img src="photo.jpg" alt="Photo">
  <p>Description</p>
</div>

<div class="card">
  <p>Text only card</p>
</div>
```

```css
/* Card with image gets grid layout */
.card:has(img) {
  display: grid;
  grid-template-rows: 200px 1fr;
}

.card:has(img) img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}

/* Card without image stays simple */
.card:not(:has(img)) {
  padding: 1.5rem;
}
```

```css
/* Form validation styling */
form:has(:invalid) {
  border: 2px solid #e74c3c;
}

form:has(:valid) {
  border: 2px solid #2ecc71;
}

/* Highlight empty states */
.list:has(> :empty) {
  border: 1px dashed #ccc;
}
```

> **Note:** `:has()` is often called the "parent selector" — it selects upward or laterally, which was previously impossible in CSS.


---

[Example](../examples/advanced/11-has-selector/index.html)

← **Previous Topic:** [Scroll Snap & Touch Interaction](../advanced/10-scroll-snap.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Advanced State Pseudo-classes](../advanced/12-state-pseudo-classes-advanced.md) →

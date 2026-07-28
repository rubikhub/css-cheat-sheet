# Cutting-edge Pseudo-elements

Modern pseudo-elements for spelling, grammar, highlights, and view transitions.

---

## ::spelling-error
**Type:** pseudo-element

Selects text with a spelling error (browser-dependent).

```css
::spelling-error {
  text-decoration: wavy underline red;
  text-decoration-skip-ink: none;
}
```

---

## ::grammar-error
**Type:** pseudo-element

Selects text with a grammar error (browser-dependent).

```css
::grammar-error {
  text-decoration: wavy underline green;
}
```

---

## ::highlight()
**Type:** pseudo-element

Selects text within a named CSS Highlight.

```css
/* Define a highlight */
::highlight(my-highlight) {
  background: yellow;
  color: black;
}
```

```js
// JavaScript to create the highlight
const range = document.createRange();
range.selectNodeContents(document.querySelector('p'));
CSS.highlights.set('my-highlight', new Highlight(range));
```

---

## ::view-transition
**Type:** pseudo-element

The root pseudo-element wrapping the entire view transition.

```css
::view-transition {
  position: fixed;
  inset: 0;
}
```

---

## ::view-transition-group()
**Type:** pseudo-element

Targets a specific view transition group by name.

```css
::view-transition-group(hero) {
  animation-duration: 0.5s;
}

::view-transition-group(page) {
  animation-duration: 0.3s;
}
```

---

## ::view-transition-image-pair()
**Type:** pseudo-element

Targets the before/after image pair of a transition.

```css
::view-transition-image-pair(hero) {
  /* Style the old and new states */
}
```

---

## ::view-transition-old()
**Type:** pseudo-element

Targets the old (outgoing) state of a view transition.

```css
::view-transition-old(hero) {
  animation: fade-out 0.3s ease;
}

@keyframes fade-out {
  from { opacity: 1; }
  to { opacity: 0; }
}
```

---

## ::view-transition-new()
**Type:** pseudo-element

Targets the new (incoming) state of a view transition.

```css
::view-transition-new(hero) {
  animation: fade-in 0.3s ease;
}

@keyframes fade-in {
  from { opacity: 0; }
  to { opacity: 1; }
}
```

```html
<h1 class="hero-title">Page Title</h1>
```

```css
/* Enable view transitions */
@view-transition {
  navigation: auto;
}

/* Named transition for hero */
.hero-title {
  view-transition-name: hero;
}

::view-transition-old(hero) {
  animation: fade-out 0.3s ease;
}

::view-transition-new(hero) {
  animation: fade-in 0.3s ease;
}
```


---

[Example](../examples/advanced/14-pseudo-elements-cutting-edge/index.html)

← **Previous Topic:** [Form Pseudo-classes — Advanced](../advanced/13-form-pseudo-classes-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [CSS At-Rules — Advanced](../advanced/15-at-rules.md) →

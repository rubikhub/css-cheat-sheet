# Web Components & Shadow DOM

Styling inside Shadow DOM and component encapsulation.

---

## :host
**Type:** pseudo-class

Selects the shadow host element from within the shadow tree.

```css
/* Style the host element */
:host {
  display: block;
  font-family: sans-serif;
  border: 1px solid #ccc;
}

/* Conditional styling */
:host(.large) {
  font-size: 1.5rem;
}

:host(:hover) {
  border-color: blue;
}
```

---

## :host()
**Type:** pseudo-class function

Selects the host element with matching selector.

```css
:host(.theme-dark) {
  background: #1a1a1a;
  color: white;
}

:host([disabled]) {
  opacity: 0.5;
  pointer-events: none;
}
```

---

## :host-context()
**Type:** pseudo-class function

Styles the host element based on an ancestor outside the shadow tree.

```css
:host-context(.theme-dark) {
  background: #1a1a1a;
  color: white;
}

:host-context(body) {
  margin: 1rem;
}
```

---

## ::part()
**Type:** pseudo-element

Selects shadow DOM elements with `part` attribute.

```html
<!-- Host element -->
<my-card>
  <div slot="header">Title</div>
  <div slot="body">Content</div>
</my-card>
```

```css
/* From outside the shadow tree */
my-card::part(header) {
  background: #667eea;
  color: white;
  padding: 1rem;
}

my-card::part(body) {
  padding: 1rem;
}
```

---

## ::slotted()
**Type:** pseudo-element

Styles slotted content inside shadow DOM.

```css
/* Inside shadow tree */
::slotted(h1) {
  color: #667eea;
}

::slotted(p) {
  line-height: 1.6;
}

::slotted([slot="footer"]) {
  border-top: 1px solid #eee;
  margin-top: 1rem;
  padding-top: 1rem;
}
```

---

## Full Example

```html
<my-card>
  <span slot="title">Card Title</span>
  <p slot="content">Card content goes here.</p>
</my-card>
```

```css
/* Component styles (inside shadow root) */
:host {
  display: block;
  border: 1px solid #ddd;
  border-radius: 8px;
  overflow: hidden;
}

::slotted([slot="title"]) {
  display: block;
  padding: 1rem;
  background: #667eea;
  color: white;
  font-weight: bold;
}

::slotted([slot="content"]) {
  display: block;
  padding: 1rem;
}

/* From outside (in global stylesheet) */
my-card::part(title) {
  background: #764ba2;
}
```


---

[Example](../examples/advanced/24-components-and-shadow-dom/index.html)

← **Previous Topic:** [Advanced Math Functions](../advanced/23-advanced-math-functions.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** *(This is the last topic)* →

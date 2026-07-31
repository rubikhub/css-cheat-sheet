# Logic Matching Selectors

> 4 pseudo-classes

Match elements using selector lists and relational conditions.

---

## Selectors

---

## :is()

**Syntax:** `:is(<selector-list>)`

Matches any element that matches one of the selectors in its argument list.

**Values:**
- `:is(h1, h2, h3)` — any heading level 1 to 3
- `:is(.card, .panel):hover` — cards or panels on hover
- `:is(input, textarea, select):required` — required form fields
- `:is(h1, .title, #main-title)` — specificity of most specific argument

**Use Cases:**
- Group selectors into a single rule
- Reduce repeated selector lists

**Example:**
```css
:is(h1, h2, h3) {
  color: blue;
}

:is(.card, .panel):hover {
  transform: translateY(-2px);
}
```

---

## :where()

**Syntax:** `:where(<selector-list>)`

Matches like `:is()` but with zero specificity.

**Values:**
- `:where(h1, h2, h3)` — any heading, zero specificity
- `:where(.card, .panel):hover` — cards or panels on hover
- `:where(input, textarea, select):required` — required form fields

**Use Cases:**
- Set base styles that are easy to override
- Reset styles without adding specificity

**Example:**
```css
:where(h1, h2, h3) {
  color: blue;
}

h1 {
  color: red;
}
```

---

## :not()

**Syntax:** `:not(<selector-list>)`

Selects elements that do not match the argument selector.

**Values:**
- `:not(.disabled)` — elements without the disabled class
- `:not(:last-child)` — elements that are not the last child
- `:not(input)` — elements that are not inputs
- `:not(.active):not(.disabled)` — chained negative matches

**Use Cases:**
- Style all elements except certain ones
- Exclude elements by type or class

**Example:**
```css
:not(.disabled) {
  opacity: 1;
}

:not(:last-child) {
  border-bottom: 1px solid #eee;
}
```

---

## :has()

**Syntax:** `:has(<selector-list>)`

Selects elements that contain a matching descendant.

**Values:**
- `.card:has(img)` — cards that contain an image
- `.form:has(input:checked)` — forms with a checked input
- `.group:has(input:focus)` — groups with a focused input
- `nav:has(a:hover)` — navs with a hovered link
- `.container:has(.error):has(.warning)` — containers with both error and warning

**Use Cases:**
- Style a parent based on its children
- Apply styles when a specific descendant exists

**Example:**
```css
.card:has(img) {
  display: grid;
  grid-template-columns: 200px 1fr;
}

.form:has(input:checked) {
  background: lightyellow;
}
```

---

**[View Example](../examples/intermediate/04-logic-matching-selectors/index.html)**

← **Previous Topic:** [Combinators Advanced](../intermediate/03-combinators-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Form Pseudo Classes](../intermediate/05-form-pseudo-classes.md) →
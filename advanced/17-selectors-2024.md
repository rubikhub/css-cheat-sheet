# Selectors 2024+

> 7 selectors

Cutting-edge selectors and matching functions.

---

## :has() (Deep)

**Syntax:** `:has(<relative-selector-list>)`

Selects elements containing specific descendants.

**Values:**
- `form:has(input[type="password"])` — parent with a specific child
- `label:has(+ input:focus)` — label followed by a focused input
- `article:has(img):not(:has(video))` — article with an image but no video

**Use Cases:**
- Style a parent based on its children's state
- Conditionally apply layouts without extra classes

**Example:**
```css
label:has(+ input:focus) {
  color: blue;
}

article:has(img):not(:has(video)) {
  grid-template-rows: 200px 1fr;
}
```

---

## :is() (Specificity)

**Syntax:** `:is(<selector-list>)`

Matches any element in the selector list, using the highest specificity of its arguments.

**Values:**
- `:is(h1, h2, h3)` — matches h1, h2, or h3 (specificity 0,1,0)
- `:is(.card) h2` — matches h2 inside .card (specificity 0,1,0)

**Use Cases:**
- Group selectors in a single rule
- Reduce repeated selector lists

**Example:**
```css
:is(h1, h2, h3) {
  line-height: 1.2;
}

:is(.card) h2 {
  font-size: 1.25rem;
}
```

---

## :where() (Zero Specificity)

**Syntax:** `:where(<selector-list>)`

Same as `:is()` but always has zero specificity, making it easy to override.

**Values:**
- `:where(h1, h2, h3)` — matches any heading with zero specificity
- `:where(ul, ol)` — matches lists with zero specificity

**Use Cases:**
- Write resets that are easy to override
- Apply defaults without specificity battles

**Example:**
```css
:where(h1, h2, h3) {
  line-height: 1.2;
}

:where(ul, ol) {
  list-style: none;
  padding: 0;
}
```

---

## :user-valid

**Syntax:** `:user-valid` | `:user-invalid`

Matches input the browser considers valid or invalid after user interaction.

**Values:**
- `input:user-valid` — valid input after user interaction
- `input:user-invalid` — invalid input after user interaction

**Use Cases:**
- Style form fields after validation
- Show feedback only once the user interacts

**Example:**
```css
input:user-valid {
  border-color: green;
}

input:user-invalid {
  border-color: red;
}
```

---

## :open

**Syntax:** `:open`

Selects elements in an open state, such as details, select, and dialog.

**Values:**
- `details:open` — open details element
- `details:open::marker` — marker of an open details element
- `select:open` — open select dropdown

**Use Cases:**
- Style expanded accordions
- Highlight open dropdowns

**Example:**
```css
details:open {
  border: 2px solid blue;
}

details:open::marker {
  content: "▼ ";
}
```

---

## :popover-open

**Syntax:** `:popover-open`

Selects elements currently shown as popovers.

**Values:**
- `[popover]:popover-open` — popover currently shown
- `.tooltip:popover-open` — tooltip popover currently shown

**Use Cases:**
- Animate popovers into view
- Style the shown popover state

**Example:**
```css
.tooltip:popover-open {
  opacity: 1;
  transform: translateY(0);
}
```

---

## @scope (in Selectors context)

**Syntax:** `@scope (<scope-root>) to (<scope-limit>)`

Scopes styles to a subtree, optionally limited by a boundary element.

**Values:**
- `@scope (.card)` — applies styles within .card
- `@scope (.card) to (.card-footer)` — excludes the .card-footer subtree

**Use Cases:**
- Scope component styles without class prefixes
- Exclude nested sections from a scope

**Example:**
```css
@scope (.card) to (.card-footer) {
  p {
    color: #333;
  }
}
```

---

**[View Example](../examples/advanced/17-selectors-2024/index.html)**

← **Previous Topic:** [Container Queries](../advanced/16-container-queries.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Anchor Positioning](../advanced/18-anchor-positioning.md) →

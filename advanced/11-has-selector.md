# :has() — The Parent Selector

> 1 selector

Selects elements based on their children or sibling state.

---

## :has()

**Syntax:** `:has(<relative-selector-list>)`

Selects an element if it contains a descendant matching the argument.

**Values:**
- `.card:has(img)` — cards containing an image
- `form:has(:invalid)` — forms with an invalid input
- `label:has(+ input:checked)` — labels next to a checked input
- `div:has(p):has(img)` — elements containing both p and img
- `.card:not(:has(img))` — cards without an image
- `.list:has(> :empty)` — lists with an empty direct child

**Use Cases:**
- Style parents based on their children
- Create form validation states
- Style siblings based on nearby elements

**Example:**
```css
.card:has(img) {
  display: grid;
  grid-template-rows: 200px 1fr;
}

form:has(:invalid) {
  border-color: red;
}
```

---

**[View Example](../examples/advanced/11-has-selector/index.html)**

← **Previous Topic:** [Scroll Snap & Touch Interaction](../advanced/10-scroll-snap.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Advanced State Pseudo-classes](../advanced/12-state-pseudo-classes-advanced.md) →

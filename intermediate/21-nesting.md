# Nesting

> 1 nesting feature

Native CSS nesting groups related selectors and media queries inside their parent.

---

## Nesting

---

## CSS Nesting

**Syntax:** `& <selector>` | `&:pseudo-class` | `@media <condition>`

Feature — allows nesting selectors inside other selectors.

**Values:**
- `& .title` — nest a descendant selector
- `& a` — nest an element selector
- `&:hover` — nest a pseudo-class
- `&.active` — nest a compound selector
- `&.external::after` — nest with pseudo-elements
- `@media (max-width: 768px)` — nest a media query

**Use Cases:**
- Group related component styles together
- Keep hover and child styles close to the parent
- Nest media queries inside their selectors

**Example:**
```css
.card {
  padding: 1rem;
  background: white;

  & .title {
    font-size: 1.2rem;
    font-weight: bold;
  }

  &:hover {
    background: lightgray;
  }

  @media (max-width: 768px) {
    padding: 0.5rem;
  }
}
```

---

**[View Example](../examples/intermediate/21-nesting/index.html)**

← **Previous Topic:** [Transition Advanced](../intermediate/20-transition-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Typography — OpenType & Variable Font Features](../advanced/01-typography-ot-features.md) →

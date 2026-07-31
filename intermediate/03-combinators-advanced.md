# Combinators Advanced

> 4 selectors

Combine selectors to target elements based on their relationship in the DOM.

---

## Selectors

---

## ~ (General Sibling)

**Syntax:** `A ~ B`

Targets all siblings that come after the element.

**Values:**
- `h2 ~ p` — paragraphs after an h2
- `.active ~ .item` — items after an active element
- `.checked ~ label` — labels after a checked input
- `.selected ~ .option` — options after a selected element

**Use Cases:**
- Style all siblings following an element
- Apply a shared style to a group after a trigger

**Example:**
```css
h2 ~ p {
  color: gray;
}

.active ~ .item {
  opacity: 0.5;
}
```

---

## + (Adjacent Sibling)

**Syntax:** `A + B`

Targets the immediately following sibling.

**Values:**
- `h2 + p` — paragraph right after an h2
- `.active + .item` — item right after an active element
- `.checked + label` — label right after a checked input
- `.selected + .option` — option right after a selected element

**Use Cases:**
- Style the first element after a heading
- Style the label next to a checked input

**Example:**
```css
h2 + p {
  font-weight: bold;
}

.checked + label {
  color: blue;
}
```

---

## > (Child)

**Syntax:** `A > B`

Targets direct children only.

**Values:**
- `.nav > li` — direct list items in a nav
- `.container > .item` — direct item children
- `.list > li` — direct list items
- `.grid > div` — direct div children

**Use Cases:**
- Target only direct children, not nested ones
- Style the top level of nested lists

**Example:**
```css
.nav > li {
  display: inline-block;
}

.container > .item {
  margin-bottom: 1rem;
}
```

---

## (space) Descendant

**Syntax:** `A B`

Targets all descendants at any depth.

**Values:**
- `nav a` — all links inside a nav
- `.container p` — all paragraphs inside a container
- `.card h2` — all headings inside a card
- `.list li` — all list items inside a list

**Use Cases:**
- Style all nested elements of a type
- Apply styles to deeply nested content

**Example:**
```css
nav a {
  text-decoration: none;
}

.container p {
  margin-bottom: 1rem;
}
```

---

**[View Example](../examples/intermediate/03-combinators-advanced/index.html)**

← **Previous Topic:** [Attribute Selectors](../intermediate/02-attribute-selectors.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Logic Matching Selectors](../intermediate/04-logic-matching-selectors.md) →

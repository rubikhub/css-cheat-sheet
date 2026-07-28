# Combinators Basics

> 4 combinators

Ways to combine selectors based on relationship.

---

## Grouping Selector

**Syntax:** `selector1, selector2, selector3`

Applies the same styles to multiple selectors.

**Values:**
- `h1, h2, h3` — multiple element types
- `.button, .link` — multiple classes
- `#header, #footer` — multiple IDs
- `p, li, span` — mixed selectors

**Use Cases:**
- Share common styles between elements
- Reduce CSS repetition
- Apply base styles to multiple elements

**Example:**
```css
h1, h2, h3 {
  font-weight: 700;
  line-height: 1.2;
}

.button, .link {
  cursor: pointer;
  text-decoration: none;
}
```

---

## Descendant Combinator

**Syntax:** `A B`

Targets all B elements inside A (any depth).

**Values:**
- `div p` — all p inside div
- `.card span` — all span inside .card
- `article h2` — all h2 inside article

**Use Cases:**
- Style all paragraphs inside a container
- Apply styles to nested elements

**Example:**
```css
.card p {
  color: #666;
  line-height: 1.6;
}

.article h2 {
  font-size: 1.5rem;
  margin-top: 2rem;
}
```

---

## Child Combinator

**Syntax:** `A > B`

Targets only direct child B elements of A.

**Values:**
- `ul > li` — direct li children of ul
- `.nav > a` — direct a children of .nav
- `div > p` — direct p children of div

**Use Cases:**
- Style only direct children
- Avoid affecting nested descendants
- Create specific component styles

**Example:**
```css
.nav > li {
  display: inline-block;
}

.nav > li > a {
  padding: 0.5rem 1rem;
}
```

---

## Adjacent Sibling Combinator

**Syntax:** `A + B`

Targets the first B element immediately after A.

**Values:**
- `h2 + p` — first p after h2
- `.header + .content` — .content after .header
- `img + figcaption` — figcaption after img

**Use Cases:**
- Remove top margin on first paragraph after heading
- Style elements immediately following others

**Example:**
```css
h2 + p {
  margin-top: 0;
}

.header + .content {
  padding-top: 0;
}
```

---

## General Sibling Combinator

**Syntax:** `A ~ B`

Targets all B elements that follow A (any depth).

**Values:**
- `h2 ~ p` — all p after h2
- `.header ~ .content` — all .content after .header
- `input ~ label` — all label after input

**Use Cases:**
- Style all siblings after a specific element
- Create layouts with sibling relationships

**Example:**
```css
h2 ~ p {
  color: #666;
}

.header ~ .content {
  margin-top: 1rem;
}
```

---

**[View Example](../examples/beginner/06-combinators-basics/index.html)**

← **Previous Topic:** [Basic Selectors](../beginner/05-basic-selectors.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Color Functions Basics](../beginner/07-color-functions-basics.md) →

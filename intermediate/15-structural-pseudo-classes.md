# Structural Pseudo Classes

> 8 pseudo-classes

Target elements based on their position among siblings.

---

## Structural

---

## :nth-child(an+b)

**Syntax:** `:nth-child(an+b)`

Selects elements based on their position among siblings.

**Values:**
- `2` — second element
- `odd` — odd elements (1, 3, 5...)
- `even` — even elements (2, 4, 6...)
- `3n` — every third element
- `3n+1` — every third starting at 1
- `-n+3` — first three elements
- `n+4` — elements from 4 onward

**Use Cases:**
- Create zebra-striped lists and tables
- Target specific positions in a group

**Example:**
```css
li:nth-child(2) {
  color: blue;
}

li:nth-child(even) {
  background: lightyellow;
}

li:nth-child(3n) {
  font-weight: bold;
}

li:nth-child(-n+3) {
  border-left: 3px solid blue;
}
```

---

## :nth-of-type(an+b)

**Syntax:** `:nth-of-type(an+b)`

Selects elements of a specific type among siblings.

**Values:**
- `1` — first element of that type
- `2` — second element of that type
- `odd` — odd positions of that type
- `3n` — every third element of that type

**Use Cases:**
- Target specific tags among mixed siblings
- Style paragraphs or divs by position

**Example:**
```css
p:nth-of-type(1) {
  font-size: 1.2em;
}

div:nth-of-type(odd) {
  background: lightgray;
}

span:nth-of-type(3n) {
  color: red;
}

p:nth-of-type(2) {
  font-style: italic;
}
```

---

## :nth-last-of-type(an+b)

**Syntax:** `:nth-last-of-type(an+b)`

Selects elements of a specific type from the end.

**Values:**
- `1` — last element of that type
- `2` — second to last of that type
- `odd` — odd positions from the end
- `3n` — every third from the end

**Use Cases:**
- Target the last of a specific tag type
- Style from the end of mixed sibling groups

**Example:**
```css
p:nth-last-of-type(1) {
  font-size: 1.2em;
}

div:nth-last-of-type(odd) {
  background: lightgray;
}

span:nth-last-of-type(3n) {
  color: red;
}

p:nth-last-of-type(2) {
  font-style: italic;
}
```

---

## :empty

**Syntax:** `:empty`

Selects elements with no children or text content.

**Values:**
- `div:empty` — empty div elements
- `.cell:empty` — empty table cells
- `.input:empty` — empty input containers
- `.container:empty` — empty containers

**Use Cases:**
- Hide empty elements
- Add placeholder content via ::before

**Example:**
```css
div:empty {
  display: none;
}

.input:empty::before {
  content: "Enter text...";
  color: #999;
}

.container:empty {
  border: 1px dashed #ccc;
}
```

---

## :only-of-type

**Syntax:** `:only-of-type`

Matches an element that is the only element of its type among its siblings.

**Values:**
- `p:only-of-type` — the only paragraph among siblings
- `li:only-of-type` — the only list item in its list
- Implies `:first-of-type` and `:last-of-type`

**Use Cases:**
- Style a lone callout
- Distinguish single items in a group

**Example:**
```css
p:only-of-type {
  font-style: italic;
}
```

---

## :first-of-type / :last-of-type

**Syntax:** `:first-of-type` | `:last-of-type`

Matches the first or last element of its type among siblings.

**Values:**
- `p:first-of-type` — first paragraph among siblings
- `li:last-of-type` — last list item
- `:first-of-type` is the same as `:nth-of-type(1)`

**Use Cases:**
- Style intro paragraphs
- Remove borders from the last block

**Example:**
```css
p:first-of-type {
  font-size: 1.1em;
}

li:last-of-type {
  border-bottom: none;
}
```

---

## :root

**Syntax:** `:root`

Matches the document root element (the html element).

**Values:**
- `:root { --brand: #123; }` — define global custom properties
- `:root { color-scheme: light dark; }` — set the color scheme
- Equivalent to `html` but with higher specificity

**Use Cases:**
- Centralize global custom properties
- Set document-level defaults

**Example:**
```css
:root {
  --brand: #4f46e5;
  --spacing: 1rem;
}
```

---

## :nth-child(An+B of S)

**Syntax:** `:nth-child(<An+B> of <selector-list>)`

Limits nth-child matching to elements that also match the given selector list.

**Values:**
- `:nth-child(2 of .item)` — the second .item
- `:nth-child(odd of li.active)` — odd-numbered active items
- `:nth-child(3n of .featured)` — every third featured item

**Use Cases:**
- Style every other tile in a filtered list
- Target a specific item within a subset

**Example:**
```css
li:nth-child(3n of .featured) {
  color: var(--brand);
}
```

---

**[View Example](../examples/intermediate/15-structural-pseudo-classes/index.html)**

← **Previous Topic:** [Grid Advanced](../intermediate/14-grid-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Form Pseudo Classes](../intermediate/16-form-pseudo-classes.md) →


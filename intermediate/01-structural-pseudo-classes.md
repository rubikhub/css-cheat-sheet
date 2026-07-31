# Structural Pseudo Classes

> 8 pseudo-classes

Target elements based on their position among siblings.

---

## Structural

---

## :first-child

**Syntax:** `:first-child`

Selects the first child element of its parent.

**Values:**
- `li:first-child` — first list item
- `.item:first-child` — first .item element
- `.card:first-child` — first card
- `p:first-child` — first paragraph

**Use Cases:**
- Style the first element in a group
- Remove the top border of a first child

**Example:**
```css
li:first-child {
  font-weight: bold;
}

p:first-child {
  font-size: 1.2em;
}

.card:first-child {
  background: lightyellow;
}
```

---

## :last-child

**Syntax:** `:last-child`

Selects the last child element of its parent.

**Values:**
- `li:last-child` — last list item
- `.item:last-child` — last .item element
- `.card:last-child` — last card
- `p:last-child` — last paragraph

**Use Cases:**
- Style the last element in a group
- Remove the bottom border of a last child

**Example:**
```css
li:last-child {
  font-weight: bold;
  color: red;
}

.item:last-child {
  border-bottom: 2px solid green;
}

p:last-child {
  margin-bottom: 0;
}
```

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

## :nth-last-child(an+b)

**Syntax:** `:nth-last-child(an+b)`

Selects elements based on position from the end.

**Values:**
- `1` — last element
- `odd` — odd positions from the end
- `even` — even positions from the end
- `3n` — every third from the end
- `-n+2` — last two elements

**Use Cases:**
- Style elements near the end of a group
- Create reverse counting patterns

**Example:**
```css
li:nth-last-child(1) {
  color: red;
}

li:nth-last-child(odd) {
  background: lightgray;
}

li:nth-last-child(-n+2) {
  border-right: 3px solid blue;
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

## :only-child

**Syntax:** `:only-child`

Selects an element that is the only child of its parent.

**Values:**
- `li:only-child` — only list item
- `.item:only-child` — only .item element
- `.card:only-child` — only card
- `p:only-child` — only paragraph

**Use Cases:**
- Style single items differently
- Adjust spacing for solo elements

**Example:**
```css
li:only-child {
  font-weight: bold;
  color: blue;
}

.item:only-child {
  border: 2px solid green;
}

p:only-child {
  font-size: 1.2em;
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

**[View Example](../examples/intermediate/01-structural-pseudo-classes/index.html)**

← **Previous Topic:** [Logical Properties](../beginner/21-logical-properties.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Attribute Selectors](../intermediate/02-attribute-selectors.md) →

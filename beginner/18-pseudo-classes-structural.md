# Structural Pseudo-classes

> 6 pseudo-classes

Target elements based on their position in the document structure.

---

## Structural

---

## :first-child

**Syntax:** `:first-child`

Targets the first child element of its parent.

**Values:**
- `li:first-child` — first list item
- `p:first-child` — first paragraph
- `.card:first-child` — first .card element

**Use Cases:**
- Remove top margin on first element
- Style first items differently

**Example:**
```css
li:first-child {
  font-weight: 700;
}

p:first-child {
  margin-top: 0;
}
```

---

## :last-child

**Syntax:** `:last-child`

Targets the last child element of its parent.

**Values:**
- `li:last-child` — last list item
- `p:last-child` — last paragraph
- `.card:last-child` — last .card element

**Use Cases:**
- Remove bottom margin on last element
- Style last items differently

**Example:**
```css
li:last-child {
  border-bottom: none;
}

p:last-child {
  margin-bottom: 0;
}
```

---

## :nth-child(an+b)

**Syntax:** `:nth-child(an+b)`

Targets elements based on position in a group.

**Values:**
- `:nth-child(2)` — second element
- `:nth-child(odd)` — odd elements (1, 3, 5...)
- `:nth-child(even)` — even elements (2, 4, 6...)
- `:nth-child(3n)` — every third element
- `:nth-child(3n+1)` — every third starting at 1
- `:nth-child(-n+3)` — first three elements

**Use Cases:**
- Create zebra-striped tables
- Style every other element
- Target specific positions

**Example:**
```css
tr:nth-child(even) {
  background: #f5f5f5;
}

li:nth-child(3n) {
  color: #0066cc;
}

li:nth-child(-n+3) {
  font-weight: 700;
}
```

---

## :nth-last-child(an+b)

**Syntax:** `:nth-last-child(an+b)`

Targets elements based on position from the end.

**Values:**
- `:nth-last-child(1)` — last element
- `:nth-last-child(2)` — second to last
- `:nth-last-child(odd)` — odd from end
- `:nth-last-child(even)` — even from end
- `:nth-last-child(3n)` — every third from end

**Use Cases:**
- Style elements near the end
- Create reverse counting patterns

**Example:**
```css
li:nth-last-child(-n+3) {
  font-weight: 700;
}
```

---

## :only-child

**Syntax:** `:only-child`

Targets elements that are the only child of their parent.

**Values:**
- `p:only-child` — only paragraph in parent
- `li:only-child` — only list item

**Use Cases:**
- Style single items differently
- Adjust spacing for solo elements

**Example:**
```css
p:only-child {
  margin: 0;
}
```

---

## :empty

**Syntax:** `:empty`

Targets elements with no children or text content.

**Values:**
- `div:empty` — empty div elements
- `p:empty` — empty paragraphs

**Use Cases:**
- Hide empty elements
- Add placeholder content

**Example:**
```css
div:empty {
  display: none;
}
```

---

**[View Example](../examples/beginner/18-pseudo-classes-structural/index.html)**

← **Previous Topic:** [Opacity](../beginner/17-opacity.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [State Pseudo-classes](../beginner/19-pseudo-classes-state.md) →


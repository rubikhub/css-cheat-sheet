# Pseudo-Classes Basics

> 12 pseudo-classes

Target elements based on state, position, or structure.

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

## State & Interaction

---

## :hover

**Syntax:** `:hover`

Targets elements when the mouse is over them.

**Values:**
- `a:hover` — links on hover
- `button:hover` — buttons on hover
- `.card:hover` — cards on hover

**Use Cases:**
- Add hover effects to interactive elements
- Provide visual feedback

**Example:**
```css
a:hover {
  color: #0066cc;
  text-decoration: underline;
}

.button:hover {
  background: #0055aa;
  transform: translateY(-2px);
}
```

---

## :active

**Syntax:** `:active`

Targets elements being clicked/activated.

**Values:**
- `button:active` — buttons while clicking
- `a:active` — links while clicking
- `.link:active` — custom link active state

**Use Cases:**
- Add click feedback
- Create pressed button effects

**Example:**
```css
button:active {
  transform: scale(0.98);
  background: #004499;
}

a:active {
  color: #003366;
}
```

---

## :focus

**Syntax:** `:focus`

Targets elements that have keyboard focus.

**Values:**
- `input:focus` — inputs when focused
- `button:focus` — buttons when focused
- `a:focus` — links when focused

**Use Cases:**
- Create focus indicators for accessibility
- Highlight active form fields

**Example:**
```css
input:focus {
  outline: 2px solid #0066cc;
  border-color: #0066cc;
}

button:focus {
  outline: 2px solid #0066cc;
  outline-offset: 2px;
}
```

---

## :link

**Syntax:** `:link`

Targets unvisited links.

**Values:**
- `a:link` — unvisited links

**Use Cases:**
- Style unvisited links differently
- Create link state styles

**Example:**
```css
a:link {
  color: #0066cc;
}
```

---

## :visited

**Syntax:** `:visited`

Targets visited links.

**Values:**
- `a:visited` — visited links

**Use Cases:**
- Show visited state
- Distinguish visited from unvisited

**Example:**
```css
a:visited {
  color: #551a8b;
}
```

---

## :target

**Syntax:** `:target`

Targets the element whose ID matches the URL fragment.

**Values:**
- `#section:target` — element with id matching URL
- `.highlight:target` — highlighted element

**Use Cases:**
- Style current section in single-page navigation
- Highlight anchored content

**Example:**
```css
:target {
  background: #fffde7;
  border-left: 4px solid #ffc107;
}
```

---

**[View Example](../examples/beginner/16-pseudo-classes-basics/index.html)**

← **Previous Topic:** [Opacity](../beginner/15-opacity.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Pseudo-Elements Basics](../beginner/17-pseudo-elements-basics.md) →

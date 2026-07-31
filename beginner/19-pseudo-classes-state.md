# State Pseudo-classes

> 6 pseudo-classes

Target elements based on user interaction and link state.

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

**[View Example](../examples/beginner/19-pseudo-classes-state/index.html)**

← **Previous Topic:** [Structural Pseudo-classes](../beginner/18-pseudo-classes-structural.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Pseudo-Elements Basics](../beginner/20-pseudo-elements-basics.md) →


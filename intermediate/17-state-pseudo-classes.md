# State Pseudo Classes

> 8 pseudo-classes

Target elements based on user interaction — hover, click, focus, and navigation state.

---

## States

---

## :active

**Syntax:** `:active`

Targets elements while they are being clicked/activated.

**Values:**
- `a:active` — links while clicking
- `button:active` — buttons while clicking
- `.card:active` — cards while pressing

**Use Cases:**
- Add click feedback
- Create pressed button effects

**Example:**
```css
button:active {
  background: darkred;
  transform: scale(0.95);
}

a:active {
  color: red;
}
```

---

## :focus

**Syntax:** `:focus`

Targets elements that have keyboard or programmatic focus.

**Values:**
- `input:focus` — inputs when focused
- `textarea:focus` — textareas when focused
- `a:focus` — links when focused

**Use Cases:**
- Create focus indicators for accessibility
- Highlight active form fields

**Example:**
```css
input:focus {
  border-color: blue;
  box-shadow: 0 0 5px rgba(0, 0, 255, 0.5);
}

a:focus {
  outline: 2px solid blue;
  outline-offset: 2px;
}
```

---

## :visited

**Syntax:** `:visited`

Targets links that have been visited.

**Values:**
- `a:visited` — visited links
- `a:visited:hover` — visited links on hover
- `.link:visited` — custom visited links

**Use Cases:**
- Show visited state
- Distinguish visited from unvisited

**Example:**
```css
a:visited {
  color: purple;
}

.link:visited {
  color: #551a8b;
  text-decoration: none;
}
```

---

## :focus-visible

**Syntax:** `:focus-visible`

Targets elements focused via keyboard rather than mouse.

**Values:**
- `button:focus-visible` — buttons when keyboard focused
- `input:focus-visible` — inputs when keyboard focused
- `a:focus-visible` — links when keyboard focused

**Use Cases:**
- Show focus rings only for keyboard users
- Avoid focus outlines on mouse clicks

**Example:**
```css
button:focus-visible {
  outline: 2px solid blue;
  outline-offset: 2px;
}

input:focus-visible {
  border-color: blue;
  box-shadow: 0 0 5px rgba(0, 0, 255, 0.5);
}
```

---

## :focus-within

**Syntax:** `:focus-within`

Targets an element when it or any descendant has focus.

**Values:**
- `form:focus-within` — forms containing a focused field
- `.card:focus-within` — cards containing a focused element
- `.container:focus-within` — containers containing a focused element

**Use Cases:**
- Highlight whole containers on focus
- Style form groups when a field is focused

**Example:**
```css
form:focus-within {
  border-color: blue;
  box-shadow: 0 0 10px rgba(0, 0, 255, 0.3);
}

.card:focus-within {
  background: lightyellow;
}
```

---

## :target

**Syntax:** `:target`

Targets the element whose ID matches the URL fragment.

**Values:**
- `:target` — element matching the URL fragment
- `.section:target` — sections matching a fragment
- `.tab:target` — tabs matching a fragment

**Use Cases:**
- Highlight the current section in single-page navigation
- Style anchored content

**Example:**
```css
:target {
  background: lightyellow;
  border: 2px solid blue;
}

.section:target {
  scroll-margin-top: 80px;
}
```

---

## :any-link

**Syntax:** `:any-link`

Matches every hyperlink, covering both `:link` and `:visited`.

**Values:**
- `a:any-link` — any anchor with an href
- `a:any-link:hover` — hover on any link state

**Use Cases:**
- Style links without repeating :link and :visited

**Example:**
```css
a:any-link {
  color: #2563eb;
}
```

---

## :modal

**Syntax:** `:modal`

Matches elements displayed in a modal state, such as a dialog opened with showModal().

**Values:**
- `dialog:modal` — an open modal dialog
- `dialog:modal::backdrop` — style the modal backdrop

**Use Cases:**
- Style open dialogs and their backdrops

**Example:**
```css
dialog:modal {
  border: none;
  border-radius: 8px;
}

dialog:modal::backdrop {
  background: rgb(0 0 0 / 0.5);
}
```

---

**[View Example](../examples/intermediate/17-state-pseudo-classes/index.html)**

← **Previous Topic:** [Form Pseudo Classes](../intermediate/16-form-pseudo-classes.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Pseudo Elements Advanced](../intermediate/18-pseudo-elements-advanced.md) →


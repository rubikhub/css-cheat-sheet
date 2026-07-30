# Pseudo-Elements Basics

> 6 pseudo-elements

Style specific parts of elements or add generated content.

---

## ::before

**Syntax:** `::before`

Inserts generated content before the element's actual content.

**Values:**
- `content: ""` — empty pseudo-element
- `content: "★"` — icon content
- `content: attr(data-tooltip)` — attribute value

**Use Cases:**
- Add icons or decorations
- Create custom bullets
- Insert content dynamically

**Example:**
```css
.link::before {
  content: "→ ";
  color: #0066cc;
}

.card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 4px;
  height: 100%;
  background: #0066cc;
}
```

---

## ::after

**Syntax:** `::after`

Inserts generated content after the element's actual content.

**Values:**
- `content: ""` — empty pseudo-element
- `content: "→"` — arrow icon
- `content: attr(href)` — link URL

**Use Cases:**
- Add decorative elements
- Create clearfix solutions
- Append icons or indicators

**Example:**
```css
a[href^="http"]::after {
  content: " ↗";
  font-size: 0.8em;
}

.clearfix::after {
  content: "";
  display: table;
  clear: both;
}
```

---

## ::first-line

**Syntax:** `::first-line`

Targets the first line of text in a block element.

**Values:**
- `p::first-line` — first line of paragraphs
- `.article::first-line` — first line of articles

**Use Cases:**
- Style opening text differently
- Create drop cap effects
- Emphasize first line

**Example:**
```css
p::first-line {
  font-weight: 700;
  color: #333;
}
```

---

## ::first-letter

**Syntax:** `::first-letter`

Targets the first letter of text in a block element.

**Values:**
- `p::first-letter` — first letter of paragraphs
- `.drop-cap::first-letter` — drop cap styling

**Use Cases:**
- Create drop cap effects
- Style first letter for emphasis

**Example:**
```css
.drop-cap::first-letter {
  font-size: 3rem;
  font-weight: 700;
  float: left;
  line-height: 1;
  margin-right: 0.5rem;
}
```

---

## ::selection

**Syntax:** `::selection`

Targets the portion of text selected by the user.

**Values:**
- `::selection` — selected text
- `p::selection` — selected text in paragraphs

**Use Cases:**
- Customize text selection color
- Create branded selection styles

**Example:**
```css
::selection {
  background: #0066cc;
  color: white;
}
```

---

## ::placeholder

**Syntax:** `::placeholder`

Targets placeholder text in form inputs.

**Values:**
- `input::placeholder` — placeholder text
- `textarea::placeholder` — textarea placeholder

**Use Cases:**
- Style placeholder text
- Customize form input placeholders

**Example:**
```css
input::placeholder {
  color: #999;
  font-style: italic;
}
```

---

**[View Example](../examples/beginner/17-pseudo-elements-basics/index.html)**

← **Previous Topic:** [Pseudo-Classes Basics](../beginner/16-pseudo-classes-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Cursor](../beginner/18-cursor.md) →

# Pseudo Elements Advanced

> 7 pseudo-elements

Insert and style generated content with pseudo-elements.

---

## Pseudo-elements

---

## ::before

**Syntax:** `::before`

Inserts content before the element's content.

**Values:**
- `.icon::before` — inserts a star icon
- `.arrow::before` — inserts a unicode arrow
- `.card::before` — empty content for decoration
- `blockquote::before` — inserts an opening quote
- `.list-item::before` — inserts a counter number

**Use Cases:**
- Add icons without extra markup
- Create decorative accents and quote marks

**Example:**
```css
.icon::before {
  content: "★";
}

.card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: #0066cc;
}
```

---

## ::after

**Syntax:** `::after`

Inserts content after the element's content.

**Values:**
- `.icon::after` — inserts a star icon
- `.clearfix::after` — clears floated children
- `.tooltip::after` — renders text from a data attribute
- `a[target="_blank"]::after` — external link indicator
- `blockquote::after` — inserts a closing quote

**Use Cases:**
- Build tooltips from data attributes
- Add clearfixes and external link indicators

**Example:**
```css
.tooltip::after {
  content: attr(data-tooltip);
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

Styles the first line of a block-level element.

**Values:**
- `p::first-line` — styles the first line of paragraphs
- `h1::first-line` — styles the first line of headings
- `blockquote::first-line` — styles the first line of blockquotes
- `.article::first-line` — styles the first line of article text

**Use Cases:**
- Emphasize the opening line of a paragraph
- Style the first line of headings differently

**Example:**
```css
p::first-line {
  font-weight: bold;
  color: #0066cc;
}

blockquote::first-line {
  font-style: italic;
  text-transform: uppercase;
}
```

---

## ::first-letter

**Syntax:** `::first-letter`

Styles the first letter of a block-level element.

**Values:**
- `p::first-letter` — styles the first letter of paragraphs
- `h1::first-letter` — styles the first letter of headings
- `blockquote::first-letter` — styles the first letter of blockquotes

**Use Cases:**
- Create drop cap effects
- Style the initial letter of paragraphs

**Example:**
```css
p::first-letter {
  font-size: 2em;
  font-weight: bold;
  float: left;
}
```

---

## ::selection

**Syntax:** `::selection`

Styles the selected/highlighted text.

**Values:**
- `::selection` — styles all selected text
- `p::selection` — styles selected text in paragraphs
- `h1::selection` — styles selected text in headings

**Use Cases:**
- Brand text selection with theme colors
- Improve selection visibility on dark backgrounds

**Example:**
```css
::selection {
  background: #ffd54d;
  color: #000;
}
```

---

## ::placeholder

**Syntax:** `::placeholder`

Styles the placeholder text of form inputs.

**Values:**
- `input::placeholder` — styles placeholder of text inputs
- `textarea::placeholder` — styles placeholder of textareas

**Use Cases:**
- Style input hints with muted colors
- Add italic styling to placeholder text

**Example:**
```css
input::placeholder {
  color: #999;
  font-style: italic;
}
```

---

## ::file-selector-button

**Syntax:** `::file-selector-button`

Targets the file-picker button of an `input[type=file]`.

**Values:**
- `input[type='file']::file-selector-button` — the button element
- Style it with normal button properties

**Use Cases:**
- Match file upload buttons to the design system

**Example:**
```css
input[type='file']::file-selector-button {
  background: #4f46e5;
  color: white;
  border: none;
  padding: 0.5em 1em;
  border-radius: 6px;
}
```

---

**[View Example](../examples/intermediate/18-pseudo-elements-advanced/index.html)**

← **Previous Topic:** [State Pseudo Classes](../intermediate/17-state-pseudo-classes.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Transition Advanced](../intermediate/19-transition-advanced.md) →


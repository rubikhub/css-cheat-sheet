# Cutting-edge Pseudo-elements

> 6 pseudo-elements

Modern pseudo-elements for spelling, grammar, and highlights.

---

## ::spelling-error

**Syntax:** `::spelling-error`

Selects text with a spelling error (browser-dependent).

**Values:**
- `::spelling-error` — misspelled text
- `p::spelling-error` — misspelled text in a paragraph

**Use Cases:**
- Customize the spelling error underline
- Style error text to match your theme

**Example:**
```css
::spelling-error {
  text-decoration: wavy underline red;
}
```

---

## ::grammar-error

**Syntax:** `::grammar-error`

Selects text with a grammar error (browser-dependent).

**Values:**
- `::grammar-error` — grammatically incorrect text
- `p::grammar-error` — grammar errors in a paragraph

**Use Cases:**
- Customize the grammar error underline
- Distinguish grammar errors from spelling errors

**Example:**
```css
::grammar-error {
  text-decoration: wavy underline green;
}
```

---

## ::highlight()

**Syntax:** `::highlight(<custom-highlight-name>)`

Selects text within a named CSS Highlight.

**Values:**
- `::highlight(my-highlight)` — text in a named highlight
- `::highlight(search)` — search results highlight

**Use Cases:**
- Style ranges marked by the Highlight API
- Apply consistent styling to selected text

**Example:**
```css
::highlight(my-highlight) {
  background: yellow;
  color: black;
}
```

---

## ::backdrop

**Syntax:** `::backdrop`

Styles the full-screen backdrop behind a top-layer element (dialog or fullscreen).

**Values:**
- `dialog:modal::backdrop` — modal dialog backdrop
- `:fullscreen::backdrop` — fullscreen backdrop
- Style with color, blur, and backdrop-filter

**Use Cases:**
- Dim and blur content behind modals

**Example:**
```css
dialog::backdrop {
  background: rgb(0 0 0 / 0.6);
  backdrop-filter: blur(4px);
}
```

---

## ::target-text

**Syntax:** `::target-text`

Styles the text that the browser scrolls to when navigating with text fragments.

**Values:**
- `::target-text` — the highlighted fragment text
- Pairs with `#:~:text=` URLs

**Use Cases:**
- Customize the text-fragment highlight color
- Match highlights to your theme

**Example:**
```css
::target-text {
  background: yellow;
  color: black;
}
```

---

## ::details-content

**Syntax:** `::details-content`

Styles the hidden content area of a details element.

**Values:**
- `details::details-content` — the content region
- Pairs with `:open` for the expanded state

**Use Cases:**
- Animate accordion content in and out
- Style the details content area separately from the summary

**Example:**
```css
details::details-content {
  padding: 1rem;
}

details:open::details-content {
  animation: expand 0.3s ease;
}
```

---

**[View Example](../examples/advanced/15-pseudo-elements-cutting-edge/index.html)**

← **Previous Topic:** [Form Pseudo-classes — Advanced](../advanced/14-form-pseudo-classes-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [View Transitions](../advanced/16-view-transitions.md) →


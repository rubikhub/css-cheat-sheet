# Cutting-edge Pseudo-elements

> 8 pseudo-elements

Modern pseudo-elements for spelling, grammar, highlights, and view transitions.

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

## ::view-transition

**Syntax:** `::view-transition`

The root pseudo-element wrapping the entire view transition.

**Values:**
- `::view-transition` — the root transition container

**Use Cases:**
- Style the transition overlay
- Set fixed positioning for the snapshot layer

**Example:**
```css
::view-transition {
  position: fixed;
  inset: 0;
}
```

---

## ::view-transition-group()

**Syntax:** `::view-transition-group(<name>)`

Targets a specific view transition group by name.

**Values:**
- `::view-transition-group(hero)` — the hero element's group
- `::view-transition-group(page)` — the page's group

**Use Cases:**
- Animate different groups at different speeds
- Control the layout of transition snapshots

**Example:**
```css
::view-transition-group(hero) {
  animation-duration: 0.5s;
}

::view-transition-group(page) {
  animation-duration: 0.3s;
}
```

---

## ::view-transition-image-pair()

**Syntax:** `::view-transition-image-pair(<name>)`

Targets the before/after image pair of a transition.

**Values:**
- `::view-transition-image-pair(hero)` — the old and new state pair

**Use Cases:**
- Blend or mask the old and new snapshots
- Customize how states layer during a transition

**Example:**
```css
::view-transition-image-pair(hero) {
  mix-blend-mode: normal;
}
```

---

## ::view-transition-old()

**Syntax:** `::view-transition-old(<name>)`

Targets the old (outgoing) state of a view transition.

**Values:**
- `::view-transition-old(hero)` — the outgoing hero snapshot

**Use Cases:**
- Create exit animations
- Fade out the old page state

**Example:**
```css
::view-transition-old(hero) {
  animation: fade-out 0.3s ease;
}
```

---

## ::view-transition-new()

**Syntax:** `::view-transition-new(<name>)`

Targets the new (incoming) state of a view transition.

**Values:**
- `::view-transition-new(hero)` — the incoming hero snapshot

**Use Cases:**
- Create entrance animations
- Fade in the new page state

**Example:**
```css
::view-transition-new(hero) {
  animation: fade-in 0.3s ease;
}
```

---

**[View Example](../examples/advanced/14-pseudo-elements-cutting-edge/index.html)**

← **Previous Topic:** [Form Pseudo-classes — Advanced](../advanced/13-form-pseudo-classes-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [CSS At-Rules — Advanced](../advanced/15-at-rules.md) →

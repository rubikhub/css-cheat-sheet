# Web Components & Shadow DOM

> 6 features

Styling inside Shadow DOM and component encapsulation.

---

## Host Styling

---

## :host

**Syntax:** `:host`

Selects the shadow host element from within the shadow tree.

**Values:**
- `:host` — any host element
- `:host(.large)` — host with the class large
- `:host(:hover)` — host in a hover state
- `:host-context(selector)` — host inside a matching ancestor

**Use Cases:**
- Style the component root element
- Apply conditional host styles

**Example:**
```css
:host {
  display: block;
  font-family: sans-serif;
  border: 1px solid #ccc;
}

:host(.large) {
  font-size: 1.5rem;
}
```

---

## :host()

**Syntax:** `:host(<selector>)`

Selects the host element when it matches a selector.

**Values:**
- `:host(.theme-dark)` — host with the theme-dark class
- `:host([disabled])` — disabled host
- `:host(h1)` — host element of type h1

**Use Cases:**
- Style hosts by class or attribute
- Theme components from the host state

**Example:**
```css
:host([disabled]) {
  opacity: 0.5;
  pointer-events: none;
}
```

---

## :host-context()

**Syntax:** `:host-context(<selector>)`

Styles the host element based on an ancestor outside the shadow tree.

**Values:**
- `:host-context(.theme-dark)` — host inside a theme-dark ancestor
- `:host-context(body)` — host inside body
- `:host-context(.sidebar)` — host inside a sidebar

**Use Cases:**
- Theme components from page context
- Apply styles based on ancestor classes

**Example:**
```css
:host-context(.theme-dark) {
  background: #1a1a1a;
  color: white;
}
```

---

## Slots & Parts

---

## ::part()

**Syntax:** `::part(<name>)`

Selects shadow DOM elements with a `part` attribute from outside the shadow tree.

**Values:**
- `my-card::part(header)` — the header part
- `my-card::part(body)` — the body part
- `my-card::part(title)` — any named part

**Use Cases:**
- Style component internals from outside
- Expose themable parts of a component

**Example:**
```css
my-card::part(header) {
  background: #667eea;
  color: white;
  padding: 1rem;
}
```

---

## ::slotted()

**Syntax:** `::slotted(<selector>)`

Styles slotted content inside the shadow DOM.

**Values:**
- `::slotted(h1)` — slotted h1 elements
- `::slotted(p)` — slotted paragraphs
- `::slotted([slot="footer"])` — elements in the footer slot

**Use Cases:**
- Style user-provided slot content
- Provide default styling for slotted elements

**Example:**
```css
::slotted(h1) {
  color: #667eea;
}

::slotted([slot="footer"]) {
  border-top: 1px solid #eee;
  margin-top: 1rem;
  padding-top: 1rem;
}
```

---

## :defined

**Syntax:** `:defined`

Matches any element that is defined — built-in or a registered custom element.

**Values:**
- `my-widget:defined` — registered and upgraded custom element
- `:not(:defined)` — custom elements not yet upgraded

**Use Cases:**
- Hide unstyled custom elements until they are upgraded

**Example:**
```css
my-widget:not(:defined) {
  visibility: hidden;
}

my-widget:defined {
  visibility: visible;
}
```

---

**[View Example](../examples/advanced/03-components-and-shadow-dom/index.html)**

← **Previous Topic:** [Selectors 2024+](../advanced/02-selectors-2024.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Advanced Color Functions](../advanced/04-color-functions-advanced.md) →

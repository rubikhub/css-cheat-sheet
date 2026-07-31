# CSS At-Rules — Advanced

> 9 features

Modern at-rules for layers, properties, scope, and view transitions.

---

## @property

**Syntax:** `@property --name { syntax; inherits; initial-value; }`

Declares custom properties with type, initial value, and inheritance.

**Values:**
- `syntax: '<color>'` — color value type
- `syntax: '<length>'` — length value type
- `syntax: '<number>'` — number value type
- `initial-value: #333` — fallback color value
- `initial-value: 1rem` — fallback length value
- `inherits: true` — custom property inherits
- `inherits: false` — custom property doesn't inherit

**Use Cases:**
- Register typed custom properties
- Enable animation of custom properties

**Example:**
```css
@property --my-color {
  syntax: '<color>';
  initial-value: #333;
  inherits: false;
}

@property --my-size {
  syntax: '<length>';
  initial-value: 1rem;
  inherits: true;
}
```

---

## @layer

**Syntax:** `@layer <name>;` | `@layer <name> { ... }`

Defines cascade layers for explicit specificity ordering.

**Values:**
- `@layer base, components, utilities;` — declare layer order
- `@layer base { ... }` — base styles layer
- `@layer components { ... }` — component styles layer
- `@layer utilities { ... }` — utility styles layer

**Use Cases:**
- Control style precedence without specificity
- Organize styles into logical groups

**Example:**
```css
@layer base, components, utilities;

@layer components {
  .card { padding: 1rem; border: 1px solid #eee; }
}
```

---

## @scope

**Syntax:** `@scope (<selector>) to (<limit>) { ... }` | `@scope (<selector>) { ... }`

Scopes styles to a specific DOM subtree with a scoping root and optional limit.

**Values:**
- `@scope (.card) to (.card-footer)` — scoped styles with a limit
- `@scope (.dropdown) { ... }` — scoped styles without a limit

**Use Cases:**
- Style components in isolation
- Avoid selector collisions across components

**Example:**
```css
@scope (.card) to (.card-footer) {
  p { color: #333; }
  a { color: blue; }
}
```

---

## @starting-style

**Syntax:** `@starting-style { ... }`

Defines styles for elements about to be displayed (enter transition).

**Values:**
- `@starting-style { .toast { opacity: 0; } }` — entry state before display

**Use Cases:**
- Animate elements on first render
- Smoothly show dialogs and toasts

**Example:**
```css
@starting-style {
  .toast {
    opacity: 0;
    transform: translateY(20px);
  }
}

.toast {
  opacity: 1;
  transform: translateY(0);
  transition: opacity 0.3s, transform 0.3s;
}
```

---

## @view-transition

**Syntax:** `@view-transition { navigation: auto; }`

Enables view transitions for navigation.

**Values:**
- `navigation: auto` — enable transitions for navigation
- `navigation: same-document` — same-document navigation only
- `navigation: none` — disable transitions

**Use Cases:**
- Enable cross-document view transitions
- Opt into animated page navigations

**Example:**
```css
@view-transition {
  navigation: auto;
}
```

---

## @counter-style

**Syntax:** `@counter-style <name> { system; symbols; suffix; }`

Defines custom counter styles.

**Values:**
- `system: cyclic` — repeat symbols in order
- `symbols: "\1F44D"` — symbols to use
- `suffix: " "` — text after each counter
- `list-style-type: thumbs` — apply the custom counter style

**Use Cases:**
- Create custom bullet or numbering styles
- Reuse symbol sets across lists

**Example:**
```css
@counter-style thumbs {
  system: cyclic;
  symbols: "\1F44D";
  suffix: " ";
}

ol {
  list-style-type: thumbs;
}
```

---

## @supports

**Syntax:** `@supports (<property>: <value>) | not <condition> | and | or`

Applies styles only when the browser supports a feature.

**Values:**
- `@supports (display: grid)` — property support
- `@supports (selector(:has(*)))` — selector support
- `@supports not (display: grid)` — negation
- `@supports (display: grid) and (gap: 1rem)` — combination

**Use Cases:**
- Progressive enhancement with fallbacks

**Example:**
```css
@supports (display: grid) {
  .layout {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
  }
}
```

---

## @import

**Syntax:** `@import url(<url>) [<media-query>]`

Loads an external stylesheet into the current one.

**Values:**
- `@import url('theme.css')` — plain import
- `@import 'print.css' print;` — import for print only
- Must appear before other rules except @charset and @layer statements

**Use Cases:**
- Split stylesheets across files
- Conditional imports per media type

**Example:**
```css
@import 'theme.css';
@import 'print.css' print;
```

---

## interpolate-size

**Syntax:** `interpolate-size: numeric-only | allow-keywords`

Allows transitions and animations between keyword and numeric sizes.

**Values:**
- `numeric-only` — only numeric values animate (default)
- `allow-keywords` — enables animating to auto/intrinsic sizes

**Use Cases:**
- Animate height to auto together with @starting-style

**Example:**
```css
:root {
  interpolate-size: allow-keywords;
}

.accordion {
  height: auto;
  transition: height 300ms;
}
```

---

**[View Example](../examples/advanced/19-at-rules/index.html)**

← **Previous Topic:** [Scroll Snap & Touch Interaction](../advanced/18-scroll-snap.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Container Queries](../advanced/20-container-queries.md) →

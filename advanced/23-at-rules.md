# CSS At-Rules — Advanced

> 15 features

Modern at-rules for layers, properties, scope, and counters.

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

## @custom-media

**Syntax:** `@custom-media --name (<media-features>);`

Defines reusable named media queries.

**Values:**
- `@custom-media --narrow (width < 600px);` — a named width query
- `@custom-media --dark (prefers-color-scheme: dark);` — named preference query

**Use Cases:**
- Reuse media conditions across files
- Centralize breakpoints in one place

**Example:**
```css
@custom-media --narrow (width < 600px);
@custom-media --motion-ok (prefers-reduced-motion: no-preference);

@media (--narrow) {
  .grid {
    grid-template-columns: 1fr;
  }
}
```

---

## @when / @else

**Syntax:** `@when <condition> { ... } @else <condition> { ... } @else { ... }`

Conditional group rules — the generic if/else for CSS.

**Values:**
- `@when media(...)` — media-condition branch
- `@when supports(...)` — support-condition branch
- `@else media(...)` — subsequent conditions
- `@else` — the fallback branch

**Use Cases:**
- Replace nested @media/@supports combinations
- Write clearer progressive enhancement

**Example:**
```css
@when media (width >= 600px) {
  .layout {
    display: grid;
  }
} @else {
  .layout {
    display: block;
  }
}
```

---

## @function

**Syntax:** `@function --name (<args>) { result: <value>; }`

Defines custom CSS functions (2026).

**Values:**
- `@function --spacing($mult) { result: calc(0.5rem * $mult); }` — a scaling function
- `result:` — the function's return value
- Arguments are used inside the body

**Use Cases:**
- Encapsulate reusable calculations
- Reduce repetition of complex math

**Example:**
```css
@function --fluid($min, $max) {
  result: clamp($min, 2vw, $max);
}

h1 {
  font-size: --fluid(1rem, 2.5rem);
}
```

---

## @mixin / @apply

**Syntax:** `@mixin --name { ... }` | `@apply --name;`

CSS mixins — reusable style blocks applied with @apply.

**Values:**
- `@mixin --button { ... }` — define a mixin
- `@apply --button;` — apply it inside a rule
- Mixins can accept arguments in the extended syntax

**Use Cases:**
- Share button, badge, and card styles
- Replace preprocessor mixins in native CSS

**Example:**
```css
@mixin --chip {
  padding: 4px 12px;
  border-radius: 999px;
  display: inline-flex;
}

.tag {
  @apply --chip;
  background: #667eea;
}
```

---

## @nest

**Syntax:** `@nest <selector> { ... }`

Enables nesting a selector that does not start with a nesting selector.

**Values:**
- `@nest &:hover` — nest using & explicitly
- `@nest .parent > &` — nest a compound selector
- Mostly superseded by the & nesting shorthand

**Use Cases:**
- Nest selectors that need a leading compound
- Keep preprocessor-style nesting

**Example:**
```css
.card {
  @nest section > & {
    margin: 2rem;
  }
}
```

---

## @charset

**Syntax:** `@charset "UTF-8";`

Declares the character encoding of the stylesheet.

**Values:**
- `@charset "UTF-8";` — UTF-8 encoding
- Must be the very first line of the file, no leading characters

**Use Cases:**
- Declare encoding for legacy servers and tools
- Ensure emoji and non-Latin text render correctly

**Example:**
```css
@charset "UTF-8";
```

---

## @namespace

**Syntax:** `@namespace <prefix>? <url>;`

Declares namespaces used by element and attribute selectors.

**Values:**
- `@namespace svg url(http://www.w3.org/2000/svg);` — an SVG prefix
- `svg|circle { ... }` — select within the namespace
- `@namespace url(...)` — default namespace

**Use Cases:**
- Style SVG or XML documents by namespace
- Scope selectors to a specific markup language

**Example:**
```css
@namespace svg url(http://www.w3.org/2000/svg);
svg|a {
  fill: blue;
}
```

---

**[View Example](../examples/advanced/23-at-rules/index.html)**

← **Previous Topic:** [Scroll Snap & Touch Interaction](../advanced/22-scroll-snap.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Container Queries](../advanced/24-container-queries.md) →


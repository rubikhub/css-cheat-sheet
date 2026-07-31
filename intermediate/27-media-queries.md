# Media Queries

> 6 features

Apply styles conditionally based on viewport size, device capabilities, and user preferences.

---

## @media & Media Types

**Syntax:** `@media <media-type> and (<media-feature>) { ... }`

Conditionally applies styles when the media query matches.

**Values:**
- `all` — matches all devices (default)
- `screen` — matches screen-based devices
- `print` — matches print media (used for print stylesheets)
- `@media (max-width: 768px)` — match viewports 768px or narrower
- `@media print` — apply styles only when printing

**Use Cases:**
- Make layouts responsive to screen size
- Provide a separate print stylesheet

**Example:**
```css
@media screen {
  .card {
    display: grid;
  }
}

@media print {
  .nav {
    display: none;
  }
}
```

---

## Media Features

**Syntax:** `@media (<feature>: <value>)`

Media features describe the environment the styles are applied in.

**Values:**
- `width` / `min-width` / `max-width` — viewport width
- `height` / `min-height` / `max-height` — viewport height
- `orientation` — `portrait` | `landscape`
- `aspect-ratio` — width/height ratio, e.g. `16/9`
- `resolution` — device pixel density, e.g. `2dppx`

**Use Cases:**
- Adapt layouts to different viewport sizes
- Serve dense graphics to high-resolution screens

**Example:**
```css
@media (min-width: 600px) {
  .layout {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (orientation: landscape) {
  .sidebar {
    display: block;
  }
}

@media (resolution: 2dppx) {
  .logo {
    background-image: url('logo@2x.png');
  }
}
```

---

## Range Syntax

**Syntax:** `@media (min-width <= width <= max-width)`

Modern range syntax expresses min/max constraints without prefixing the feature name.

**Values:**
- `(400px <= width <= 700px)` — width between 400px and 700px
- `(width >= 600px)` — equivalent to `min-width: 600px`
- `(width < 1000px)` — narrower than 1000px
- `(600px < width)` — wider than 600px

**Use Cases:**
- Express viewport intervals more clearly
- Combine lower and upper bounds in one condition

**Example:**
```css
@media (400px <= width <= 700px) {
  .grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
```

---

## Logical Operators

**Syntax:** `@media <condition> and <condition> | @media or | not <condition>`

Combine or negate media conditions.

**Values:**
- `and` — all conditions must match
- `or` — any condition can match
- `not` — negates the whole query
- `,` — comma list acts like `or`

**Use Cases:**
- Target tablets and desktop together
- Exclude a specific range

**Example:**
```css
@media (min-width: 600px) and (orientation: landscape) {
  .header {
    padding: 2rem;
  }
}

@media not (width < 400px) {
  .content {
    margin: 1rem;
  }
}
```

---

## Interaction Features

**Syntax:** `@media (hover: none) | (pointer: coarse)`

Media features that describe the pointing device.

**Values:**
- `hover` — `none` | `hover` — can the primary input hover?
- `any-hover` — `none` | `hover` — can any input hover?
- `pointer` — `none` | `coarse` | `fine` — accuracy of the primary pointer
- `any-pointer` — `none` | `coarse` | `fine` — accuracy of any pointer

**Use Cases:**
- Show tap targets instead of hover styles on touch devices
- Provide mouse-only affordances

**Example:**
```css
@media (hover: hover) {
  .card:hover {
    transform: translateY(-4px);
  }
}

@media (pointer: coarse) {
  .button {
    min-height: 44px;
  }
}
```

---

## User Preference Queries

**Syntax:** `@media (prefers-color-scheme: light | dark)`

Media features that respect user OS-level preferences.

**Values:**
- `prefers-color-scheme` — `light` | `dark`
- `prefers-reduced-motion` — `no-preference` | `reduce`
- `prefers-contrast` — `no-preference` | `more` | `less`
- `prefers-reduced-transparency` — `no-preference` | `reduce`

**Use Cases:**
- Implement dark mode
- Disable animations for users who prefer reduced motion

**Example:**
```css
:root {
  --bg: white;
  --text: #222;
}

@media (prefers-color-scheme: dark) {
  :root {
    --bg: #111;
    --text: #eee;
  }
}

@media (prefers-reduced-motion: reduce) {
  * {
    animation: none;
    transition: none;
  }
}
```

---

**[View Example](../examples/intermediate/27-media-queries/index.html)**

← **Previous Topic:** [Nesting](../intermediate/26-nesting.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [:has() — The Parent Selector](../advanced/01-has-selector.md) →


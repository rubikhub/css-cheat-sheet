# Advanced Visual Effects

> 2 properties

Backdrop filters and blend modes.

---

## backdrop-filter

**Syntax:** `backdrop-filter: <filter-function-list> | none`

Applies filter effects to the area behind an element (frosted glass effect).

**Values:**
- `none` — no backdrop filter (default)
- `blur(10px)` — gaussian blur on the backdrop
- `brightness(150%)` — adjusts backdrop brightness
- `contrast(200%)` — adjusts backdrop contrast
- `grayscale(100%)` — converts backdrop to grayscale
- `blur(5px) brightness(150%)` — combines multiple filters
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create frosted glass cards
- Blur content behind modals

**Example:**
```css
.glass-card {
  backdrop-filter: blur(10px);
  -webkit-backdrop-filter: blur(10px);
  background: rgba(255, 255, 255, 0.25);
  border: 1px solid rgba(255, 255, 255, 0.3);
}
```

---

## mix-blend-mode

**Syntax:** `mix-blend-mode: normal | multiply | screen | overlay | darken | lighten | color-dodge | color-burn | hard-light | soft-light | difference | exclusion | hue | saturation | color | luminosity`

Determines how an element's content blends with what's behind it.

**Values:**
- `normal` — no blending (default)
- `multiply` — multiplies colors, darkens
- `screen` — inverts multiply, lightens
- `overlay` — combines multiply and screen
- `darken` — keeps the darker color
- `lighten` — keeps the lighter color
- `color-dodge` — brightens the backdrop
- `color-burn` — darkens the backdrop
- `hard-light` — strong contrast blend
- `soft-light` — subtle contrast blend
- `difference` — subtracts colors
- `exclusion` — like difference, softer
- `hue` — uses element hue with backdrop saturation/luminosity
- `saturation` — uses element saturation
- `color` — uses element hue and saturation
- `luminosity` — uses element luminosity
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Blend text or shapes over images
- Create textured overlays

**Example:**
```css
.text-over-image {
  mix-blend-mode: multiply;
}

.logo {
  mix-blend-mode: screen;
}
```

---

**[View Example](../examples/advanced/20-advanced-effects/index.html)**

← **Previous Topic:** [Animation — Direction, Fill Mode & Play State](../advanced/19-animation-fill-and-play-state.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [CSS Masks](../advanced/21-css-masks.md) →


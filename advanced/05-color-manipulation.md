# Color Manipulation

> 4 features

Mixing and deriving colors, and scheme-aware theming.

---

## color-mix()

**Syntax:** `color-mix(in <color-space>, <color> <percentage>, <color> <percentage>)`

Mixes two colors in a given color space.

**Values:**
- `color-mix(in srgb, red, blue)` — equal 50/50 mix
- `color-mix(in oklch, #667eea 30%, #764ba2 70%)` — weighted mix
- `color-mix(in srgb, currentColor 50%, transparent)` — mix with transparency

**Use Cases:**
- Create color shades from a base color
- Blend with currentColor for theming

**Example:**
```css
.element {
  background: color-mix(in oklch, #667eea 30%, #764ba2 70%);
}
```

---

## relative color syntax

**Syntax:** `oklch(from <color> <components>)`

Derives colors from existing colors using `from`.

**Values:**
- `oklch(from var(--primary) calc(l + 0.2) c h)` — lighter version
- `oklch(from var(--primary) calc(l - 0.2) c h)` — darker version
- `oklch(from var(--primary) l c h / 50%)` — transparent version
- `oklch(from var(--primary) l calc(c * 0.5) h)` — desaturated version

**Use Cases:**
- Create hover and active color variants
- Derive shades and tints from a theme color

**Example:**
```css
.button:hover {
  background: oklch(from var(--primary) calc(l - 0.1) c h);
}
```

---

## color-scheme

**Syntax:** `color-scheme: normal | light | dark | light dark`

Declares which color schemes an element renders in.

**Values:**
- `normal` — no preference (default)
- `light` — light scheme only
- `dark` — dark scheme only
- `light dark` — supports both

**Use Cases:**
- Opt into dark scrollbars and form controls

**Example:**
```css
:root {
  color-scheme: light dark;
}
```

---

## light-dark()

**Syntax:** `color: light-dark(<light-color>, <dark-color>)`

Returns a color based on the current color scheme.

**Values:**
- `light-dark(white, black)` — white in light, black in dark mode
- `light-dark(var(--bg), var(--bg-dark))` — use with custom properties
- Requires `color-scheme` to be set on an ancestor

**Use Cases:**
- Theme components without media queries

**Example:**
```css
.card {
  color-scheme: light dark;
  background: light-dark(#fff, #222);
  color: light-dark(#222, #fff);
}
```

---

**[View Example](../examples/advanced/05-color-manipulation/index.html)**

← **Previous Topic:** [Color Spaces](../advanced/04-color-spaces.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Background Blend Mode](../advanced/06-background-blend-mode.md) →


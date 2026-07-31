# Advanced Color Functions

> 9 features

Modern color definition and mixing functions using perceptually uniform color spaces.

---

## Color Spaces

---

## oklch()

**Syntax:** `oklch(L C H / alpha)`

Defines colors using Lightness, Chroma, and Hue in the OKLCH color space.

**Values:**
- `oklch(70% 0.15 250)` — blue at 70% lightness
- `oklch(0.9 0.05 100 / 0.8)` — pale green at 80% opacity
- `oklch(0.5 0.2 300)` — purple at 50% lightness
- `oklch(65% 0.15 260)` — primary blue
- `oklch(75% 0.2 30)` — orange accent

**Use Cases:**
- Create perceptually uniform color palettes
- Adjust lightness while keeping hue constant

**Example:**
```css
.element {
  color: oklch(70% 0.15 250);
  background: oklch(0.9 0.05 100 / 0.8);
}
```

---

## oklab()

**Syntax:** `oklab(L a b / alpha)`

Defines colors using Lightness, a-axis, and b-axis in the OKLAB color space.

**Values:**
- `oklab(0.7 0.1 -0.1)` — mid lightness with a green-blue cast
- `oklab(0.9 0.05 0.05 / 0.5)` — pale color at 50% opacity
- `oklab(0.5 0.2 0)` — deep neutral color

**Use Cases:**
- Create perceptually uniform colors
- Fine-tune color with the a and b axes

**Example:**
```css
.element {
  color: oklab(0.7 0.1 -0.1);
  background: oklab(0.9 0.05 0.05 / 0.5);
}
```

---

## lch()

**Syntax:** `lch(L C H / alpha)`

Defines colors using Lightness, Chroma, and Hue in the CIE LCH color space.

**Values:**
- `lch(70% 50 240)` — blue at 70% lightness
- `lch(90% 30 120 / 0.9)` — green at 90% opacity
- `lch(50% 60 20)` — saturated red-orange

**Use Cases:**
- Define colors by perceptual lightness
- Keep lightness stable while changing hue

**Example:**
```css
.element {
  color: lch(70% 50 240);
  background: lch(90% 30 120 / 0.9);
}
```

---

## lab()

**Syntax:** `lab(L a b / alpha)`

Defines colors using Lightness and the a and b axes in the CIE LAB color space.

**Values:**
- `lab(50% 30 -20)` — green-blue at 50% lightness
- `lab(90% 10 20 / 0.8)` — pale red at 80% opacity
- `lab(30% 50 50)` — deep red

**Use Cases:**
- Define device-independent colors
- Match colors across displays

**Example:**
```css
.element {
  color: lab(50% 30 -20);
  background: lab(90% 10 20 / 0.8);
}
```

---

## color()

**Syntax:** `color(<color-space> <channels> / <alpha>)`

Defines colors in various color spaces.

**Values:**
- `color(display-p3 1 0.5 0)` — orange in Display P3
- `color(prophoto-rgb 0.8 0.4 0.2)` — brown in ProPhoto RGB
- `color(rec2020 0.5 0.3 0.7)` — purple in Rec2020

**Use Cases:**
- Use wide-gamut colors such as Display P3
- Target specific color spaces

**Example:**
```css
.element {
  color: color(display-p3 1 0.5 0);
}
```

---

## Color Manipulation

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

**[View Example](../examples/advanced/04-color-functions-advanced/index.html)**

← **Previous Topic:** [Web Components & Shadow DOM](../advanced/03-components-and-shadow-dom.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Background Blend Mode](../advanced/05-background-blend-mode.md) →

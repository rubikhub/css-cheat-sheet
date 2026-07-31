# Color Spaces

> 5 features

Modern color definition functions using perceptually uniform color spaces.

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

**[View Example](../examples/advanced/04-color-spaces/index.html)**

← **Previous Topic:** [Web Components & Shadow DOM](../advanced/03-components-and-shadow-dom.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Color Manipulation](../advanced/05-color-manipulation.md) →


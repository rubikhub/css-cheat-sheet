# Advanced Color Functions

Modern color manipulation and definition functions.

---

## oklch()
**Type:** function

Defines colors using Lightness, Chroma, and Hue in the OKLCH color space.

```css
/* oklch(L C H / alpha) */
.element {
  color: oklch(70% 0.15 250);
  background: oklch(0.9 0.05 100 / 0.8);
  border-color: oklch(0.5 0.2 300);
}

/* Perceptually uniform */
.primary { color: oklch(65% 0.15 260); }
.secondary { color: oklch(70% 0.12 180); }
.accent { color: oklch(75% 0.2 30); }
```

---

## oklab()
**Type:** function

Defines colors using Lightness, a-axis, and b-axis in the OKLAB color space.

```css
/* oklab(L a b / alpha) */
.element {
  color: oklab(0.7 0.1 -0.1);
  background: oklab(0.9 0.05 0.05 / 0.5);
}
```

---

## lch()
**Type:** function

CIE LCH color space (Lightness, Chroma, Hue).

```css
.element {
  color: lch(70% 50 240);
  background: lch(90% 30 120 / 0.9);
}
```

---

## lab()
**Type:** function

CIE LAB color space.

```css
.element {
  color: lab(50% 30 -20);
  background: lab(90% 10 20 / 0.8);
}
```

---

## color()
**Type:** function

Defines colors in various color spaces.

```css
/* Display P3 */
.element {
  color: color(display-p3 1 0.5 0);
}

/* ProPhoto RGB */
.element {
  color: color(prophoto-rgb 0.8 0.4 0.2);
}

/* Rec2020 */
.element {
  color: color(rec2020 0.5 0.3 0.7);
}
```

---

## color-mix()
**Type:** function

Mixes two colors in a given color space.

```css
/* 50/50 mix */
.element {
  background: color-mix(in srgb, red, blue);
}

/* Custom比例 */
.element {
  background: color-mix(in oklch, #667eea 30%, #764ba2 70%);
}

/* With alpha */
.element {
  background: color-mix(in srgb, currentColor 50%, transparent);
}
```

---

## relative color syntax
**Type:** syntax

Derives colors from existing colors using `from`.

```css
/* Lighter version */
--primary-light: oklch(from var(--primary) calc(l + 0.2) c h);

/* Darker version */
--primary-dark: oklch(from var(--primary) calc(l - 0.2) c h);

/* Transparent version */
--primary-transparent: oklch(from var(--primary) l c h / 50%);

/* Desaturated */
--primary-muted: oklch(from var(--primary) l calc(c * 0.5) h);
```

```css
:root {
  --primary: oklch(65% 0.2 260);
}

.button {
  background: var(--primary);
}

.button:hover {
  background: oklch(from var(--primary) calc(l - 0.1) c h);
}

.button:active {
  background: oklch(from var(--primary) calc(l - 0.2) c h);
}

.button-light {
  background: oklch(from var(--primary) calc(l + 0.3) c h / 20%);
}
```


---

[Example](../examples/advanced/21-color-functions-advanced/index.html)

← **Previous Topic:** [Scroll State Queries](../advanced/20-scroll-state.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Typography 2024+](../advanced/22-typography-2024.md) →

# Color Functions Basics

> 6 functions

Ways to specify and manipulate colors in CSS.

---

## Named Colors

**Syntax:** `<named-color>`

Predefined color names recognized by browsers.

**Values:**
- `red` — #ff0000
- `blue` — #0000ff
- `green` — #008000
- `black` — #000000
- `white` — #ffffff
- `transparent` — fully transparent
- `currentColor` — matches current color

**Use Cases:**
- Quick color specification
- Readable color values

**Example:**
```css
.text {
  color: red;
}

.background {
  background: transparent;
}
```

---

## Hex Colors

**Syntax:** `#RRGGBB` | `#RGB`

Hexadecimal color notation.

**Values:**
- `#ff5733` — 6-digit hex (full)
- `#f00` — 3-digit hex (shorthand)
- `#ff573380` — 8-digit hex (with alpha)
- `#f008` — 4-digit hex (shorthand with alpha)

**Use Cases:**
- Precise color specification
- Brand color values

**Example:**
```css
.text {
  color: #333;
}

.accent {
  color: #0066cc;
}

.transparent {
  background: rgba(0, 0, 0, 0.5);
}
```

---

## RGB / RGBA

**Syntax:** `rgb(red, green, blue)` | `rgba(red, green, blue, alpha)`

Red, Green, Blue color model.

**Values:**
- `rgb(255, 0, 0)` — pure red
- `rgb(0, 128, 0)` — green
- `rgb(255, 255, 255)` — white
- `rgba(0, 0, 0, 0.5)` — black with 50% opacity
- `rgb(0% 50% 100%)` — percentage values
- `rgb(255 0 0 / 0.5)` — modern syntax

**Use Cases:**
- Precise color mixing
- Adding transparency to colors

**Example:**
```css
.text {
  color: rgb(51, 51, 51);
}

.overlay {
  background: rgba(0, 0, 0, 0.5);
}

.gradient {
  background: rgb(102 126 234 / 0.8);
}
```

---

## HSL / HSLA

**Syntax:** `hsl(hue, saturation, lightness)` | `hsla(hue, saturation, lightness, alpha)`

Hue, Saturation, Lightness color model.

**Values:**
- `hsl(0, 100%, 50%)` — pure red
- `hsl(120, 100%, 50%)` — pure green
- `hsl(240, 100%, 50%)` — pure blue
- `hsla(0, 0%, 0%, 0.5)` — black with opacity
- `hsl(200 50% 50%)` — modern syntax

**Use Cases:**
- Create color variations easily
- Adjust lightness/darkness
- Generate color palettes

**Example:**
```css
.text {
  color: hsl(0, 0%, 33%);
}

.accent {
  color: hsl(210, 100%, 50%);
}

.overlay {
  background: hsla(0, 0%, 0%, 0.5);
}
```

---

## currentColor

**Syntax:** `currentColor`

Keyword that references the current color value.

**Values:**
- `currentColor` — matches the element's computed color
- Used in borders, shadows, and gradients

**Use Cases:**
- Create color-consistent components
- Use text color for borders/shadows
- Build theme-aware styles

**Example:**
```css
.button {
  color: #0066cc;
  border: 2px solid currentColor;
}

.icon {
  color: #333;
  filter: drop-shadow(0 0 2px currentColor);
}
```

---

## transparent

**Syntax:** `transparent`

Keyword for fully transparent color.

**Values:**
- `transparent` — fully transparent (rgba(0,0,0,0))
- Used for backgrounds and borders

**Use Cases:**
- Create invisible backgrounds
- Make borders transparent
- Build hover transitions

**Example:**
```css
.button {
  background: transparent;
  border: 1px solid #0066cc;
  transition: background 0.2s;
}

.button:hover {
  background: #0066cc;
}
```
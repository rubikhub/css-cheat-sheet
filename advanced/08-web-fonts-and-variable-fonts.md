# Web & Variable Fonts

> 4 features

Declaring custom fonts with @font-face and tuning variable font axes.

---

## @font-face

**Syntax:** `@font-face { font-family; src; font-weight; font-style; font-display; }`

Declares a custom font family and its source file.

**Values:**
- `font-family: 'CustomFont'` — the name used to reference the font
- `src: url(...) format('woff2')` — font file and format
- `font-weight: 100 900` — range of supported weights
- `font-style: normal` — font style
- `font-display: swap` — fallback display behavior

**Use Cases:**
- Load custom fonts for branding
- Optimize font loading with font-display

**Example:**
```css
@font-face {
  font-family: 'CustomFont';
  src: url('custom-font.woff2') format('woff2'),
       url('custom-font.woff') format('woff');
  font-weight: 100 900;
  font-style: normal;
  font-display: swap;
}
```

---

## @font-feature-values

**Syntax:** `@font-feature-values <family> { @styleset { ... } }`

Defines named values for OpenType feature settings, reusable across rules.

**Values:**
- `@font-feature-values MyFont` — binds the definitions to a font family
- `@styleset { liga: 1; kern: 1; }` — named styleset values
- `@swash { swsh: 1; }` — named swash values

**Use Cases:**
- Create reusable names for feature settings
- Keep feature values consistent across rules

**Example:**
```css
@font-feature-values MyFont {
  @styleset {
    liga: 1;
    kern: 1;
  }
  @swash {
    swsh: 1;
  }
}
```

---

## font-variation-settings

**Syntax:** `font-variation-settings: <axis> <value>`

Fine-tunes variable font axes (weight, width, optical size, custom axes).

**Values:**
- `'wght' 750` — set the weight axis
- `'opsz' 36` — set the optical size axis
- `'wdth' 110` — set the width axis
- `'wght' 750, 'opsz' 36, 'wdth' 110` — set multiple axes
- `'XTRA' 500` — set a custom axis
- `normal` — no variation (default)
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Fine-tune variable font weight or width
- Set custom axes for design fonts

**Example:**
```css
.thin {
  font-variation-settings: 'wght' 100;
}

.bold {
  font-variation-settings: 'wght' 900;
}

.wide {
  font-variation-settings: 'wdth' 150;
}
```

---

## font-optical-sizing

**Syntax:** `font-optical-sizing: auto | none`

Controls whether the browser adjusts optical size for the font.

**Values:**
- `auto` — browser adjusts optical size (default)
- `none` — disables optical sizing
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Keep text readable at large display sizes
- Disable optical sizing for consistent rendering

**Example:**
```css
.display {
  font-optical-sizing: auto;
}

.title {
  font-optical-sizing: none;
}
```

---

**[View Example](../examples/advanced/08-web-fonts-and-variable-fonts/index.html)**

← **Previous Topic:** [Typography — OpenType Features](../advanced/07-typography-ot-features.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Typography 2024+](../advanced/09-typography-2024.md) →


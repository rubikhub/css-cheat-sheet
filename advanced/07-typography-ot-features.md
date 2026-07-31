# Typography — OpenType Features

> 4 properties

Advanced typography properties for OpenType features.

---

## OpenType Features

---

## font-feature-settings

**Syntax:** `font-feature-settings: <feature-tag> <value>`

Enables or disables specific OpenType font features by tag.

**Values:**
- `"liga" 1` — enable ligatures
- `"kern" 1` — enable kerning
- `"smcp" 1` — enable small caps
- `"onum" 1` — enable old-style numerals
- `"liga" 0` — disable a feature
- `"liga" 1, "kern" 1, "smcp" 1` — multiple features at once
- `normal` — no feature settings (default)
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Enable OpenType typographic features
- Toggle ligatures or numeral styles

**Example:**
```css
.fancy {
  font-feature-settings: "liga" 1, "kern" 1;
}

.old-nums {
  font-feature-settings: "onum" 1;
}
```

---

## font-variant-ligatures

**Syntax:** `font-variant-ligatures: normal | none | <ligature>`

Controls common, contextual, discretionary, and historical ligatures.

**Values:**
- `normal` — common and contextual ligatures (default)
- `none` — no ligatures
- `common-ligatures` / `no-common-ligatures`
- `discretionary-ligatures` / `historical-ligatures`

**Use Cases:**
- Enable fancy ligatures for display text

**Example:**
```css
.brand {
  font-variant-ligatures: discretionary-ligatures;
}
```

---

## font-variant-numeric

**Syntax:** `font-variant-numeric: normal | <numeric-feature>`

Controls figure style, spacing, fractions, and ordinals.

**Values:**
- `lining-nums` / `oldstyle-nums` — figure style
- `tabular-nums` — fixed-width digits for tables
- `proportional-nums` — natural digit widths
- `diagonal-fractions` / `stacked-fractions`

**Use Cases:**
- Align numbers in tables and stat blocks

**Example:**
```css
.price {
  font-variant-numeric: tabular-nums;
}
```

---

## font-variant-caps

**Syntax:** `font-variant-caps: normal | small-caps | all-small-caps | petite-caps | unicase | titling-caps`

Controls capital-letter styling.

**Values:**
- `normal` — default capitalization (default)
- `small-caps` — small capital letters
- `all-small-caps` — small caps for all letters
- `titling-caps` — display capitals

**Use Cases:**
- Style headings and labels without retyping

**Example:**
```css
.nav-label {
  font-variant-caps: all-small-caps;
}
```

---

**[View Example](../examples/advanced/07-typography-ot-features/index.html)**

← **Previous Topic:** [Background Blend Mode](../advanced/06-background-blend-mode.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Web & Variable Fonts](../advanced/08-web-fonts-and-variable-fonts.md) →


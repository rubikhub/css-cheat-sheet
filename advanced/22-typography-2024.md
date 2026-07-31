# Typography 2024+

> 9 properties

Modern CSS typography features for text wrapping, font metrics, and color fonts.

---

## Text Wrapping

---

## text-wrap: balance

**Syntax:** `text-wrap: balance`

Balances line lengths for better readability.

**Values:**
- `balance` — balances line lengths across the block
- `wrap` — normal wrapping (default)
- `nowrap` — no wrapping
- `pretty` — optimizes line breaks
- `inherit` — inherits from parent
- `initial` — sets to default (wrap)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Balance multi-line headings
- Improve the look of short centered text

**Example:**
```css
h1, h2, h3 {
  text-wrap: balance;
}
```

---

## text-wrap: pretty

**Syntax:** `text-wrap: pretty`

Optimizes line breaks for better readability.

**Values:**
- `pretty` — optimizes line breaking and avoids orphans
- `wrap` — normal wrapping (default)
- `balance` — balances line lengths
- `nowrap` — no wrapping
- `inherit` — inherits from parent
- `initial` — sets to default (wrap)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Reduce orphaned words in paragraphs
- Improve paragraph text appearance

**Example:**
```css
p {
  text-wrap: pretty;
}
```

---

## Font Metrics

---

## text-box-trim / text-box-edge

**Syntax:** `text-box-trim: none | trim-start | trim-end | both; text-box-edge: auto | <edge>`

Trims whitespace above and below text for precise sizing.

**Values:**
- `both` — trim above and below
- `top` — trim above only
- `bottom` — trim below only
- `none` — no trimming (default)
- `ex alphabetic` — trim to ex-height and alphabetic baseline
- `cap alphabetic` — trim to cap height and alphabetic baseline
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Align text precisely in buttons and badges
- Remove leading whitespace around headings

**Example:**
```css
.heading {
  text-box-trim: both;
  text-box-edge: ex alphabetic;
}
```

---

## font-size-adjust

**Syntax:** `font-size-adjust: <number> | none`

Adjusts font size to maintain x-height.

**Values:**
- `none` — no adjustment (default)
- `0.5` — match an x-height ratio of 0.5
- `ex-height 0.5` — adjust using the ex-height metric
- `ch-width 0.5` — adjust using the ch-width metric
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Keep fallback fonts visually similar
- Maintain x-height across font families

**Example:**
```css
body {
  font-size-adjust: 0.5;
}

.text {
  font-size-adjust: ex-height 0.5;
}
```

---

## Font Palettes

---

## font-palette

**Syntax:** `font-palette: normal | <palette-identifier>`

Selects a font palette from the font.

**Values:**
- `normal` — use the font's default palette (default)
- `--my-palette` — use a custom palette
- `light` — use the font's light palette
- `dark` — use the font's dark palette
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Swap color font palettes
- Apply brand colors to color fonts

**Example:**
```css
.heading {
  font-palette: --my-palette;
}

@font-palette-values --my-palette {
  font-family: "My Font";
  base-palette: 0;
  override-colors: 0 #333, 1 #667eea;
}
```

---

## @font-palette-values

**Syntax:** `@font-palette-values <name> { font-family; base-palette; override-colors; }`

Defines custom font palettes.

**Values:**
- `font-family: "Color Font"` — the font to apply the palette to
- `base-palette: 0` — start from the font's palette index 0
- `override-colors: 0 #ff6b6b, 1 #feca57` — override specific palette colors
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Define reusable color palettes
- Override specific glyph colors

**Example:**
```css
@font-palette-values --rainbow {
  font-family: "Color Font";
  base-palette: 0;
  override-colors:
    0 #ff6b6b,
    1 #feca57,
    2 #48dbfb,
    3 #ff9ff3;
}
```

---

## Typography Details

---

## font-variant-position

**Syntax:** `font-variant-position: normal | super | sub`

Uses alternate glyphs for superscript and subscript.

**Values:**
- `normal` — no superscript or subscript positioning (default)
- `super` — use superscript glyphs
- `sub` — use subscript glyphs
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Style footnotes and exponents
- Avoid line-height shifts from sup and sub elements

**Example:**
```css
sup {
  font-variant-position: super;
}

sub {
  font-variant-position: sub;
}
```

---

## initial-letter

**Syntax:** `initial-letter: <number> | normal`

Makes the first letter large and floated.

**Values:**
- `normal` — no initial letter (default)
- `3` — drop the first letter across 3 lines
- `2 1` — height 2 lines, sink 1 line
- `3 2` — height 3 lines, sink 2 lines
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create drop caps for articles
- Add editorial emphasis to paragraphs

**Example:**
```css
p:first-of-type::first-letter {
  initial-letter: 3;
  font-weight: bold;
  color: #667eea;
}
```

---

## hyphenate-limit-chars

**Syntax:** `hyphenate-limit-chars: <number> <number> <number>`

Controls the minimum number of characters for hyphenation.

**Values:**
- `6 3 2` — minimum 6 before, 3 after, 2 per word
- `auto` — browser decides the limits (default)
- `4` — minimum 4 characters per word
- `5 2` — minimum 5 before and 2 after a hyphen
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Control hyphenation density
- Prevent awkward hyphen breaks

**Example:**
```css
p {
  hyphens: auto;
  hyphenate-limit-chars: 6 3 2;
}
```

---

**[View Example](../examples/advanced/22-typography-2024/index.html)**

← **Previous Topic:** [Advanced Color Functions](../advanced/21-color-functions-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Advanced Math Functions](../advanced/23-advanced-math-functions.md) →

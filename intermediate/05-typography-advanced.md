# Typography Advanced

> 13 properties

Fine-tune fonts and text rendering with advanced typography properties.

---

## Font

---

## font-family

**Syntax:** `font-family: <family-name> | <generic-family>`

Typeface stack — fallback fonts listed in priority order.

**Values:**
- `serif` — generic serif family
- `sans-serif` — generic sans-serif family
- `monospace` — generic monospace family
- `system-ui` — system's default UI font
- `"Helvetica Neue", Arial, sans-serif` — fallback stack
- `inherit` — inherits from parent
- `initial` — sets to default (user agent)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Set fallback font stacks
- Use system fonts for performance

**Example:**
```css
body {
  font-family: "Helvetica Neue", Arial, sans-serif;
}

code {
  font-family: ui-monospace, monospace;
}
```

---

## font-size

**Syntax:** `font-size: <length> | <percentage> | <absolute-size> | <relative-size>`

Text size — sets the computed size of font glyphs.

**Values:**
- `16px` — fixed pixel size
- `1.2em` — relative to parent font size
- `1.5rem` — relative to root font size
- `120%` — percentage of parent
- `medium` — default size (1rem)
- `larger` — one step larger than parent
- `inherit` — inherits from parent
- `initial` — sets to default (medium)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Set a base text size
- Scale headings with rem for accessibility

**Example:**
```css
body {
  font-size: 16px;
}

h1 {
  font-size: 2rem;
}
```

---

## font-weight

**Syntax:** `font-weight: <number> | normal | bold | bolder | lighter`

Thickness — 100 (thin) to 900 (black), or normal/bold.

**Values:**
- `100` — thin
- `300` — light
- `400` — normal (default)
- `700` — bold
- `900` — black
- `bold` — bold keyword
- `bolder` — relative to parent weight
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Emphasize headings
- Create a clear type hierarchy

**Example:**
```css
strong {
  font-weight: 700;
}

.light {
  font-weight: 300;
}
```

---

## font-style

**Syntax:** `font-style: normal | italic | oblique <angle>?`

Style variant — normal, italic, or oblique with optional angle.

**Values:**
- `normal` — upright text (default)
- `italic` — slanted italic text
- `oblique` — synthetically slanted text
- `oblique 14deg` — oblique with angle
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Emphasize quotes and citations
- Distinguish special text from body copy

**Example:**
```css
blockquote {
  font-style: italic;
}

.emphatic {
  font-style: oblique 14deg;
}
```

---

## font-variation-settings

**Syntax:** `font-variation-settings: normal | <string> <number>#`

Variable font axes — fine-tunes optical size, weight, width, etc.

**Values:**
- `normal` — no variation applied (default)
- `'wght' 750` — weight axis
- `'opsz' 36` — optical size axis
- `'wght' 750, 'opsz' 36` — multiple axes
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Control variable font axes
- Fine-tune weight without extra font files

**Example:**
```css
.headline {
  font-variation-settings: 'wght' 750, 'opsz' 36;
}
```

---

## font-optical-sizing

**Syntax:** `font-optical-sizing: auto | none`

Auto-adjusts optical size axis for legibility at different sizes.

**Values:**
- `auto` — adjust optical size automatically (default)
- `none` — no optical size adjustment
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Keep text legible at small sizes
- Use with variable fonts that support optical size

**Example:**
```css
body {
  font-optical-sizing: auto;
}
```

---

## font-synthesis

**Syntax:** `font-synthesis: none | weight | style | weight style`

Controls synthetic styles — which bold/italic the browser can fake.

**Values:**
- `weight style` — allow synthetic bold and italic (default)
- `none` — no fake bold or italic
- `weight` — allow synthetic bold only
- `style` — allow synthetic italic only
- `inherit` — inherits from parent
- `initial` — sets to default (weight style)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Prevent fake bold/italic for custom fonts
- Keep typography crisp on serif fonts

**Example:**
```css
.body {
  font-synthesis: none;
}
```

---

## font

**Syntax:** `font: <style> <weight> <size>/<line-height> <family>`

Shorthand — sets size, weight, style, and family in one declaration.

**Values:**
- `700 1.2rem/1.4 'Inter', sans-serif` — full shorthand
- `16px sans-serif` — size and family
- `italic bold 1rem Georgia` — style, weight, size, family
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Set typography in one line
- Reset inherited font styles

**Example:**
```css
body {
  font: 700 1.2rem/1.4 "Inter", sans-serif;
}
```

---

## font-kerning

**Syntax:** `font-kerning: auto | normal | none`

Controls whether kerning pairs are applied.

**Values:**
- `auto` — browser decides whether to kern (default)
- `normal` — always apply kerning
- `none` — never apply kerning

**Use Cases:**
- Improve large display text
- Tighten small headings

**Example:**
```css
h1 {
  font-kerning: normal;
}
```

---

## font-stretch

**Syntax:** `font-stretch: normal | <keyword> | <percentage>`

Selects a wider or narrower face of a font family.

**Values:**
- `normal` — regular width (default)
- `condensed` / `semi-condensed` — narrower faces
- `expanded` / `semi-expanded` — wider faces
- `font-stretch: 125%` — percentage width

**Use Cases:**
- Pick a condensed headline face
- Fit more text in a fixed space

**Example:**
```css
.headline {
  font-stretch: condensed;
}
```

---

## Text

---

## color

**Syntax:** `color: <color>`

Foreground color — sets text and decoration color.

**Values:**
- `red` — named color
- `#ff5733` — hex color
- `rgb(255, 0, 0)` — RGB color
- `rgba(255, 0, 0, 0.5)` — RGB with alpha
- `hsl(0, 100%, 50%)` — HSL color
- `transparent` — fully transparent
- `currentColor` — matches current text color
- `inherit` — inherits from parent
- `initial` — sets to default (user agent)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Set text color
- Match text to brand colors

**Example:**
```css
body {
  color: #333;
}

.link {
  color: hsl(210, 100%, 40%);
}
```

---

## word-spacing

**Syntax:** `word-spacing: normal | <length>`

Controls the spacing between words.

**Values:**
- `normal` — use the font's normal word spacing (default)
- `0.5em` — half-em extra space between words
- `-2px` — tighten word spacing

**Use Cases:**
- Loosen or tighten word spacing in headings
- Emphasize or de-emphasize text blocks

**Example:**
```css
.headline {
  word-spacing: 0.25em;
}
```

---

## vertical-align

**Syntax:** `vertical-align: baseline | sub | super | top | bottom | middle | <length> | <percentage>`

Aligns inline-level content and table cells vertically.

**Values:**
- `baseline` — align to the text baseline (default)
- `middle` — center the box on the parent baseline
- `top` / `bottom` — align to the line box top or bottom
- `sub` / `super` — align like subscript or superscript
- `20px` — offset from the baseline by a length

**Use Cases:**
- Align images and icons with surrounding text
- Vertically center content in table cells

**Example:**
```css
.icon {
  vertical-align: middle;
}

td {
  vertical-align: top;
}
```

---

**[View Example](../examples/intermediate/05-typography-advanced/index.html)**

← **Previous Topic:** [Image Sizing](../intermediate/04-image-sizing.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Text Decoration](../intermediate/06-text-decoration.md) →


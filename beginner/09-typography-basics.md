# Typography Basics

> 15 properties

Font families, sizes, weights, text decoration, alignment, and spacing.

---

## Font

---

## font-family

**Syntax:** `font-family: <family-list>`

Typeface stack — fallback fonts listed in priority order.

**Values:**
- `serif` — serif typefaces
- `sans-serif` — sans-serif typefaces
- `monospace` — monospaced typefaces
- `cursive` — cursive typefaces
- `fantasy` — decorative typefaces
- `system-ui` — system default UI font
- `"Helvetica Neue", Arial, sans-serif` — specific font stack
- `inherit` — inherits from parent
- `initial` — sets to default (user agent)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Set consistent typography across a site
- Provide fallback fonts for cross-platform compatibility

**Example:**
```css
body {
  font-family: 'Inter', system-ui, sans-serif;
}
```

---

## font-size

**Syntax:** `font-size: <length> | <percentage> | <keyword>`

Text size — sets the computed size of font glyphs.

**Values:**
- `xx-small` — extra extra small
- `x-small` — extra small
- `small` — small
- `medium` — medium (default)
- `large` — large
- `x-large` — extra large
- `xx-large` — extra extra large
- `smaller` — smaller than parent
- `larger` — larger than parent
- `16px` — absolute pixel size
- `1.2em` — relative to parent font
- `1.5rem` — relative to root font
- `100%` — same as parent
- `inherit` — inherits from parent
- `initial` — sets to default (medium)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Set base font size on body
- Create typographic scale for headings

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

**Syntax:** `font-weight: <number> | normal | bold | lighter | bolder`

Thickness — 100 (thin) to 900 (black), or normal/bold.

**Values:**
- `100` — thin
- `200` — extra light
- `300` — light
- `400` — normal (default)
- `500` — medium
- `600` — semi-bold
- `700` — bold
- `800` — extra bold
- `900` — black
- `normal` — same as 400
- `bold` — same as 700
- `lighter` — lighter than parent
- `bolder` — bolder than parent
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Emphasize headings with bold weights
- Create subtle hierarchy with light/medium weights

**Example:**
```css
h1 {
  font-weight: 700;
}

.caption {
  font-weight: 300;
}
```

---

## font-style

**Syntax:** `font-style: normal | italic | oblique`

Style variant — normal, italic, or oblique with optional angle.

**Values:**
- `normal` — upright text (default)
- `italic` — italic typeface
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Italicize emphasis text
- Style quotes or citations

**Example:**
```css
 em {
  font-style: italic;
}

.quote {
  font-style: italic;
}
```

---

## font

**Syntax:** `font: <style> <weight> <size>/<line-height> <family>`

Shorthand — sets size, weight, style, and family in one declaration.

**Values:**
- `700 1.2rem/1.4 'Inter', sans-serif` — weight size/line-height family
- `italic 1rem Georgia, serif` — style size family
- `inherit` — inherits from parent
- `initial` — sets to default
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Simplify font declarations
- Set multiple font properties at once

**Example:**
```css
body {
  font: 400 1rem/1.5 'Inter', system-ui, sans-serif;
}
```

---

## text-align

**Syntax:** `text-align: left | right | center | justify | start | end`

Horizontal alignment — left, right, center, or justify within the line box.

**Values:**
- `left` — align to left edge
- `right` — align to right edge
- `center` — center horizontally
- `justify` — stretch lines to fill width
- `start` — align to start edge (left in LTR)
- `end` — align to end edge (right in LTR)
- `match-parent` — inherit with direction
- `inherit` — inherits from parent
- `initial` — sets to default (start)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center headings and buttons
- Justify paragraphs for print-like layouts

**Example:**
```css
h1 {
  text-align: center;
}

p {
  text-align: justify;
}
```

---

## text-decoration

**Syntax:** `text-decoration: none | underline | overline | line-through`

Line decoration — underline, overline, or line-through with style and color.

**Values:**
- `none` — no decoration (default)
- `underline` — line under text
- `overline` — line above text
- `line-through` — line through text
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Remove default link underlines
- Add strikethrough to discounted prices

**Example:**
```css
a {
  text-decoration: none;
}

.discount {
  text-decoration: line-through;
}
```

---

## text-transform

**Syntax:** `text-transform: none | capitalize | uppercase | lowercase | full-width`

Case transformation — uppercase, lowercase, capitalize.

**Values:**
- `none` — no transformation (default)
- `capitalize` — capitalize first letter of each word
- `uppercase` — transform to ALL CAPS
- `lowercase` — transform to all lowercase
- `full-width` — full-width characters
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create consistent button labels
- Style navigation menus

**Example:**
```css
.button {
  text-transform: uppercase;
}

.nav-link {
  text-transform: capitalize;
}
```

---

## line-height

**Syntax:** `line-height: <number> | <length> | <percentage> | normal`

Line spacing — controls the distance between lines of text.

**Values:**
- `normal` — browser default (usually ~1.2)
- `1.5` — 1.5x font size
- `24px` — fixed pixel height
- `150%` — 150% of font size
- `1` — no extra spacing
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Improve readability of body text
- Create vertical rhythm in typography

**Example:**
```css
body {
  line-height: 1.6;
}

h1 {
  line-height: 1.2;
}
```

---

## letter-spacing

**Syntax:** `letter-spacing: <length> | normal`

Character spacing — adjusts space between letters.

**Values:**
- `normal` — default spacing (default)
- `0.05em` — add slight spacing
- `2px` — fixed pixel spacing
- `-0.02em` — tighten spacing
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Improve readability of uppercase text
- Create elegant headings

**Example:**
```css
.heading {
  letter-spacing: 0.05em;
}

.uppercase {
  letter-spacing: 0.1em;
}
```

---

## text-indent

**Syntax:** `text-indent: <length> | <percentage>`

First-line indent — offsets the first line of a block.

**Values:**
- `2em` — indent by 2em
- `20px` — fixed pixel indent
- `10%` — percentage of container width
- `each-line` — indent each line
- `0` — no indent (default)
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create traditional paragraph indentation
- Style blockquotes

**Example:**
```css
p {
  text-indent: 2em;
}
```

---

## white-space

**Syntax:** `white-space: normal | nowrap | pre | pre-wrap | pre-line | break-spaces`

Whitespace handling — controls line breaks and space collapsing.

**Values:**
- `normal` — collapses spaces, wraps (default)
- `nowrap` — no wrapping
- `pre` — preserves whitespace, no wrap
- `pre-wrap` — preserves whitespace, wraps
- `pre-line` — preserves newlines, wraps
- `break-spaces` — preserves spaces, wraps
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Prevent text wrapping in buttons
- Display preformatted text

**Example:**
```css
.button-text {
  white-space: nowrap;
}

.code {
  white-space: pre;
}
```

---

**[View Example](../examples/beginner/09-typography-basics/index.html)**

← **Previous Topic:** [Background Basics](../beginner/08-background-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Border Basics](../beginner/10-border-basics.md) →


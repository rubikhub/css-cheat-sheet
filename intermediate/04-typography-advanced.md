# Typography Advanced

> 28 properties

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

## text-align

**Syntax:** `text-align: left | right | center | justify | start | end`

Horizontal alignment — left, right, center, or justify within the line box.

**Values:**
- `start` — align to line start (default)
- `left` — align left
- `right` — align right
- `center` — center text
- `justify` — stretch lines edge to edge
- `end` — align to line end
- `inherit` — inherits from parent
- `initial` — sets to default (start)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center headings
- Justify body text

**Example:**
```css
h1 {
  text-align: center;
}

.article {
  text-align: justify;
}
```

---

## text-align-last

**Syntax:** `text-align-last: auto | start | end | left | right | center | justify`

Alignment of the last line — useful for justify blocks.

**Values:**
- `auto` — uses the text-align value (default)
- `center` — center the last line
- `left` — align the last line left
- `right` — align the last line right
- `justify` — justify the last line
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Center the last line of justified text
- Align the last line in centered blocks

**Example:**
```css
p {
  text-align: justify;
  text-align-last: center;
}
```

---

## text-decoration

**Syntax:** `text-decoration: none | <line> <style> <color>`

Line decoration — underline, overline, or line-through with style and color.

**Values:**
- `none` — no decoration (default)
- `underline` — line under text
- `overline` — line above text
- `line-through` — line through text
- `underline wavy red` — shorthand with style and color
- `underline dotted` — shorthand with style
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Style link underlines
- Add emphasis with strike-through

**Example:**
```css
a {
  text-decoration: underline wavy #0066cc;
}
```

---

## text-decoration-line

**Syntax:** `text-decoration-line: none | underline | overline | line-through`

Which lines to decorate — underline, overline, line-through.

**Values:**
- `none` — no decoration (default)
- `underline` — line under text
- `overline` — line above text
- `line-through` — line through text
- `underline overline` — multiple lines
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add underlines to links
- Combine lines for emphasis

**Example:**
```css
a {
  text-decoration-line: underline;
}

del {
  text-decoration-line: line-through;
}
```

---

## text-decoration-style

**Syntax:** `text-decoration-style: solid | double | dotted | dashed | wavy`

Decoration style — solid, dashed, dotted, double, wavy.

**Values:**
- `solid` — solid line (default)
- `dashed` — dashed line
- `dotted` — dotted line
- `double` — double line
- `wavy` — wavy line
- `inherit` — inherits from parent
- `initial` — sets to default (solid)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add wavy underlines for warnings
- Style link underlines

**Example:**
```css
.warning {
  text-decoration-line: underline;
  text-decoration-style: wavy;
  text-decoration-color: #d32f2f;
}
```

---

## text-decoration-color

**Syntax:** `text-decoration-color: <color>`

Decoration color — independent of text color.

**Values:**
- `currentColor` — matches text color (default)
- `red` — named color
- `#a3a3a3` — hex color
- `inherit` — inherits from parent
- `initial` — sets to default (currentColor)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Highlight links with colored underlines
- Match decoration to brand colors

**Example:**
```css
a {
  text-decoration: underline;
  text-decoration-color: #0066cc;
}
```

---

## text-decoration-thickness

**Syntax:** `text-decoration-thickness: auto | from-font | <length> | <percentage>`

Thickness of the decoration line — precise control over underline weight.

**Values:**
- `auto` — browser-determined thickness (default)
- `from-font` — use the font's specified thickness
- `1px` — thin line
- `3px` — thick line
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Make underlines thinner or bolder
- Keep underline weight consistent

**Example:**
```css
a {
  text-decoration: underline;
  text-decoration-thickness: 2px;
}
```

---

## text-underline-offset

**Syntax:** `text-underline-offset: auto | from-font | <length> | <percentage>`

Distance from baseline to underline — adjusts underline position.

**Values:**
- `auto` — default position (default)
- `from-font` — use the font's specified offset
- `1px` — close to text
- `4px` — small gap
- `8px` — far from text
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add breathing room under underlined links
- Align underlines with descenders

**Example:**
```css
a {
  text-decoration: underline;
  text-underline-offset: 4px;
}
```

---

## text-transform

**Syntax:** `text-transform: none | capitalize | uppercase | lowercase | full-width`

Case transformation — uppercase, lowercase, capitalize.

**Values:**
- `none` — no transformation (default)
- `capitalize` — capitalize each word
- `uppercase` — all uppercase
- `lowercase` — all lowercase
- `full-width` — full-width characters
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Style buttons and badges in uppercase
- Normalize user input casing

**Example:**
```css
button {
  text-transform: uppercase;
}

h1 {
  text-transform: capitalize;
}
```

---

## text-indent

**Syntax:** `text-indent: <length> | <percentage>`

First-line indent — offsets the first line of a block.

**Values:**
- `0` — no indent (default)
- `2em` — indent relative to font size
- `20px` — fixed indent
- `10%` — percentage of container width
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Format paragraphs in print styles
- Indent opening lines of text blocks

**Example:**
```css
p {
  text-indent: 2em;
}
```

---

## text-overflow

**Syntax:** `text-overflow: clip | ellipsis`

Overflow behavior — clip or ellipsis for truncated text.

**Values:**
- `clip` — hard cut-off (default)
- `ellipsis` — trailing three dots
- `inherit` — inherits from parent
- `initial` — sets to default (clip)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Truncate long titles with an ellipsis
- Keep single-line labels from overflowing

**Example:**
```css
.title {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
}
```

---

## text-shadow

**Syntax:** `text-shadow: none | <offset-x> <offset-y> <blur> <color>`

Text shadow — adds drop shadow effect to text.

**Values:**
- `none` — no shadow (default)
- `2px 2px #555` — offset shadow
- `1px 1px 2px rgba(0,0,0,0.5)` — shadow with blur and alpha
- `0 2px 6px #333, 0 0 12px #999` — multiple shadows
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add depth to headings
- Create glow effects

**Example:**
```css
h1 {
  text-shadow: 1px 1px 2px rgba(0, 0, 0, 0.5);
}
```

---

## text-wrap

**Syntax:** `text-wrap: wrap | nowrap | balance | pretty`

Wrapping mode — normal, wrap (balanced), pretty, or nowrap.

**Values:**
- `wrap` — wrap at allowed break points (default)
- `nowrap` — no wrapping
- `balance` — balance line lengths
- `pretty` — minimize orphans and ragged edges
- `inherit` — inherits from parent
- `initial` — sets to default (wrap)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Balance heading lines
- Avoid orphaned words in paragraphs

**Example:**
```css
h2 {
  text-wrap: balance;
}
```

---

## white-space

**Syntax:** `white-space: normal | nowrap | pre | pre-wrap | pre-line | break-spaces`

Whitespace handling — controls line breaks and space collapsing.

**Values:**
- `normal` — collapse spaces, wrap at width (default)
- `nowrap` — no wrapping
- `pre` — preserve whitespace, no wrapping
- `pre-wrap` — preserve whitespace, wrap
- `pre-line` — collapse spaces, keep line breaks
- `break-spaces` — preserve breaks and spaces
- `inherit` — inherits from parent
- `initial` — sets to default (normal)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Preserve code formatting
- Prevent wrapping in UI labels

**Example:**
```css
pre {
  white-space: pre;
}

.tag {
  white-space: nowrap;
}
```

---

## word-break

**Syntax:** `word-break: normal | break-all | keep-all | auto-phrase`

Controls where line-breaking happens within words.

**Values:**
- `normal` — default line breaking rules (default)
- `break-all` — break between any characters
- `keep-all` — no breaks between CJK words
- `auto-phrase` — break at phrase boundaries

**Use Cases:**
- Wrap long URLs and code tokens
- Handle CJK text correctly

**Example:**
```css
.url {
  word-break: break-all;
}

.cjk {
  word-break: keep-all;
}
```

---

## tab-size

**Syntax:** `tab-size: <integer> | <length>`

Sets the width of a tab character.

**Values:**
- `tab-size: 4` — four spaces per tab
- `tab-size: 2` — two spaces per tab
- `tab-size: 8` — default tab width

**Use Cases:**
- Control indentation width in pre blocks

**Example:**
```css
pre {
  tab-size: 2;
}
```

---

## line-clamp

**Syntax:** `line-clamp: none | <integer>`

Limits text to a number of lines and truncates with an ellipsis.

**Values:**
- `none` — no clamping (default)
- `line-clamp: 2` — max two lines
- `line-clamp: 3` — max three lines
- legacy pattern — `display: -webkit-box; -webkit-line-clamp: 3; -webkit-box-orient: vertical`

**Use Cases:**
- Truncate card titles and previews

**Example:**
```css
.title {
  overflow: hidden;
  text-overflow: ellipsis;
  line-clamp: 2;
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

**[View Example](../examples/intermediate/04-typography-advanced/index.html)**

← **Previous Topic:** [Background Advanced](../intermediate/03-background-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Border Advanced](../intermediate/05-border-advanced.md) →

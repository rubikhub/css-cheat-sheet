# Text Layout & Wrapping

> 18 properties

Text alignment, wrapping, and overflow behavior.

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

## text-justify

**Syntax:** `text-justify: auto | none | inter-word | inter-character`

Controls how justified text is spaced.

**Values:**
- `auto` — browser picks the best method (default)
- `none` — no justification, like text-align: left
- `inter-word` — justify by adding space between words
- `inter-character` — justify by adding space between characters (CJK)

**Use Cases:**
- Fine-tune justification for CJK text
- Avoid stretched spacing in narrow columns

**Example:**
```css
.cjk {
  text-align: justify;
  text-justify: inter-character;
}
```

---

## line-break

**Syntax:** `line-break: auto | loose | normal | strict | anywhere`

Controls line breaking rules for CJK and punctuation.

**Values:**
- `auto` — browser default rules (default)
- `loose` — relaxed rules, less strict breaks
- `normal` — standard breaking rules
- `strict` — stricter rules for punctuation
- `anywhere` — break between any characters

**Use Cases:**
- Control where CJK text wraps
- Prevent punctuation from breaking rules

**Example:**
```css
.japanese {
  line-break: strict;
}
```

---

## white-space-collapse

**Syntax:** `white-space-collapse: collapse | preserve | preserve-breaks | preserve-spaces | break-spaces`

Longhand of white-space controlling how whitespace sequences collapse.

**Values:**
- `collapse` — collapse spaces and line breaks (default)
- `preserve` — keep spaces and line breaks
- `preserve-breaks` — keep line breaks, collapse spaces
- `preserve-spaces` — keep spaces, collapse line breaks
- `break-spaces` — preserve everything and allow breaks

**Use Cases:**
- Replace white-space shorthand with composable longhands
- Keep newlines without preserving spaces

**Example:**
```css
.code {
  white-space-collapse: preserve;
  text-wrap-mode: wrap;
}
```

---

## text-wrap-mode

**Syntax:** `text-wrap-mode: wrap | nowrap`

Longhand of text-wrap controlling whether text wraps at all.

**Values:**
- `wrap` — text wraps at soft wrap opportunities (default)
- `nowrap` — text does not wrap

**Use Cases:**
- Control wrapping independently of text-wrap-style
- Replace white-space: nowrap with composable longhands

**Example:**
```css
.tag {
  text-wrap-mode: nowrap;
}
```

---

## text-wrap-style

**Syntax:** `text-wrap-style: auto | balance | pretty | stable`

Longhand of text-wrap controlling the wrapping algorithm.

**Values:**
- `auto` — browser default wrapping (default)
- `balance` — balance line lengths across the block
- `pretty` — minimize orphans and ragged right edges
- `stable` — keep wrapping stable while editing

**Use Cases:**
- Balance headings without affecting nowrap behavior
- Improve paragraphs without balancing everywhere

**Example:**
```css
h2 {
  text-wrap-style: balance;
}

p {
  text-wrap-style: pretty;
}
```

---

## hyphens

**Syntax:** `hyphens: none | manual | auto`

Controls hyphenation of words at line breaks.

**Values:**
- `none` — no hyphenation (default)
- `manual` — hyphenate only at explicit hyphens
- `auto` — hyphenate automatically (needs lang attribute)

**Use Cases:**
- Hyphenate justified text for tighter lines
- Improve narrow-column typography

**Example:**
```css
article {
  hyphens: auto;
  text-align: justify;
}
```

---

## hyphenate-character

**Syntax:** `hyphenate-character: auto | <string>`

Sets the character used at hyphenation break points.

**Values:**
- `auto` — use the language-appropriate hyphen (default)
- `"-"` — a plain hyphen
- `"·"` — middle dot

**Use Cases:**
- Customize the visible hyphen glyph
- Use a preferred break mark for a language

**Example:**
```css
p {
  hyphens: auto;
  hyphenate-character: "‑";
}
```

---

**[View Example](../examples/intermediate/07-text-layout/index.html)**

← **Previous Topic:** [Text Decoration](../intermediate/06-text-decoration.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Border Advanced](../intermediate/08-border-advanced.md) →


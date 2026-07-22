# Typography Advanced
---
## Font
### font-family
**Type/Initial:** family list | (user agent)

**Description:** Typeface stack — fallback fonts listed in priority order.

**CSS:**
```css
/* Generic families */
font-family: serif;
font-family: sans-serif;
font-family: monospace;
font-family: cursive;
font-family: fantasy;
font-family: system-ui;
font-family: ui-serif;
font-family: ui-sans-serif;
font-family: ui-monospace;
font-family: ui-rounded;

/* Specific font names */
font-family: "Helvetica Neue", Arial, sans-serif;

/* Global values */
font-family: inherit;
font-family: initial;
font-family: revert;
font-family: unset;
```

**HTML:**
```html
<div class="db style-a">
  <div class="style-b">
    Inter, system-ui, sans-serif
  </div>
  <div class="style-c">
    Georgia, 'Times New Roman', serif
  </div>
  <div class="style-d">
    SF Mono, Consolas, monospace
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.3rem;
}
.style-b {
  font-family: 'Inter', system-ui, sans-serif;
  color: #333;
  font-size: 0.9rem;
}
.style-c {
  font-family: Georgia, 'Times New Roman', serif;
  color: #333;
  font-size: 0.9rem;
}
.style-d {
  font-family: 'SF Mono', 'Cascadia Code', Consolas, monospace;
  color: #333;
  font-size: 0.9rem;
}
```

### font-size
**Type/Initial:** length | % | medium

**Description:** Text size — sets the computed size of font glyphs.

**CSS:**
```css
/* Absolute size keywords */
font-size: xx-small;
font-size: x-small;
font-size: small;
font-size: medium;
font-size: large;
font-size: x-large;
font-size: xx-large;

/* Relative size keywords */
font-size: smaller;
font-size: larger;

/* Length values */
font-size: 16px;
font-size: 1.2em;
font-size: 1.5rem;

/* Percentage values */
font-size: 100%;
font-size: 120%;

/* Global values */
font-size: inherit;
font-size: initial;
font-size: revert;
font-size: unset;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    0.75rem — small text
  </span>
  <span class="style-c">
    1rem — base text
  </span>
  <span class="style-d">
    1.5rem — large text
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
}
.style-b {
  font-size: 0.75rem;
  color: #333;
}
.style-c {
  font-size: 1rem;
  color: #333;
}
.style-d {
  font-size: 1.5rem;
  color: #333;
}
```

### font-weight
**Type/Initial:** number | keyword | normal

**Description:** Thickness — 100 (thin) to 900 (black), or normal/bold.

**CSS:**
```css
/* Numeric values */
font-weight: 100;
font-weight: 200;
font-weight: 300;
font-weight: 400;
font-weight: 500;
font-weight: 600;
font-weight: 700;
font-weight: 800;
font-weight: 900;

/* Keyword values */
font-weight: normal;
font-weight: bold;
font-weight: lighter;
font-weight: bolder;

/* Global values */
font-weight: inherit;
font-weight: initial;
font-weight: revert;
font-weight: unset;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    100 Thin
  </span>
  <span class="style-c">
    300 Light
  </span>
  <span class="style-d">
    400 Normal
  </span>
  <span class="style-e">
    600 Semi-bold
  </span>
  <span class="style-f">
    700 Bold
  </span>
  <span class="style-g">
    900 Black
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.15rem;
}
.style-b {
  font-weight: 100;
  color: #333;
  font-size: 0.9rem;
}
.style-c {
  font-weight: 300;
  color: #333;
  font-size: 0.9rem;
}
.style-d {
  font-weight: 400;
  color: #333;
  font-size: 0.9rem;
}
.style-e {
  font-weight: 600;
  color: #333;
  font-size: 0.9rem;
}
.style-f {
  font-weight: 700;
  color: #333;
  font-size: 0.9rem;
}
.style-g {
  font-weight: 900;
  color: #333;
  font-size: 0.9rem;
}
```

### font-style
**Type/Initial:** keyword | normal

**Description:** Style variant — normal, italic, or oblique with optional angle.

**CSS:**
```css
font-style: normal;
font-style: italic;
font-style: oblique;
font-style: oblique 14deg;  /* with angle */

font-style: inherit;
font-style: initial;
font-style: revert;
font-style: unset;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    normal
  </span>
  <span class="style-c">
    italic
  </span>
  <span class="style-d">
    oblique 12deg
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  gap: 0.8rem;
  flex-wrap: wrap;
}
.style-b {
  font-style: normal;
  color: #333;
  font-size: 0.9rem;
}
.style-c {
  font-style: italic;
  color: #333;
  font-size: 0.9rem;
}
.style-d {
  font-style: oblique 12deg;
  color: #333;
  font-size: 0.9rem;
}
```

### font-variation-settings
**Type/Initial:** string | normal

**Description:** Variable font axes — fine-tunes optical size, weight, width, etc.

**CSS:**
```css
font-variation-settings: 'wght' 750, 'opsz' 36;
```

**HTML:**
```html
<div class="db">
  <span class="style-a">
    wght 750 — variable font weight axis
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  font-variation-settings: 'wght' 750;
  color: #333;
  font-size: 1rem;
}
```

### font-optical-sizing
**Type/Initial:** keyword | auto

**Description:** Auto-adjusts optical size axis for legibility at different sizes.

**CSS:**
```css
font-optical-sizing: auto;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    0.7rem auto
  </span>
  <span class="style-c">
    1.4rem auto
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  gap: 0.8rem;
  align-items: baseline;
}
.style-b {
  font-optical-sizing: auto;
  color: #333;
  font-size: 0.7rem;
}
.style-c {
  font-optical-sizing: auto;
  color: #333;
  font-size: 1.4rem;
}
```

### font-synthesis
**Type/Initial:** keyword list | weight style

**Description:** Controls synthetic styles — which bold/italic the browser can fake.

**CSS:**
```css
font-synthesis: none; /* no fake bold/italic */
font-synthesis: weight; /* fake bold only */
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    none — no synthesis
  </span>
  <span class="style-c">
    weight — bold synthesis
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  gap: 0.8rem;
  flex-wrap: wrap;
}
.style-b {
  font-synthesis: none;
  color: #333;
  font-size: 0.85rem;
}
.style-c {
  font-synthesis: weight;
  color: #333;
  font-size: 0.85rem;
}
```

### font
**Type/Initial:** shorthand | —

**Description:** Shorthand — sets size, weight, style, and family in one declaration.

**CSS:**
```css
font: 700 1.2rem/1.4 'Inter', sans-serif;
```

**HTML:**
```html
<div class="db">
  <span class="style-a">
    font: 700 1.2rem/1.4 'Inter', sans-serif
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  font: 700 1.2rem/1.4 'Inter', sans-serif;
  color: #333;
}
```

## Text
### color
**Type/Initial:** color | (user agent)

**Description:** Foreground color — sets text and decoration color.

**CSS:**
```css
/* Keyword values */
color: currentColor;

/* Named colors */
color: red;
color: transparent;

/* Hex */
color: #ff5733;
color: #f00;

/* RGB */
color: rgb(255, 0, 0);
color: rgba(255, 0, 0, 0.5);

/* HSL */
color: hsl(0, 100%, 50%);
color: hsla(0, 100%, 50%, 0.5);

/* Global values */
color: inherit;
color: initial;
color: revert;
color: unset;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    #fff
  </span>
  <span class="style-c">
    #000
  </span>
  <span class="style-d">
    #525252
  </span>
  <span class="style-e">
    #737373
  </span>
  <span class="style-f">
    #a3a3a3
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  gap: 0.6rem;
  flex-wrap: wrap;
}
.style-b {
  color: #fff;
}
.style-c {
  color: #000;
}
.style-d {
  color: #525252;
}
.style-e {
  color: #737373;
}
.style-f {
  color: #a3a3a3;
}
```

### text-align
**Type/Initial:** keyword | start

**Description:** Horizontal alignment — left, right, center, or justify within the line box.

**CSS:**
```css
text-align: left;
text-align: right;
text-align: center;
text-align: justify;
text-align: justify-all;
text-align: start;
text-align: end;
text-align: match-parent;

text-align: inherit;
text-align: initial;
text-align: revert;
text-align: unset;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    ← left aligned
  </span>
  <span class="style-c">
    center aligned →
  </span>
  <span class="style-d">
    right aligned →
  </span>
  <span class="style-e">
    This long sentence is justified so the edges line up neatly on both sides of the line box.
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
  font-size: 0.85rem;
}
.style-b {
  text-align: left;
  color: #333;
}
.style-c {
  text-align: center;
  color: #333;
}
.style-d {
  text-align: right;
  color: #333;
}
.style-e {
  text-align: justify;
  color: #333;
}
```

### text-align-last
**Type/Initial:** keyword | auto

**Description:** Alignment of the last line — useful for justify blocks.

**CSS:**
```css
text-align: justify;
text-align-last: center;
```

**HTML:**
```html
<div class="db">
  <div class="style-a">
    This justified paragraph has its last line centered instead of following the full justify alignment of the previous lines above.
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  text-align: justify;
  text-align-last: center;
  color: #333;
  font-size: 0.85rem;
}
```

### text-decoration
**Type/Initial:** shorthand | none

**Description:** Line decoration — underline, overline, or line-through with style and color.

**CSS:**
```css
/* None */
text-decoration: none;

/* Line values */
text-decoration: underline;
text-decoration: overline;
text-decoration: line-through;

/* Shorthand */
text-decoration: underline wavy red;
text-decoration: underline dotted;

text-decoration: inherit;
text-decoration: initial;
text-decoration: revert;
text-decoration: unset;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    underline solid
  </span>
  <span class="style-c">
    underline wavy
  </span>
  <span class="style-d">
    line-through
  </span>
  <span class="style-e">
    overline
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
  font-size: 0.9rem;
}
.style-b {
  text-decoration: underline;
  color: #333;
}
.style-c {
  text-decoration: underline wavy #525252;
  color: #333;
}
.style-d {
  text-decoration: line-through;
  color: #333;
}
.style-e {
  text-decoration: overline #737373;
  color: #333;
}
```

### text-decoration-line
**Type/Initial:** keyword | none

**Description:** Which lines to decorate — underline, overline, line-through.

**CSS:**
```css
text-decoration-line: underline overline;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    underline
  </span>
  <span class="style-c">
    overline
  </span>
  <span class="style-d">
    both
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  gap: 0.8rem;
  flex-wrap: wrap;
  font-size: 0.9rem;
}
.style-b {
  text-decoration-line: underline;
  color: #333;
}
.style-c {
  text-decoration-line: overline;
  color: #333;
}
.style-d {
  text-decoration-line: underline overline;
  color: #333;
}
```

### text-decoration-style
**Type/Initial:** keyword | solid

**Description:** Decoration style — solid, dashed, dotted, double, wavy.

**CSS:**
```css
text-decoration-style: wavy;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    solid
  </span>
  <span class="style-c">
    dashed
  </span>
  <span class="style-d">
    dotted
  </span>
  <span class="style-e">
    double
  </span>
  <span class="style-f">
    wavy
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
  font-size: 0.9rem;
}
.style-b {
  text-decoration: underline solid;
  color: #333;
}
.style-c {
  text-decoration: underline dashed;
  color: #333;
}
.style-d {
  text-decoration: underline dotted;
  color: #333;
}
.style-e {
  text-decoration: underline double;
  color: #333;
}
.style-f {
  text-decoration: underline wavy;
  color: #333;
}
```

### text-decoration-color
**Type/Initial:** color | currentColor

**Description:** Decoration color — independent of text color.

**CSS:**
```css
text-decoration: underline;
text-decoration-color: red;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    gray line
  </span>
  <span class="style-c">
    white line
  </span>
  <span class="style-d">
    wavy gray
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  gap: 0.8rem;
  flex-wrap: wrap;
  font-size: 0.9rem;
}
.style-b {
  text-decoration: underline;
  text-decoration-color: #a3a3a3;
  color: #333;
}
.style-c {
  text-decoration: underline;
  text-decoration-color: #fff;
  color: #333;
}
.style-d {
  text-decoration: underline wavy;
  text-decoration-color: #525252;
  color: #333;
}
```

### text-decoration-thickness
**Type/Initial:** length | from-font | auto

**Description:** Thickness of the decoration line — precise control over underline weight.

**CSS:**
```css
text-decoration-thickness: 3px;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    1px thin
  </span>
  <span class="style-c">
    3px thick
  </span>
  <span class="style-d">
    5px heavy
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
  font-size: 0.9rem;
}
.style-b {
  text-decoration: underline;
  text-decoration-thickness: 1px;
  color: #333;
}
.style-c {
  text-decoration: underline;
  text-decoration-thickness: 3px;
  color: #333;
}
.style-d {
  text-decoration: underline;
  text-decoration-thickness: 5px;
  color: #333;
}
```

### text-underline-offset
**Type/Initial:** length | from-font | auto

**Description:** Distance from baseline to underline — adjusts underline position.

**CSS:**
```css
text-underline-offset: 4px;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    offset 1px — close
  </span>
  <span class="style-c">
    offset 4px — gap
  </span>
  <span class="style-d">
    offset 8px — far
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
  font-size: 0.9rem;
}
.style-b {
  text-decoration: underline;
  text-underline-offset: 1px;
  color: #333;
}
.style-c {
  text-decoration: underline;
  text-underline-offset: 4px;
  color: #333;
}
.style-d {
  text-decoration: underline;
  text-underline-offset: 8px;
  color: #333;
}
```

### text-transform
**Type/Initial:** keyword | none

**Description:** Case transformation — uppercase, lowercase, capitalize.

**CSS:**
```css
text-transform: none;
text-transform: capitalize;
text-transform: uppercase;
text-transform: lowercase;
text-transform: full-width;

text-transform: inherit;
text-transform: initial;
text-transform: revert;
text-transform: unset;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    uppercase text transform
  </span>
  <span class="style-c">
    LOWERCASE TEXT TRANSFORM
  </span>
  <span class="style-d">
    capitalize each word here
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.2rem;
  font-size: 0.9rem;
}
.style-b {
  text-transform: uppercase;
  color: #333;
}
.style-c {
  text-transform: lowercase;
  color: #333;
}
.style-d {
  text-transform: capitalize;
  color: #333;
}
```

### text-indent
**Type/Initial:** length | % | 0

**Description:** First-line indent — offsets the first line of a block.

**CSS:**
```css
/* Length values */
text-indent: 2em;
text-indent: 20px;

/* Percentage values */
text-indent: 10%;

/* Keyword value */
text-indent: each-line;

text-indent: inherit;
text-indent: initial;
text-indent: revert;
text-indent: unset;
```

**HTML:**
```html
<div class="db">
  <div class="style-a">
    This paragraph has a first-line indent of 2em. The indent pushes the first line to the right while subsequent lines start at the normal left edge, which is the traditional typesetting convention for printed text.
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  text-indent: 2em;
  color: #333;
  font-size: 0.85rem;
  line-height: 1.6;
}
```

### text-overflow
**Type/Initial:** keyword | clip

**Description:** Overflow behavior — clip or ellipsis for truncated text.

**CSS:**
```css
text-overflow: clip;
text-overflow: ellipsis;

text-overflow: inherit;
text-overflow: initial;
text-overflow: revert;
text-overflow: unset;
```

**HTML:**
```html
<div class="db style-a">
  <div class="style-b">
    text-overflow: ellipsis — this long string gets truncated with three dots when it overflows the container width
  </div>
  <div class="style-c">
    text-overflow: clip — this long string gets hard-clipped with no ellipsis when it overflows the container width
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.3rem;
}
.style-b {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: ellipsis;
  color: #333;
  font-size: 0.85rem;
  border: 1px solid #d4d4d4;
  padding: 0.2rem 0.4rem;
  border-radius: 3px;
}
.style-c {
  white-space: nowrap;
  overflow: hidden;
  text-overflow: clip;
  color: #333;
  font-size: 0.85rem;
  border: 1px solid #d4d4d4;
  padding: 0.2rem 0.4rem;
  border-radius: 3px;
}
```

### text-shadow
**Type/Initial:** none | shadow list | none

**Description:** Text shadow — adds drop shadow effect to text.

**CSS:**
```css
/* No shadow */
text-shadow: none;

/* With values */
text-shadow: 2px 2px #555;
text-shadow: 1px 1px 2px rgba(0,0,0,0.5);

text-shadow: inherit;
text-shadow: initial;
text-shadow: revert;
text-shadow: unset;
```

**HTML:**
```html
<div class="db style-a">
  <span class="style-b">
    subtle shadow
  </span>
  <span class="style-c">
    double glow
  </span>
  <span class="style-d">
    retro stack
  </span>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.3rem;
}
.style-b {
  text-shadow: 0 1px 2px rgba(0,0,0,0.4);
  color: #333;
  font-size: 1rem;
}
.style-c {
  text-shadow: 0 2px 6px rgba(0,0,0,0.6), 0 0 12px #a3a3a3;
  color: #333;
  font-size: 1rem;
}
.style-d {
  text-shadow: 2px 2px 0 #a3a3a3, 4px 4px 0 #d4d4d4;
  color: #000;
  font-size: 1rem;
}
```

### text-wrap
**Type/Initial:** keyword | normal

**Description:** Wrapping mode — normal, wrap (balanced), pretty, or nowrap.

**CSS:**
```css
text-wrap: wrap;
text-wrap: nowrap;
text-wrap: balance;
text-wrap: pretty;

text-wrap: inherit;
text-wrap: initial;
text-wrap: revert;
text-wrap: unset;
```

**HTML:**
```html
<div class="db style-a">
  <div class="style-b">
    Normal wrap
  </div>
  <div class="style-c">
    This heading text wraps naturally based on available width with no balance adjustment applied.
  </div>
  <div class="style-d">
    Balanced wrap
  </div>
  <div class="style-e">
    This heading text wraps in a more visually balanced way using text-wrap: balance.
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}
.style-b {
  color: #000;
  font-size: 1rem;
  font-weight: 600;
}
.style-c {
  color: #333;
  font-size: 0.85rem;
}
.style-d {
  color: #000;
  font-size: 1rem;
  font-weight: 600;
  text-wrap: balance;
}
.style-e {
  color: #333;
  font-size: 0.85rem;
}
```

### white-space
**Type/Initial:** keyword | normal

**Description:** Whitespace handling — controls line breaks and space collapsing.

**CSS:**
```css
white-space: normal;
white-space: nowrap;
white-space: pre;
white-space: pre-wrap;
white-space: pre-line;
white-space: break-spaces;

white-space: inherit;
white-space: initial;
white-space: revert;
white-space: unset;
```

**HTML:**
```html
<div class="db style-a">
  <div class="style-b">
    normal: spaces collapse, wraps at width
  </div>
  <div class="style-c">
    nowrap: no wrapping at all, overflows
  </div>
  <div class="style-d">
    pre:    preserves   all   whitespace
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: flex;
  flex-direction: column;
  gap: 0.3rem;
}
.style-b {
  white-space: normal;
  color: #333;
  font-size: 0.85rem;
}
.style-c {
  white-space: nowrap;
  color: #333;
  font-size: 0.85rem;
}
.style-d {
  white-space: pre;
  color: #333;
  font-size: 0.85rem;
}
```
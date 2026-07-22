# Typography 2024+

Modern typography CSS features.

---

## text-wrap: balance
**Type:** keyword | **Initial:** wrap

Balances line lengths for better readability.

```css
h1, h2, h3 {
  text-wrap: balance;
}
```

---

## text-wrap: pretty
**Type:** keyword | **Initial:** wrap

Optimizes line breaks for better readability.

```css
p {
  text-wrap: pretty;
}
```

---

## text-box-trim / text-box-edge
**Type:** keyword | **Initial:** none

Trims whitespace above and below text for precise sizing.

```css
/* Trim both sides */
.heading {
  text-box-trim: both;
  text-box-edge: ex alphabetic;
}

/* Trim top only */
.heading {
  text-box-trim: top;
  text-box-edge: cap alphabetic;
}
```

---

## font-size-adjust
**Type:** number | **Initial:** none

Adjusts font size to maintain x-height.

```css
body {
  font-size-adjust: 0.5;
}

/* Specific metrics */
.text {
  font-size-adjust: ex-height 0.5;
}
```

---

## font-palette
**Type:** keyword | **Initial:** normal

Selects a font palette from the font.

```css
/* Use font's default palette */
.heading {
  font-palette: normal;
}

/* Custom palette */
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
**Type:** at-rule

Defines custom font palettes.

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

## font-variant-position
**Type:** keyword | **Initial:** normal

Uses alternate glyphs for superscript/subscript.

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
**Type:** number | **Initial:** normal

Makes the first letter large and floated.

```css
p:first-of-type::first-letter {
  initial-letter: 3;
  font-weight: bold;
  color: #667eea;
}
```

---

## hyphenate-limit-chars
**Type:** number | **Initial:** auto

Controls the minimum number of characters for hyphenation.

```css
p {
  hyphens: auto;
  hyphenate-limit-chars: 6 3 2;
}
```

```html
<p>This is a paragraph with some long words that might need hyphenation for better readability and layout.</p>
```

```css
h1 {
  text-wrap: balance;
  text-box-trim: both;
  text-box-edge: cap alphabetic;
}

p {
  text-wrap: pretty;
  hyphens: auto;
  hyphenate-limit-chars: 6 3 2;
}

.first-para::first-letter {
  initial-letter: 3;
  font-weight: bold;
  color: #667eea;
}
```

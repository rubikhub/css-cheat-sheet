# Typography — OpenType & Variable Font Features

Advanced typography properties for OpenType features, variable fonts, and font face declarations.

---

## OpenType Features

### font-feature-settings
**Type:** string | **Initial:** normal

Enables or disables specific OpenType font features by tag.

```css
/* Enable specific features */
font-feature-settings: "liga" 1;
font-feature-settings: "kern" 1;
font-feature-settings: "smcp" 1;
font-feature-settings: "onum" 1;

/* Disable features */
font-feature-settings: "liga" 0;

/* Multiple features */
font-feature-settings: "liga" 1, "kern" 1, "smcp" 1;

/* Global values */
font-feature-settings: inherit;
font-feature-settings: initial;
```

---

### font-optical-sizing
**Type:** keyword | **Initial:** auto

Controls whether the browser adjusts optical size for the font.

```css
font-optical-sizing: auto;
font-optical-sizing: none;
```

---

## Variable Fonts

### font-variation-settings
**Type:** string | **Initial:** normal

Fine-tunes variable font axes (weight, width, optical size, custom axes).

```css
/* Weight axis */
font-variation-settings: 'wght' 750;

/* Optical size axis */
font-variation-settings: 'opsz' 36;

/* Multiple axes */
font-variation-settings: 'wght' 750, 'opsz' 36, 'wdth' 110;

/* Custom axis */
font-variation-settings: 'XTRA' 500;
```

```html
<span class="thin">Thin weight</span>
<span class="bold">Bold weight</span>
<span class="wide">Wide variant</span>
```

```css
.thin { font-variation-settings: 'wght' 100; }
.bold { font-variation-settings: 'wght' 900; }
.wide { font-variation-settings: 'wdth' 150; }
```

---

## Font Face

### @font-face
**Type:** at-rule

Declares a custom font family and its source file.

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

### @font-feature-values
**Type:** at-rule

Defines named values for OpenType feature settings, reusable across rules.

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

[Example](../examples/advanced/01-typography-ot-features/index.html)

← **Previous Topic:** [Nesting](../intermediate/21-nesting.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Background Blend Mode](../advanced/02-background-blend-mode.md) →

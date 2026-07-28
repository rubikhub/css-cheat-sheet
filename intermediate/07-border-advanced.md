# Border Advanced
---
## Border
### border
**Type/Initial:** shorthand | —

**Description:** Shorthand — sets width, style, and color on all sides.

**CSS:**
```css
/* Single values */
border: 1px;
border: solid;
border: red;

/* Multi values */
border: 1px solid;
border: 1px solid red;
border: 1px red;

border: inherit;
border: initial;
border: revert;
border: unset;
```

**HTML:**
```html
<div class="db style-a">
  3px solid purple border on all sides.
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
  border: 3px solid #6c5ce7;
}
```

### border-width
**Type/Initial:** shorthand | medium

**Description:** Thickness — thin, medium, thick, or custom length.

**CSS:**
```css
/* Keyword values */
border-width: thin;
border-width: medium;
border-width: thick;

/* Length values */
border-width: 1px;
border-width: 0.5em;
border-width: 0;

border-width: inherit;
border-width: initial;
border-width: revert;
border-width: unset;
```

**HTML:**
```html
<div class="db style-a">
  Thick border using border-width: 5px.
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
  border: 5px solid #fff;
}
```

### border-style
**Type/Initial:** keyword | none

**Description:** Line style — solid, dashed, dotted, double, groove, ridge, inset, outset.

**CSS:**
```css
border-style: none;
border-style: hidden;
border-style: dotted;
border-style: dashed;
border-style: solid;
border-style: double;
border-style: groove;
border-style: ridge;
border-style: inset;
border-style: outset;

border-style: inherit;
border-style: initial;
border-style: revert;
border-style: unset;
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
  gap: 0.5rem;
  flex-wrap: wrap;
  padding: 0.4rem;
}
.style-b {
  border: 2px solid #6c5ce7;
  padding: 0.3rem 0.5rem;
  border-radius: 3px;
}
.style-c {
  border: 2px dashed #00b894;
  padding: 0.3rem 0.5rem;
  border-radius: 3px;
}
.style-d {
  border: 2px dotted #fdcb6e;
  padding: 0.3rem 0.5rem;
  border-radius: 3px;
}
.style-e {
  border: 3px double #e17055;
  padding: 0.3rem 0.5rem;
  border-radius: 3px;
}
```

### border-color
**Type/Initial:** color | currentColor

**Description:** Line color — sets the color of the border.

**CSS:**
```css
/* Named colors */
border-color: currentColor;
border-color: red;
border-color: transparent;

/* Hex */
border-color: #ff5733;

/* RGB/RGBA */
border-color: rgb(255, 0, 0);
border-color: rgba(255, 0, 0, 0.5);

/* HSL/HSLA */
border-color: hsl(0, 100%, 50%);

border-color: inherit;
border-color: initial;
border-color: revert;
border-color: unset;
```

**HTML:**
```html
<div class="db style-a">
  Cyan-colored border line.
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
  border: 3px solid #00cec9;
}
```

### border-top / right / bottom / left
**Type/Initial:** shorthand | —

**Description:** Individual sides — style each border edge independently.

**CSS:**
```css
/* Single values */
border-top: 1px;
border-right: solid;
border-bottom: red;

/* Multi values */
border-top: 1px solid red;
border-right: 2px dashed blue;

border-top: inherit;
border-top: initial;
border-top: revert;
border-top: unset;
```

**HTML:**
```html
<div class="db style-a">
  Red top border, blue bottom border, no sides.
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
  border-top: 3px solid #d63031;
  border-bottom: 3px solid #0984e3;
}
```

### border-collapse
**Type/Initial:** keyword | separate

**Description:** Table model — collapse adjacent borders or keep separate.

**CSS:**
```css
border-collapse: separate;
border-collapse: collapse;

border-collapse: inherit;
border-collapse: initial;
border-collapse: revert;
border-collapse: unset;
```

**HTML:**
```html
<div class="db style-a">
  <table class="style-b">
    <tr>
      <td class="style-c">
        A1
      </td>
      <td class="style-d">
        B1
      </td>
    </tr>
    <tr>
      <td class="style-e">
        A2
      </td>
      <td class="style-f">
        B2
      </td>
    </tr>
  </table>
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
  padding: 0;
}
.style-b {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.85rem;
}
.style-c {
  border: 1px solid #fff;
  padding: 0.3rem;
}
.style-d {
  border: 1px solid #fff;
  padding: 0.3rem;
}
.style-e {
  border: 1px solid #fff;
  padding: 0.3rem;
}
.style-f {
  border: 1px solid #fff;
  padding: 0.3rem;
}
```

### border-spacing
**Type/Initial:** length | 0

**Description:** Cell gap — space between table cell borders in separate model.

**CSS:**
```css
border-spacing: 6px;
```

**HTML:**
```html
<div class="db style-a">
  <table class="style-b">
    <tr>
      <td class="style-c">
        A1
      </td>
      <td class="style-d">
        B1
      </td>
    </tr>
    <tr>
      <td class="style-e">
        A2
      </td>
      <td class="style-f">
        B2
      </td>
    </tr>
  </table>
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
  padding: 0;
}
.style-b {
  width: 100%;
  border: 1px solid #fff;
  border-collapse: separate;
  border-spacing: 6px;
  font-size: 0.85rem;
}
.style-c {
  background: #fff;
  padding: 0.3rem;
  border-radius: 3px;
}
.style-d {
  background: #fff;
  padding: 0.3rem;
  border-radius: 3px;
}
.style-e {
  background: #fff;
  padding: 0.3rem;
  border-radius: 3px;
}
.style-f {
  background: #fff;
  padding: 0.3rem;
  border-radius: 3px;
}
```

### border-image
**Type/Initial:** shorthand | —

**Description:** Image border — uses an image slice as the border decoration.

**CSS:**
```css
border-image: url('border.png') 30;
border-image: url('border.png') 30 / 10px;
border-image: url('border.png') 30 / 10px / 5px stretch;

border-image: inherit;
border-image: initial;
border-image: revert;
border-image: unset;
```

**HTML:**
```html
<div class="db style-a">
  Gradient border using border-image.
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
  border: 4px solid;
  border-image: linear-gradient(135deg, #6c5ce7, #fd79a8) 1;
}
```

## Outline
### outline
**Type/Initial:** shorthand | —

**Description:** Outline — a line drawn outside the border edge (doesn't affect layout).

**CSS:**
```css
/* Single values */
outline: 1px;
outline: solid;
outline: red;

/* Multi values */
outline: 1px solid;
outline: 1px solid red;
outline: 2px dashed blue 3px;

outline: inherit;
outline: initial;
outline: revert;
outline: unset;
```

**HTML:**
```html
<div class="db style-a">
  Outline drawn outside the border, no layout shift.
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
  border: 2px solid #fff;
  outline: 3px solid #00cec9;
}
```

### outline-width
**Type/Initial:** length | medium

**Description:** Outline thickness — controls how thick the outline is.

**CSS:**
```css
outline-width: thin;
outline-width: medium;
outline-width: thick;
outline-width: 2px;
outline-width: 0;

outline-width: inherit;
outline-width: initial;
outline-width: revert;
outline-width: unset;
```

**HTML:**
```html
<div class="db style-a">
  4px pink outline around the element.
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
  border: 2px solid #fff;
  outline: 4px solid #fd79a8;
}
```

### outline-style
**Type/Initial:** keyword | none

**Description:** Outline style — same values as border-style.

**CSS:**
```css
outline-style: none;
outline-style: dotted;
outline-style: dashed;
outline-style: solid;
outline-style: double;
outline-style: groove;
outline-style: ridge;
outline-style: inset;
outline-style: outset;
outline-style: auto;

outline-style: inherit;
outline-style: initial;
outline-style: revert;
outline-style: unset;
```

**HTML:**
```html
<div class="db style-a">
  Dashed yellow outline style.
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
  border: 2px solid #fff;
  outline: 3px dashed #fdcb6e;
}
```

### outline-color
**Type/Initial:** color | currentColor

**Description:** Outline color — sets the outline's color independently.

**CSS:**
```css
/* Keyword value */
outline-color: invert;

/* Colors */
outline-color: red;
outline-color: #ff5733;
outline-color: rgb(255, 0, 0);

outline-color: inherit;
outline-color: initial;
outline-color: revert;
outline-color: unset;
```

**HTML:**
```html
<div class="db style-a">
  Double orange outline color.
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
  border: 2px solid #fff;
  outline: 3px double #e17055;
}
```

### outline-offset
**Type/Initial:** length | 0

**Description:** Outline gap — distance between border edge and outline.

**CSS:**
```css
/* Length values */
outline-offset: 3px;
outline-offset: -2px;
outline-offset: 0;

/* Global values */
outline-offset: inherit;
outline-offset: initial;
outline-offset: revert;
outline-offset: unset;
```

**HTML:**
```html
<div class="db style-a">
  Outline pushed 6px away from border edge.
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
  border: 2px solid #fff;
  outline: 2px solid #6c5ce7;
  outline-offset: 6px;
}
```

## Border Radius
### border-radius
**Type/Initial:** shorthand | 0

**Description:** Rounded corners — curves the border-box corners.

**CSS:**
```css
/* Length values */
border-radius: 10px;
border-radius: 50%;
border-radius: 0;

/* Two-value syntax */
border-radius: 10px 20px;
border-radius: 10px 20px 30px;
border-radius: 10px 20px 30px 40px;

/* Global values */
border-radius: inherit;
border-radius: initial;
border-radius: revert;
border-radius: unset;
```

**HTML:**
```html
<div class="db style-a">
  All four corners rounded to 12px.
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
  border: 2px solid #fff;
  border-radius: 12px;
}
```

### border-top-left-radius / top-right-radius
**Type/Initial:** length | % | 0

**Description:** Individual corner — radius for a specific corner.

**CSS:**
```css
border-top-left-radius: 10px;
border-top-left-radius: 50%;
border-top-left-radius: 10px 20px;

border-top-left-radius: inherit;
border-top-left-radius: initial;
border-top-left-radius: revert;
border-top-left-radius: unset;
```

**HTML:**
```html
<div class="db style-a">
  Only top-left and bottom-right corners rounded.
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
  border: 2px solid #fff;
  border-top-left-radius: 20px;
  border-bottom-right-radius: 20px;
}
```

### border-bottom-left-radius / bottom-right-radius
**Type/Initial:** length | % | 0

**Description:** Individual corner — radius for a specific corner.

**CSS:**
```css
border-bottom-left-radius: 10px;
border-bottom-left-radius: 50%;
border-bottom-left-radius: 10px 20px;

border-bottom-left-radius: inherit;
border-bottom-left-radius: initial;
border-bottom-left-radius: revert;
border-bottom-left-radius: unset;
```

**HTML:**
```html
<div class="db style-a">
  Bottom corners at 50% create a pill/squircle shape.
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
  border: 2px solid #fff;
  border-bottom-left-radius: 50%;
  border-bottom-right-radius: 50%;
}
```

### border-start-radius / border-end-radius
**Type/Initial:** length | % | 0

**Description:** Logical corner radius — maps to physical corners based on writing direction.

**CSS:**
```css
border-start-start-radius: 16px;
border-start-end-radius: 0;
border-end-start-radius: 0;
border-end-end-radius: 16px;
```

**HTML:**
```html
<div class="db style-a">
  Logical start/start + end/end match top-left + bottom-right in LTR.
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
  border: 2px solid #fff;
  border-start-start-radius: 16px;
  border-end-end-radius: 16px;
}
```

## Shadow
### box-shadow
**Type/Initial:** none | shadow list | none

**Description:** Drop shadow — adds one or more shadows behind the element.

**CSS:**
```css
box-shadow: 0 4px 6px rgba(108,92,231,.4), 0 12px 24px rgba(108,92,231,.2);
```

**HTML:**
```html
<div class="db style-a">
  Layered purple drop shadows create depth.
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
  box-shadow: 0 4px 6px rgba(108,92,231,.4), 0 12px 24px rgba(108,92,231,.2);
}
```

### box-shadow: inset
**Type/Initial:** inset | offset | blur | spread | color | none

**Description:** Inset shadows — appear inside the element's border.

**CSS:**
```css
box-shadow: inset 0 2px 8px rgba(0,0,0,.6), 0 4px 12px rgba(0,0,0,.3);
```

**HTML:**
```html
<div class="db style-a">
  Inner shadow creates pressed-in look, outer shadow adds lift.
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
  box-shadow: inset 0 2px 8px rgba(0,0,0,.6), 0 4px 12px rgba(0,0,0,.3);
}
```

---

[Example](../examples/intermediate/07-border-advanced/index.html)

← **Previous Topic:** [State Pseudo Classes](../intermediate/06-state-pseudo-classes.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Transform](../intermediate/08-transform.md) →

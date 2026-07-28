# Background Advanced
---
## Color & Image
### background-color
**Type/Initial:** color | transparent

**Description:** Solid color — fills the element with a background color.

**CSS:**
```css
/* Named colors */
background-color: transparent;
background-color: red;
background-color: currentColor;

/* Hex */
background-color: #ff5733;
background-color: #f00;

/* RGB/RGBA */
background-color: rgb(255, 0, 0);
background-color: rgba(255, 0, 0, 0.5);

/* HSL/HSLA */
background-color: hsl(0, 100%, 50%);
background-color: hsla(0, 100%, 50%, 0.5);

/* Global values */
background-color: inherit;
background-color: initial;
background-color: revert;
background-color: unset;
```

**HTML:**
```html
<div class="db style-a">
  Solid background color fills this box.
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
  background: #6c5ce7;
  color: #fff;
}
```

### background-image
**Type/Initial:** url() | none

**Description:** Background image — tiled by default to fill the element.

**CSS:**
```css
/* No image */
background-image: none;

/* URL */
background-image: url('image.jpg');

/* Gradients */
background-image: linear-gradient(to right, red, blue);
background-image: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
background-image: radial-gradient(circle, red, blue);
background-image: conic-gradient(red, orange, yellow, green, blue);

/* Global values */
background-image: inherit;
background-image: initial;
background-image: revert;
background-image: unset;
```

**HTML:**
```html
<div class="db style-a">
  Diagonal stripe pattern from background-image.
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
  background-image: repeating-linear-gradient(45deg, transparent, transparent 8px, rgba(255,255,255,.08) 8px, rgba(255,255,255,.08) 16px);
}
```

### background
**Type/Initial:** shorthand | —

**Description:** Shorthand — combines color, image, position, repeat, size, and attachment.

**CSS:**
```css
/* Single values */
background: red;
background: url('image.jpg');
background: center;
background: no-repeat;
background: fixed;

/* Multi values */
background: url('image.jpg') center no-repeat;
background: red url('image.jpg') center/cover no-repeat;

/* Global values */
background: inherit;
background: initial;
background: revert;
background: unset;
```

**HTML:**
```html
<div class="db style-a">
  Shorthand sets color + image + position + size + repeat.
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
  background: linear-gradient(135deg, #e17055, #d63031);
  background-size: cover;
  background-position: center;
}
```

## Gradient
### linear-gradient()
**Type/Initial:** function | —

**Description:** Linear gradient — transitions colors along a straight line.

**CSS:**
```css
background: linear-gradient(135deg, #6c5ce7, #a29bfe, #fd79a8);
```

**HTML:**
```html
<div class="db style-a">
  135deg gradient from purple to pink.
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
  background: linear-gradient(135deg, #6c5ce7, #a29bfe, #fd79a8);
  color: #fff;
}
```

### radial-gradient()
**Type/Initial:** function | —

**Description:** Radial gradient — radiates colors outward from a center point.

**CSS:**
```css
background: radial-gradient(circle, #00b894, #00cec9, #0984e3);
```

**HTML:**
```html
<div class="db style-a">
  Radial burst from green to blue center.
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
  background: radial-gradient(circle, #00b894, #00cec9, #0984e3);
  color: #fff;
}
```

### conic-gradient()
**Type/Initial:** function | —

**Description:** Conic gradient — sweeps colors around a center point like a color wheel.

**CSS:**
```css
background: conic-gradient(#ff6b6b, #feca57, #48dbfb, #ff9ff3, #ff6b6b);
```

**HTML:**
```html
<div class="db style-a">
  Conic color wheel sweep.
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
  background: conic-gradient(#ff6b6b, #feca57, #48dbfb, #ff9ff3, #ff6b6b);
  border-radius: 50%;
  aspect-ratio: 1;
  max-width: 200px;
  color: #fff;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}
```

### repeating-linear-gradient()
**Type/Initial:** function | —

**Description:** Repeating linear — tiles a gradient pattern.

**CSS:**
```css
background: repeating-linear-gradient(90deg, #d63031 0px, #d63031 20px, #fdcb6e 20px, #fdcb6e 40px);
```

**HTML:**
```html
<div class="db style-a">
  Red and yellow vertical stripes repeating at 20px.
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
  background: repeating-linear-gradient(90deg, #d63031 0px, #d63031 20px, #fdcb6e 20px, #fdcb6e 40px);
  color: #fff;
}
```

### repeating-radial-gradient()
**Type/Initial:** function | —

**Description:** Repeating radial — tiles a radial gradient pattern.

**CSS:**
```css
background: repeating-radial-gradient(circle, #2d3436 0px, #2d3436 10px, #636e72 10px, #636e72 20px);
```

**HTML:**
```html
<div class="db style-a">
  Concentric dark rings repeating outward.
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
  background: repeating-radial-gradient(circle, #2d3436 0px, #2d3436 10px, #636e72 10px, #636e72 20px);
  color: #fff;
}
```

## Repeat & Size
### background-repeat
**Type/Initial:** keyword | repeat

**Description:** Tiling behavior — repeat, no-repeat, repeat-x, repeat-y, round, space.

**CSS:**
```css
background-repeat: repeat;
background-repeat: repeat-x;
background-repeat: repeat-y;
background-repeat: no-repeat;
background-repeat: space;
background-repeat: round;

/* Two-value syntax */
background-repeat: repeat space;
background-repeat: repeat round;
background-repeat: no-repeat space;

/* Global values */
background-repeat: inherit;
background-repeat: initial;
background-repeat: revert;
background-repeat: unset;
```

**HTML:**
```html
<div class="db style-a">
  Vertical bars distributed with even spacing via round.
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
  background: repeating-linear-gradient(0deg, #6c5ce7 0px, #6c5ce7 6px, transparent 6px, transparent 18px);
  background-repeat: space;
  background-size: 6px 18px;
}
```

### background-size
**Type/Initial:** length | % | cover | contain | auto

**Description:** Image dimensions — auto, cover (fill), or contain (fit).

**CSS:**
```css
/* Keywords */
background-size: auto;
background-size: cover;
background-size: contain;

/* Length values */
background-size: 200px;
background-size: 200px 100px;

/* Percentage values */
background-size: 50%;
background-size: 50% 75%;

/* Global values */
background-size: inherit;
background-size: initial;
background-size: revert;
background-size: unset;
```

**HTML:**
```html
<div class="db style-a">
  <div class="style-b">
    cover fills area
  </div>
  <div class="style-c">
    contain fits inside
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
  gap: 0.6rem;
  flex-wrap: wrap;
  padding: 0;
}
.style-b {
  flex: 1;
  min-width: 120px;
  background: linear-gradient(135deg, #00b894, #0984e3);
  background-size: cover;
  background-position: center;
  padding: 1.2rem 0.6rem;
  border-radius: 4px;
  color: #fff;
}
.style-c {
  flex: 1;
  min-width: 120px;
  background: linear-gradient(135deg, #fdcb6e, #e17055);
  background-size: contain;
  background-repeat: no-repeat;
  padding: 1.2rem 0.6rem;
  border-radius: 4px;
  color: #fff;
}
```

### background-position
**Type/Initial:** position | 0% 0%

**Description:** Image placement — keyword pairs or x/y coordinates.

**CSS:**
```css
/* Keywords */
background-position: top;
background-position: bottom;
background-position: left;
background-position: right;
background-position: center;

/* One value */
background-position: 20px;
background-position: 50%;

/* Two values */
background-position: 20px 40px;
background-position: top right;
background-position: center bottom;

/* Three/four values */
background-position: right 10px bottom 20px;

/* Global values */
background-position: inherit;
background-position: initial;
background-position: revert;
background-position: unset;
```

**HTML:**
```html
<div class="db style-a">
  Gradient bar pinned to bottom-right corner.
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
  background: linear-gradient(to right, #6c5ce7 4px, transparent 4px);
  background-position: right 20px bottom 10px;
  background-repeat: no-repeat;
  background-size: 4px 60%;
}
```

### background-attachment
**Type/Initial:** keyword | scroll

**Description:** Scroll behavior — fixed (viewport), local (scroll container), or scroll.

**CSS:**
```css
background-attachment: scroll;
background-attachment: fixed;
background-attachment: local;
background-attachment: local scroll;

/* Global values */
background-attachment: inherit;
background-attachment: initial;
background-attachment: revert;
background-attachment: unset;
```

**HTML:**
```html
<div class="db style-a">
  Fixed gradient stays in place when scrolling.
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
  background: linear-gradient(180deg, #0984e3 0%, #6c5ce7 50%, #d63031 100%);
  background-attachment: fixed;
  color: #fff;
}
```

## Clip & Origin
### background-clip
**Type/Initial:** keyword | border-box

**Description:** Paint boundary — how far the background extends (border-box, padding-box, content-box, text).

**CSS:**
```css
background-clip: border-box;
background-clip: padding-box;
background-clip: content-box;
background-clip: text;
background-clip: no-clip;

/* Global values */
background-clip: inherit;
background-clip: initial;
background-clip: revert;
background-clip: unset;
```

**HTML:**
```html
<div class="db style-a">
  Gradient clipped to text shape.
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
  background: linear-gradient(135deg, #fd79a8, #fdcb6e, #00cec9);
  -webkit-background-clip: text;
  background-clip: text;
  color: transparent;
  font-weight: 700;
  font-size: 1.3rem;
}
```

### background-origin
**Type/Initial:** keyword | padding-box

**Description:** Position origin — coordinate system for background-position.

**CSS:**
```css
background-origin: padding-box;
background-origin: border-box;
background-origin: content-box;

/* Global values */
background-origin: inherit;
background-origin: initial;
background-origin: revert;
background-origin: unset;
```

**HTML:**
```html
<div class="db style-a">
  Background starts from content-box, showing padding as transparent gap.
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
  background-image: linear-gradient(135deg, #d63031, #fdcb6e);
  background-origin: content-box;
  background-clip: content-box;
  padding: 10px;
}
```

---

[Example](../examples/intermediate/10-background-advanced/index.html)

← **Previous Topic:** [Transform Functions](../intermediate/09-transform-functions.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Flexbox Advanced](../intermediate/11-flexbox-advanced.md) →

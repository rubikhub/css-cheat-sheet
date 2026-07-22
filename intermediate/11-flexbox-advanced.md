# Flexbox Advanced
---
## Container Properties
### display
**Type/Initial:** keyword | inline

**Description:** Flex container — enables flex layout on children.

**CSS:**
```css
display: flex;
display: inline-flex;
display: block-flex;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  gap: 0.4rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### flex-direction
**Type/Initial:** keyword | row

**Description:** Direction — sets main axis direction of flex items.

**CSS:**
```css
flex-direction: row;
flex-direction: row-reverse;
flex-direction: column;
flex-direction: column-reverse;

flex-direction: inherit;
flex-direction: initial;
flex-direction: revert;
flex-direction: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### flex-wrap
**Type/Initial:** keyword | nowrap

**Description:** Wrap — allows flex items to wrap onto multiple lines.

**CSS:**
```css
flex-wrap: nowrap;
flex-wrap: wrap;
flex-wrap: wrap-reverse;

flex-wrap: inherit;
flex-wrap: initial;
flex-wrap: revert;
flex-wrap: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  flex-wrap: wrap;
  width: 160px;
  gap: 0.3rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### justify-content
**Type/Initial:** keyword | flex-start

**Description:** Main-axis alignment — distributes space along the main axis.

**CSS:**
```css
justify-content: flex-start;
justify-content: flex-end;
justify-content: center;
justify-content: space-between;
justify-content: space-around;
justify-content: space-evenly;
justify-content: start;
justify-content: end;
justify-content: left;
justify-content: right;
justify-content: stretch;

justify-content: inherit;
justify-content: initial;
justify-content: revert;
justify-content: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  justify-content: space-between;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### align-items
**Type/Initial:** keyword | stretch

**Description:** Cross-axis alignment — aligns items along the cross axis.

**CSS:**
```css
align-items: flex-start;
align-items: flex-end;
align-items: center;
align-items: baseline;
align-items: stretch;
align-items: start;
align-items: end;
align-items: self-start;
align-items: self-end;

align-items: inherit;
align-items: initial;
align-items: revert;
align-items: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  align-items: center;
  height: 64px;
  gap: 0.4rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 1.2rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.6rem;
  border-radius: 4px;
  color: #333;
}
```

### align-content
**Type/Initial:** keyword | stretch

**Description:** Multi-line alignment — aligns packed lines in a multi-line flex container.

**CSS:**
```css
align-content: flex-start;
align-content: flex-end;
align-content: center;
align-content: space-between;
align-content: space-around;
align-content: space-evenly;
align-content: stretch;
align-content: start;
align-content: end;

align-content: inherit;
align-content: initial;
align-content: revert;
align-content: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
  </div>
  <div class="db style-e">
    D
  </div>
  <div class="db style-f">
    E
  </div>
  <div class="db style-g">
    F
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
  flex-wrap: wrap;
  align-content: center;
  height: 100px;
  gap: 0.3rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-f {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-g {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### gap
**Type/Initial:** length | 0

**Description:** Gutters — sets spacing between flex items.

**CSS:**
```css
gap: 10px;
gap: 1rem;
gap: 5%;

gap: 10px 20px;
gap: 1rem 2rem;

gap: inherit;
gap: initial;
gap: revert;
gap: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  gap: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

## Item Properties
### order
**Type/Initial:** integer | 0

**Description:** Order — reorders flex items within the container.

**CSS:**
```css
order: 0;
order: 1;
order: -1;
order: 10;

order: inherit;
order: initial;
order: revert;
order: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  gap: 0.4rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  order: 2;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  order: 3;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  order: 1;
}
```

### flex-grow
**Type/Initial:** number | 0

**Description:** Grow — defines how much an item grows relative to others.

**CSS:**
```css
flex-grow: 0;
flex-grow: 1;
flex-grow: 2;

flex-grow: inherit;
flex-grow: initial;
flex-grow: revert;
flex-grow: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  gap: 0.4rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  flex-grow: 0;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  flex-grow: 2;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  flex-grow: 0;
}
```

### flex-shrink
**Type/Initial:** number | 1

**Description:** Shrink — defines how much an item shrinks when space is limited.

**CSS:**
```css
flex-shrink: 0;
flex-shrink: 1;
flex-shrink: 2;

flex-shrink: inherit;
flex-shrink: initial;
flex-shrink: revert;
flex-shrink: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  width: 120px;
  gap: 0.4rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  flex-shrink: 0;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  flex-shrink: 2;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  flex-shrink: 1;
}
```

### flex-basis
**Type/Initial:** length | auto

**Description:** Basis — sets the initial main-axis size of an item before growing/shrinking.

**CSS:**
```css
/* Length values */
flex-basis: 100px;
flex-basis: 0;
flex-basis: 10em;

/* Percentage values */
flex-basis: 50%;

/* Keyword values */
flex-basis: auto;
flex-basis: content;

/* Global values */
flex-basis: inherit;
flex-basis: initial;
flex-basis: revert;
flex-basis: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  gap: 0.4rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  flex-basis: 40px;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  flex-basis: 80px;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  flex-basis: 40px;
}
```

### flex
**Type/Initial:** shorthand | 0 1 auto

**Description:** Shorthand — combines grow, shrink, and basis in one declaration.

**CSS:**
```css
/* Single values */
flex: auto;
flex: initial;
flex: none;
flex: 1;
flex: 0 1 auto;
flex: 1 0 0%;

/* Global values */
flex: inherit;
flex: initial;
flex: revert;
flex: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  gap: 0.4rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  flex: 0 1 40px;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  flex: 2 1 60px;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  flex: 0 1 40px;
}
```

### align-self
**Type/Initial:** keyword | auto

**Description:** Self-align — overrides align-items for a single flex item.

**CSS:**
```css
align-self: auto;
align-self: flex-start;
align-self: flex-end;
align-self: center;
align-self: baseline;
align-self: stretch;
align-self: start;
align-self: end;
align-self: self-start;
align-self: self-end;

align-self: inherit;
align-self: initial;
align-self: revert;
align-self: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  height: 64px;
  gap: 0.4rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  align-self: flex-start;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  align-self: center;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  align-self: flex-end;
}
```

### place-items
**Type/Initial:** shorthand | stretch

**Description:** Place items — shorthand for align-items and justify-items together.

**CSS:**
```css
display: flex;
place-items: center;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
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
  height: 64px;
  gap: 0.4rem;
  place-items: center;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 1.2rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.5rem;
  border-radius: 4px;
  color: #333;
}
```
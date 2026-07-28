# Counters & Markers
---
## Container Properties
### counter-reset
**Type/Initial:** identifier | none

**Description:** Reset — creates or resets a CSS counter to a given value.

**CSS:**
```css
counter-reset: none;
counter-reset: myCounter;
counter-reset: myCounter 0;
counter-reset: myCounter 10;
counter-reset: myCounter -1;
counter-reset: myCounter 0 anotherCounter 0;

counter-reset: inherit;
counter-reset: initial;
counter-reset: revert;
counter-reset: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    item 1
  </div>
  <div class="db style-c">
    item 2
  </div>
  <div class="db style-d">
    item 3
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
  counter-reset: myCounter;
  padding: 1rem;
  display: flex;
  gap: 0.5rem;
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

### counter-increment
**Type/Initial:** identifier | none

**Description:** Increment — increments a CSS counter by a given value.

**CSS:**
```css
counter-increment: none;
counter-increment: myCounter;
counter-increment: myCounter 1;
counter-increment: myCounter 2;
counter-increment: myCounter -1;
counter-increment: myCounter 0.5;
counter-increment: myCounter anotherCounter;

counter-increment: inherit;
counter-increment: initial;
counter-increment: revert;
counter-increment: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    item
  </div>
  <div class="db style-c">
    item
  </div>
  <div class="db style-d">
    item
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
  counter-reset: myCounter;
  padding: 1rem;
  display: flex;
  gap: 0.5rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  counter-increment: myCounter;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  counter-increment: myCounter;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  counter-increment: myCounter;
}
```

### counter()
**Type/Initial:** function | (none)

**Description:** Function — displays the current value of a named counter.

**CSS:**
```css
/* Basic */
content: counter(myCounter);

/* With counter style */
content: counter(myCounter, decimal);
content: counter(myCounter, decimal-leading-zero);
content: counter(myCounter, lower-roman);
content: counter(myCounter, upper-roman);
content: counter(myCounter, lower-alpha);
content: counter(myCounter, upper-alpha);

/* Nested counters */
content: counter(parent) "." counter(child);
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    decimal
  </div>
  <div class="db style-c">
    upper-roman
  </div>
  <div class="db style-d">
    lower-alpha
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
  counter-reset: myCounter;
  padding: 1rem;
  display: flex;
  gap: 0.8rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  counter-increment: myCounter;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  counter-increment: myCounter;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  counter-increment: myCounter;
}
```

### counters()
**Type/Initial:** function | (none)

**Description:** Function — displays the current value of all nested counters with the same name.

**CSS:**
```css
/* Basic with separator */
counters(myCounter, ".");
counters(myCounter, " > ");
counters(myCounter, " - ");
counters(myCounter, "", decimal);

/* Nested structure */
counters(section, ".");
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    item
  </div>
  <div class="db style-c">
    item
  </div>
  <div class="db style-d">
    item
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
  counter-reset: section;
  padding: 1rem;
  display: flex;
  gap: 0.8rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  counter-increment: section;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  counter-increment: section;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  counter-increment: section;
}
```

### list-style-type
**Type/Initial:** keyword | disc

**Description:** Type — specifies the marker style for list items.

**CSS:**
```css
/* Disc types */
list-style-type: disc;
list-style-type: circle;
list-style-type: square;
list-style-type: none;

/* Numbering */
list-style-type: decimal;
list-style-type: decimal-leading-zero;
list-style-type: lower-roman;
list-style-type: upper-roman;
list-style-type: lower-alpha;
list-style-type: upper-alpha;
list-style-type: lower-greek;
list-style-type: lower-latin;
list-style-type: upper-latin;

/* Symbols */
list-style-type: disclosure-open;
list-style-type: disclosure-closed;
list-style-type: hebrew;
list-style-type: cjk-ideographic;
list-style-type: hiragana;
list-style-type: katakana;

/* Custom symbol */
list-style-type: "→";

list-style-type: inherit;
list-style-type: initial;
list-style-type: revert;
list-style-type: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    disc
  </div>
  <div class="db style-c">
    circle
  </div>
  <div class="db style-d">
    square
  </div>
  <div class="db style-e">
    decimal
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
  gap: 0.8rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  list-style-type: disc;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  list-style-type: circle;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  list-style-type: square;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  list-style-type: decimal;
}
```

### list-style-image
**Type/Initial:** url | none

**Description:** Image — specifies an image as the list marker.

**CSS:**
```css
list-style-image: none;
list-style-image: url("check.svg");
list-style-image: url("arrow.png");
list-style-image: url("bullet.gif");

list-style-image: inherit;
list-style-image: initial;
list-style-image: revert;
list-style-image: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    custom image
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
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  list-style-image: url("check.svg");
}
```

### list-style-position
**Type/Initial:** keyword | outside

**Description:** Position — determines whether the marker is inside or outside the content box.

**CSS:**
```css
list-style-position: outside;
list-style-position: inside;

list-style-position: inherit;
list-style-position: initial;
list-style-position: revert;
list-style-position: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    outside
  </div>
  <div class="db style-c">
    inside
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
  gap: 1.5rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  list-style-position: outside;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  list-style-position: inside;
}
```

### list-style
**Type/Initial:** shorthand | disc outside none

**Description:** Shorthand — combines list-style-type, list-style-position, and list-style-image.

**CSS:**
```css
list-style: none;
list-style: disc outside;
list-style: square inside;
list-style: url("check.svg") outside;
list-style: decimal leading-zero inside;
list-style: lower-roman url("marker.png") outside;

list-style: inherit;
list-style: initial;
list-style: revert;
list-style: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    none
  </div>
  <div class="db style-c">
    disc outside
  </div>
  <div class="db style-d">
    square inside
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
  gap: 0.8rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  list-style: none;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  list-style: disc outside;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  list-style: square inside;
}
```

---

[Example](../examples/intermediate/13-counters-and-markers/index.html)

← **Previous Topic:** [Grid Advanced](../intermediate/12-grid-advanced.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Filter & Clip Path](../intermediate/14-filter-and-clip-path.md) →

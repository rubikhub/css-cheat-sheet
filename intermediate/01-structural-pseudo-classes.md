# Structural Pseudo Classes
---
## Container Properties
### :first-child
**Type/Initial:** pseudo-class | (none)

**Description:** Selects the first child element of its parent.

**CSS:**
```css
li:first-child {
  font-weight: bold;
  color: blue;
}

.item:first-child {
  border-top: 2px solid green;
}

.card:first-child {
  background: lightyellow;
}

p:first-child {
  font-size: 1.2em;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    first child (selected)
  </div>
  <div class="db style-c">
    second child
  </div>
  <div class="db style-d">
    third child
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
  border-top: 2px solid green;
  font-weight: bold;
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

### :last-child
**Type/Initial:** pseudo-class | (none)

**Description:** Selects the last child element of its parent.

**CSS:**
```css
li:last-child {
  font-weight: bold;
  color: red;
}

.item:last-child {
  border-bottom: 2px solid green;
}

.card:last-child {
  background: lightyellow;
}

p:last-child {
  margin-bottom: 0;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    first child
  </div>
  <div class="db style-c">
    second child
  </div>
  <div class="db style-d">
    last child (selected)
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
  border-bottom: 2px solid green;
  font-weight: bold;
}
```

### :nth-child()
**Type/Initial:** pseudo-class | (none)

**Description:** Selects elements based on their position among siblings.

**CSS:**
```css
/* Specific position */
li:nth-child(2) {
  color: blue;
}

/* Odd/even */
li:nth-child(odd) {
  background: lightgray;
}

li:nth-child(even) {
  background: lightyellow;
}

/* Formula */
li:nth-child(3n) {
  font-weight: bold;
}

li:nth-child(3n+1) {
  color: red;
}

li:nth-child(-n+3) {
  border-left: 3px solid blue;
}

li:nth-child(n+4) {
  opacity: 0.7;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    1
  </div>
  <div class="db style-c">
    2
  </div>
  <div class="db style-d">
    3
  </div>
  <div class="db style-e">
    4
  </div>
  <div class="db style-f">
    5
  </div>
  <div class="db style-g">
    6
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
  gap: 0.5rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightgray;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightyellow;
  color: blue;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightgray;
  font-weight: bold;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightyellow;
}
.style-f {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightgray;
}
.style-g {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightyellow;
}
```

### :nth-last-child()
**Type/Initial:** pseudo-class | (none)

**Description:** Selects elements based on position from the end.

**CSS:**
```css
li:nth-last-child(1) {
  color: red;
}

li:nth-last-child(odd) {
  background: lightgray;
}

li:nth-last-child(even) {
  background: lightyellow;
}

li:nth-last-child(3n) {
  font-weight: bold;
}

li:nth-last-child(-n+2) {
  border-right: 3px solid blue;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    1
  </div>
  <div class="db style-c">
    2
  </div>
  <div class="db style-d">
    3
  </div>
  <div class="db style-e">
    4
  </div>
  <div class="db style-f">
    5
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
  gap: 0.5rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightgray;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightyellow;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightgray;
  font-weight: bold;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightyellow;
  border-right: 3px solid blue;
}
.style-f {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightgray;
  border-right: 3px solid blue;
  color: red;
}
```

### :nth-of-type()
**Type/Initial:** pseudo-class | (none)

**Description:** Selects elements of a specific type among siblings.

**CSS:**
```css
p:nth-of-type(1) {
  font-size: 1.2em;
}

div:nth-of-type(odd) {
  background: lightgray;
}

span:nth-of-type(3n) {
  color: red;
}

p:nth-of-type(2) {
  font-style: italic;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    div 1
  </div>
  <div class="db style-c">
    div 2
  </div>
  <div class="db style-d">
    div 3
  </div>
  <div class="db style-e">
    div 4
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
  background: lightgray;
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
  background: lightgray;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### :nth-last-of-type()
**Type/Initial:** pseudo-class | (none)

**Description:** Selects elements of a specific type from the end.

**CSS:**
```css
p:nth-last-of-type(1) {
  font-size: 1.2em;
}

div:nth-last-of-type(odd) {
  background: lightgray;
}

span:nth-last-of-type(3n) {
  color: red;
}

p:nth-last-of-type(2) {
  font-style: italic;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    div 1
  </div>
  <div class="db style-c">
    div 2
  </div>
  <div class="db style-d">
    div 3
  </div>
  <div class="db style-e">
    div 4
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
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightgray;
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
  background: lightgray;
}
```

### :only-child
**Type/Initial:** pseudo-class | (none)

**Description:** Selects an element that is the only child of its parent.

**CSS:**
```css
li:only-child {
  font-weight: bold;
  color: blue;
}

.item:only-child {
  border: 2px solid green;
}

.card:only-child {
  background: lightyellow;
}

p:only-child {
  font-size: 1.2em;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    only child (selected)
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
  border: 2px solid green;
  font-weight: bold;
}
```

### :empty
**Type/Initial:** pseudo-class | (none)

**Description:** Selects elements with no children or text content.

**CSS:**
```css
div:empty {
  display: none;
}

.cell:empty {
  background: lightgray;
}

.input:empty::before {
  content: "Enter text...";
  color: #999;
}

.container:empty {
  border: 1px dashed #ccc;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    has content
  </div>
  <div class="db style-c">
  </div>
  <div class="db style-d">
    has content
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
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: lightgray;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

---

[Example](../examples/intermediate/01-structural-pseudo-classes/index.html)

← **Previous Topic:** [Logical Properties](../beginner/21-logical-properties.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Attribute Selectors](../intermediate/02-attribute-selectors.md) →

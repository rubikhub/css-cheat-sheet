# Pseudo Elements Advanced
---
## Container Properties
### ::before
**Type/Initial:** pseudo-element | (none)

**Description:** Inserts content before the element's content.

**CSS:**
```css
/* Basic content */
.icon::before {
  content: "★";
}

/* Unicode */
.arrow::before {
  content: "\2192";
}

/* Empty content for decoration */
.card::before {
  content: "";
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 4px;
  background: blue;
}

/* Quotes */
blockquote::before {
  content: open-quote;
}

/* Counter */
.list-item::before {
  content: counter(item) ". ";
  counter-increment: item;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    star icon
  </div>
  <div class="db style-c">
    arrow icon
  </div>
  <div class="db style-d">
    decorated
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
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  position: relative;
}
```

### ::after
**Type/Initial:** pseudo-element | (none)

**Description:** Inserts content after the element's content.

**CSS:**
```css
/* Basic content */
.icon::after {
  content: "★";
}

/* Clearfix */
.clearfix::after {
  content: "";
  display: table;
  clear: both;
}

/* Tooltip */
.tooltip::after {
  content: attr(data-tooltip);
  position: absolute;
  bottom: 100%;
  left: 50%;
  transform: translateX(-50%);
  padding: 0.5rem;
  background: black;
  color: white;
  border-radius: 4px;
  white-space: nowrap;
}

/* External link indicator */
a[target="_blank"]::after {
  content: " ↗";
}

/* Quote closing */
blockquote::after {
  content: close-quote;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    after content
  </div>
  <div class="db style-c">
    external link
  </div>
  <div class="db style-d">
    tooltip
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
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  position: relative;
}
```

### ::first-line
**Type/Initial:** pseudo-element | (none)

**Description:** Styles the first line of a block-level element.

**CSS:**
```css
p::first-line {
  font-weight: bold;
  color: blue;
}

h1::first-line {
  font-size: 1.5em;
}

blockquote::first-line {
  font-style: italic;
  text-transform: uppercase;
}

.article::first-line {
  color: #333;
  line-height: 1.6;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    This is a paragraph with enough text to demonstrate the first line styling effect.
  </div>
  <div class="db style-c">
    Another paragraph showing how first-line pseudo-element works with different styles.
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
  max-width: 300px;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border-left: 3px solid blue;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border-left: 3px solid blue;
}
```

### ::first-letter
**Type/Initial:** pseudo-element | (none)

**Description:** Styles the first letter of a block-level element.

**CSS:**
```css
p::first-letter {
  font-size: 2em;
  font-weight: bold;
  color: red;
  float: left;
  line-height: 1;
  margin-right: 0.1em;
}

h1::first-letter {
  font-size: 1.5em;
  color: blue;
}

blockquote::first-letter {
  font-size: 3em;
  font-weight: bold;
  color: #666;
  float: left;
  margin-right: 0.1em;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    First letter is styled larger and bolder.
  </div>
  <div class="db style-c">
    Drop cap effect using first-letter pseudo-element.
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
  border-left: 3px solid red;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border-left: 3px solid red;
}
```

### ::selection
**Type/Initial:** pseudo-element | (none)

**Description:** Styles the selected/highlighted text.

**CSS:**
```css
::selection {
  background: yellow;
  color: black;
}

p::selection {
  background: lightblue;
  color: darkblue;
}

h1::selection {
  background: lightgreen;
  color: darkgreen;
}

::selection {
  background: rgba(0, 120, 255, 0.3);
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    Select this text
  </div>
  <div class="db style-c">
    Select this text too
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
}
```

### ::placeholder
**Type/Initial:** pseudo-element | (none)

**Description:** Styles the placeholder text of form inputs.

**CSS:**
```css
input::placeholder {
  color: #999;
  font-style: italic;
}

input::placeholder {
  opacity: 0.7;
}

textarea::placeholder {
  color: #aaa;
  font-size: 0.9em;
}

input::placeholder {
  color: gray;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    placeholder text
  </div>
  <div class="db style-c">
    custom placeholder
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
  border: 1px solid #ccc;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border: 1px solid #ccc;
}
```
# Logic Matching Selectors
---
## Container Properties
### :is()
**Type/Initial:** pseudo-class | (none)

**Description:** Matches any element that can be selected by one of the selectors in its argument list.

**CSS:**
```css
/* Single selector */
:is(h1, h2, h3) {
  color: blue;
}

/* Nested selectors */
:is(.card, .panel):hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

/* With compound selectors */
:is(input, textarea, select):required {
  border-left: 3px solid red;
}

/* Specificity uses most specific argument */
:is(h1, .title, #main-title) {
  font-size: 2em;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    h1
  </div>
  <div class="db style-c">
    h2
  </div>
  <div class="db style-d">
    h3
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
  color: blue;
  font-weight: bold;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: blue;
  font-weight: bold;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: blue;
  font-weight: bold;
}
```

### :where()
**Type/Initial:** pseudo-class | (none)

**Description:** Like :is() but with zero specificity.

**CSS:**
```css
/* Zero specificity */
:where(h1, h2, h3) {
  color: blue;
}

:where(.card, .panel):hover {
  transform: translateY(-2px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
}

:where(input, textarea, select):required {
  border-left: 3px solid red;
}

/* Easy to override */
:where(h1, h2, h3) {
  color: blue;
}

h1 {
  color: red; /* This wins over :where() */
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    zero specificity
  </div>
  <div class="db style-c">
    easy to override
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

### :not()
**Type/Initial:** pseudo-class | (none)

**Description:** Selects elements that do not match the selector.

**CSS:**
```css
/* Single selector */
:not(.disabled) {
  opacity: 1;
}

:not(:last-child) {
  border-bottom: 1px solid #eee;
}

:not(input) {
  padding: 0.5rem;
}

/* Compound selector */
:not(.active):not(.disabled) {
  color: gray;
}

/* Complex */
:not(h1):not(h2):not(h3) {
  font-size: 1rem;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    active (selected)
  </div>
  <div class="db style-c">
    disabled (not selected)
  </div>
  <div class="db style-d">
    normal (selected)
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
  border-left: 3px solid blue;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: #f5f5f5;
  color: #999;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border-left: 3px solid blue;
}
```

### :has()
**Type/Initial:** pseudo-class | (none)

**Description:** Selects elements that contain a matching descendant.

**CSS:**
```css
/* Has child */
.card:has(img) {
  display: grid;
  grid-template-columns: 200px 1fr;
}

/* Has checked input */
.form:has(input:checked) {
  background: lightyellow;
}

/* Has focused input */
.group:has(input:focus) {
  border-color: blue;
}

/* Has any link */
nav:has(a:hover) {
  background: lightgray;
}

/* Complex */
.container:has(.error):has(.warning) {
  border: 2px solid orange;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    has image
  </div>
  <div class="db style-c">
    no image
  </div>
  <div class="db style-d">
    has image
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
  border: 2px solid blue;
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
  border: 2px solid blue;
}
```
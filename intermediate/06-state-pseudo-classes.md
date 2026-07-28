# State Pseudo Classes
---
## Container Properties
### :hover
**Type/Initial:** pseudo-class | (none)

**Description:** Selects elements when the mouse is over them.

**CSS:**
```css
a:hover {
  color: red;
  text-decoration: underline;
}

button:hover {
  background: darkblue;
  color: white;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
}

.item:hover {
  background: lightyellow;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    hover me
  </div>
  <div class="db style-c">
    hover me too
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
  transition: all 0.2s ease;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transition: all 0.2s ease;
}
```

### :active
**Type/Initial:** pseudo-class | (none)

**Description:** Selects elements when they are being activated (clicked).

**CSS:**
```css
a:active {
  color: red;
}

button:active {
  background: darkred;
  transform: scale(0.95);
}

.link:active {
  color: blue;
}

.card:active {
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2);
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    click me
  </div>
  <div class="db style-c">
    click me too
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
  transition: all 0.1s ease;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transition: all 0.1s ease;
}
```

### :focus
**Type/Initial:** pseudo-class | (none)

**Description:** Selects elements when they receive focus.

**CSS:**
```css
input:focus {
  border-color: blue;
  outline: none;
  box-shadow: 0 0 5px rgba(0, 0, 255, 0.5);
}

textarea:focus {
  border-color: green;
  outline: none;
}

a:focus {
  outline: 2px solid blue;
  outline-offset: 2px;
}

button:focus {
  outline: 2px solid green;
  outline-offset: 2px;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    focus on input below
  </div>
  <div class="db style-c">
    click to focus
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

### :visited
**Type/Initial:** pseudo-class | (none)

**Description:** Selects links that have been visited.

**CSS:**
```css
a:visited {
  color: purple;
}

a:visited:hover {
  color: red;
}

.link:visited {
  text-decoration: none;
  color: #551a8b;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    visited link
  </div>
  <div class="db style-c">
    unvisited link
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

### :focus-visible
**Type/Initial:** pseudo-class | (none)

**Description:** Selects elements when focused via keyboard (not mouse).

**CSS:**
```css
button:focus-visible {
  outline: 2px solid blue;
  outline-offset: 2px;
}

input:focus-visible {
  border-color: blue;
  box-shadow: 0 0 5px rgba(0, 0, 255, 0.5);
}

a:focus-visible {
  outline: 2px solid blue;
  outline-offset: 2px;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    tab to focus
  </div>
  <div class="db style-c">
    tab to focus
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

### :focus-within
**Type/Initial:** pseudo-class | (none)

**Description:** Selects an element when it or any descendant has focus.

**CSS:**
```css
form:focus-within {
  border-color: blue;
  box-shadow: 0 0 10px rgba(0, 0, 255, 0.3);
}

.card:focus-within {
  background: lightyellow;
}

.container:focus-within {
  outline: 2px solid blue;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    click inside card
  </div>
  <div class="db style-c">
    click inside card
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
  transition: all 0.2s ease;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  transition: all 0.2s ease;
}
```

### :target
**Type/Initial:** pseudo-class | (none)

**Description:** Selects the element whose ID matches the URL fragment.

**CSS:**
```css
:target {
  background: lightyellow;
  border: 2px solid blue;
}

.section:target {
  scroll-margin-top: 80px;
}

.tab:target {
  display: block;
}

.panel:target {
  opacity: 1;
  transform: translateY(0);
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    #section-1 (target)
  </div>
  <div class="db style-c">
    #section-2
  </div>
  <div class="db style-d">
    #section-3
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
}
```

---

[Example](../examples/intermediate/06-state-pseudo-classes/index.html)

← **Previous Topic:** [Form Pseudo Classes](../intermediate/05-form-pseudo-classes.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Border Advanced](../intermediate/07-border-advanced.md) →

# Form Pseudo Classes
---
## Container Properties
### :enabled
**Type/Initial:** pseudo-class | (none)

**Description:** Selects enabled form elements.

**CSS:**
```css
input:enabled {
  background: white;
  border: 1px solid #ccc;
}

button:enabled {
  background: blue;
  color: white;
  cursor: pointer;
}

select:enabled {
  border-color: green;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    enabled input
  </div>
  <div class="db style-c">
    enabled button
  </div>
  <div class="db style-d">
    disabled input
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
  background: blue;
  color: white;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  background: #f5f5f5;
  color: #999;
}
```

### :disabled
**Type/Initial:** pseudo-class | (none)

**Description:** Selects disabled form elements.

**CSS:**
```css
input:disabled {
  background: #f5f5f5;
  color: #999;
  cursor: not-allowed;
}

button:disabled {
  background: #ccc;
  color: #666;
  cursor: not-allowed;
}

select:disabled {
  background: #f5f5f5;
  border-color: #ddd;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    enabled
  </div>
  <div class="db style-c">
    disabled
  </div>
  <div class="db style-d">
    enabled
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
  background: #f5f5f5;
  color: #999;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### :checked
**Type/Initial:** pseudo-class | (none)

**Description:** Selects checked checkboxes and radio buttons.

**CSS:**
```css
input:checked {
  accent-color: blue;
}

input:checked + label {
  color: blue;
  font-weight: bold;
}

input:checked::before {
  content: "✓ ";
  color: green;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    checked
  </div>
  <div class="db style-c">
    unchecked
  </div>
  <div class="db style-d">
    checked
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
  border-left: 3px solid blue;
  font-weight: bold;
}
```

### :indeterminate
**Type/Initial:** pseudo-class | (none)

**Description:** Selects indeterminate checkboxes, radio groups, and progress bars.

**CSS:**
```css
input:indeterminate {
  accent-color: orange;
}

input:indeterminate + label {
  color: orange;
  font-style: italic;
}

progress:indeterminate {
  opacity: 0.7;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    indeterminate checkbox
  </div>
  <div class="db style-c">
    progress bar
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
  border-left: 3px solid orange;
  font-style: italic;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  opacity: 0.7;
}
```

### :placeholder-shown
**Type/Initial:** pseudo-class | (none)

**Description:** Selects inputs when placeholder is visible (empty).

**CSS:**
```css
input:placeholder-shown {
  border-color: #ccc;
  font-style: italic;
}

input:placeholder-shown + label {
  opacity: 0.5;
}

textarea:placeholder-shown {
  color: #999;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    empty (placeholder shown)
  </div>
  <div class="db style-c">
    has value
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
  font-style: italic;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border: 1px solid green;
}
```

### :required
**Type/Initial:** pseudo-class | (none)

**Description:** Selects required form elements.

**CSS:**
```css
input:required {
  border-left: 3px solid red;
}

input:required + label::after {
  content: " *";
  color: red;
}

select:required {
  border-color: red;
}

textarea:required {
  border-left: 3px solid red;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    required
  </div>
  <div class="db style-c">
    optional
  </div>
  <div class="db style-d">
    required
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
  border-left: 3px solid red;
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
  border-left: 3px solid red;
}
```

### :optional
**Type/Initial:** pseudo-class | (none)

**Description:** Selects optional form elements.

**CSS:**
```css
input:optional {
  border-left: 3px solid green;
}

input:optional + label {
  color: green;
}

select:optional {
  border-color: green;
}

textarea:optional {
  border-left: 3px solid green;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    optional
  </div>
  <div class="db style-c">
    required
  </div>
  <div class="db style-d">
    optional
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
  border-left: 3px solid green;
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
  border-left: 3px solid green;
}
```
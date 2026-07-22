# Combinators Advanced
---
## Container Properties
### ~ (General Sibling)
**Type/Initial:** selector | (none)

**Description:** Selector — targets all siblings that come after the element.

**CSS:**
```css
/* All siblings after */
h2 ~ p {
  color: gray;
}

.active ~ .item {
  opacity: 0.5;
}

.checked ~ label {
  font-weight: bold;
}

.selected ~ .option {
  background: lightblue;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    heading
  </div>
  <div class="db style-c">
    paragraph 1
  </div>
  <div class="db style-d">
    paragraph 2
  </div>
  <div class="db style-e">
    paragraph 3
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
  border-left: 3px solid blue;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border-left: 3px solid gray;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border-left: 3px solid gray;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border-left: 3px solid gray;
}
```

### + (Adjacent Sibling)
**Type/Initial:** selector | (none)

**Description:** Selector — targets the immediately following sibling.

**CSS:**
```css
/* Immediately after */
h2 + p {
  font-weight: bold;
}

.active + .item {
  border-left: 3px solid green;
}

.checked + label {
  color: blue;
}

.selected + .option {
  background: lightyellow;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    heading
  </div>
  <div class="db style-c">
    first paragraph (adjacent)
  </div>
  <div class="db style-d">
    second paragraph (not adjacent)
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
  border-left: 3px solid blue;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border-left: 3px solid green;
  font-weight: bold;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### > (Child)
**Type/Initial:** selector | (none)

**Description:** Selector — targets direct children only.

**CSS:**
```css
/* Direct children */
.nav > li {
  display: inline-block;
}

.container > .item {
  margin-bottom: 1rem;
}

.list > li {
  padding: 0.5rem;
}

.grid > div {
  border: 1px solid #ddd;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    direct child
  </div>
  <div class="db style-c">
    <div class="db style-d">
      nested (not targeted)
    </div>
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
  border: 2px solid blue;
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
}
.style-d {
  background: #f5f5f5;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border: 1px dashed #999;
}
```

### (space) Descendant
**Type/Initial:** selector | (none)

**Description:** Selector — targets all descendants at any depth.

**CSS:**
```css
/* All descendants */
nav a {
  text-decoration: none;
}

.container p {
  margin-bottom: 1rem;
}

.card h2 {
  font-size: 1.2rem;
}

.list li {
  padding: 0.5rem;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    direct child
  </div>
  <div class="db style-c">
    <div class="db style-d">
      nested descendant
    </div>
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
  border: 2px solid blue;
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
}
.style-d {
  background: #f5f5f5;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border-left: 3px solid blue;
}
```
# Attribute Selectors
---
## Container Properties
### [attr]
**Type/Initial:** selector | (none)

**Description:** Selector — targets elements that have the specified attribute.

**CSS:**
```css
/* Has attribute */
[title] {
  color: red;
}

[href] {
  color: blue;
}

[data-active] {
  font-weight: bold;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    has title
  </div>
  <div class="db style-c">
    no title
  </div>
  <div class="db style-d">
    has data-active
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
  border-left: 3px solid blue;
}
```

### [attr="value"]
**Type/Initial:** selector | (none)

**Description:** Selector — targets elements with exact attribute value match.

**CSS:**
```css
/* Exact match */
[type="text"] {
  border: 2px solid blue;
}

[type="email"] {
  border: 2px solid green;
}

[type="password"] {
  border: 2px solid red;
}

[data-status="active"] {
  background: lightgreen;
}

[data-status="inactive"] {
  background: lightcoral;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    type="text"
  </div>
  <div class="db style-c">
    type="email"
  </div>
  <div class="db style-d">
    type="password"
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
  border-left: 3px solid green;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border-left: 3px solid red;
}
```

### [attr~="value"]
**Type/Initial:** selector | (none)

**Description:** Selector — targets elements where attribute value contains the word.

**CSS:**
```css
[class~="highlight"] {
  background: yellow;
}

[class~="active"] {
  border: 2px solid green;
}

[class~="primary"] {
  color: blue;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    highlight
  </div>
  <div class="db style-c">
    active primary
  </div>
  <div class="db style-d">
    regular
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
  background: lightyellow;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border: 2px solid green;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### [attr|="value"]
**Type/Initial:** selector | (none)

**Description:** Selector — targets elements with exact value or value followed by hyphen.

**CSS:**
```css
[hreflang|="en"] {
  color: blue;
}

[hreflang|="fr"] {
  color: red;
}

[data-lang|="zh"] {
  font-weight: bold;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    en
  </div>
  <div class="db style-c">
    en-US
  </div>
  <div class="db style-d">
    fr
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
  border-left: 3px solid blue;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  border-left: 3px solid red;
}
```

### [attr^="value"]
**Type/Initial:** selector | (none)

**Description:** Selector — targets elements where attribute value starts with the specified string.

**CSS:**
```css
[href^="https"] {
  color: green;
}

[href^="http"] {
  color: orange;
}

[data-id^="user-"] {
  font-weight: bold;
}

[src^="/images/"] {
  border: 1px solid #ccc;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    https://...
  </div>
  <div class="db style-c">
    http://...
  </div>
  <div class="db style-d">
    ftp://...
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
  border-left: 3px solid orange;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### [attr$="value"]
**Type/Initial:** selector | (none)

**Description:** Selector — targets elements where attribute value ends with the specified string.

**CSS:**
```css
[href$=".pdf"] {
  color: red;
}

[href$=".zip"] {
  color: orange;
}

[src$=".jpg"] {
  border: 1px solid #ccc;
}

[data-file$=".png"] {
  font-weight: bold;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    .pdf
  </div>
  <div class="db style-c">
    .zip
  </div>
  <div class="db style-d">
    .txt
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
  border-left: 3px solid orange;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### [attr*="value"]
**Type/Initial:** selector | (none)

**Description:** Selector — targets elements where attribute value contains the substring.

**CSS:**
```css
[href*="example"] {
  color: purple;
}

[data-name*="admin"] {
  font-weight: bold;
}

[class*="btn"] {
  padding: 0.5rem 1rem;
}

[src*="avatar"] {
  border-radius: 50%;
}
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    contains example
  </div>
  <div class="db style-c">
    no match
  </div>
  <div class="db style-d">
    another example here
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
  border-left: 3px solid purple;
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
  border-left: 3px solid purple;
}
```

---

[Example](../examples/intermediate/02-attribute-selectors/index.html)

← **Previous Topic:** [Structural Pseudo Classes](../intermediate/01-structural-pseudo-classes.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Combinators Advanced](../intermediate/03-combinators-advanced.md) →

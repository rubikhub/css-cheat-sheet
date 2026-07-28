# Basic Selectors

> 8 selectors

Fundamental ways to target HTML elements for styling.

---

## Universal Selector

**Syntax:** `*`

Targets all elements in the document.

**Values:**
- `*` — all elements
- `*` — commonly used with box-sizing

**Use Cases:**
- Reset default margins/padding
- Apply box-sizing globally
- Create CSS resets

**Example:**
```css
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}
```

---

## Element Selector

**Syntax:** `element`

Targets all elements of a given type.

**Values:**
- `p` — all paragraph elements
- `h1` — all h1 elements
- `div` — all div elements
- `a` — all anchor elements
- `img` — all image elements

**Use Cases:**
- Set base styles for element types
- Create default typography

**Example:**
```css
p {
  line-height: 1.6;
  margin-bottom: 1rem;
}

h1 {
  font-size: 2rem;
  font-weight: 700;
}
```

---

## Class Selector

**Syntax:** `.class`

Targets elements with a specific class attribute.

**Values:**
- `.button` — elements with class="button"
- `.card` — elements with class="card"
- `.active` — elements with class="active"
- `.primary` — elements with class="primary"

**Use Cases:**
- Style reusable components
- Create variant styles
- Apply specific styling to groups

**Example:**
```css
.button {
  background: #0066cc;
  color: white;
  padding: 0.5rem 1rem;
}

.card {
  border: 1px solid #e0e0e0;
  border-radius: 8px;
}
```

---

## ID Selector

**Syntax:** `#id`

Targets a single element with a specific id attribute.

**Values:**
- `#header` — element with id="header"
- `#main-content` — element with id="main-content"
- `#footer` — element with id="footer"
- `#hero` — element with id="hero"

**Use Cases:**
- Style unique page sections
- Target specific elements for JavaScript
- Create page-specific overrides

**Example:**
```css
#header {
  background: #333;
  color: white;
  padding: 1rem;
}

#hero {
  background: linear-gradient(135deg, #667eea, #764ba2);
}
```

---


## Attribute Selector

**Syntax:** `[attribute]` | `[attribute="value"]`

Targets elements with specific attributes or values.

**Values:**
- `[href]` — elements with href attribute
- `[type="text"]` — exact attribute match


**Use Cases:**
- Style form inputs by type
- Target elements with data attributes
- Style links based on attributes

**Example:**
```css
[type="text"] {
  border: 1px solid #ccc;
  padding: 0.5rem;
}

[href] {
  color: #0066cc;
}

```


---

**[View Example](../examples/beginner/05-basic-selectors/index.html)**

← **Previous Topic:** [Inheritance](../beginner/04-inheritance.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Combinators Basics](../beginner/06-combinators-basics.md) →

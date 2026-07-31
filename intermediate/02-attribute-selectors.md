# Attribute Selectors

> 5 selectors

Target elements based on the presence or value of their attributes.

---

## Selectors

---

## [attr~="value"]

**Syntax:** `[attr~="value"]`

Targets elements whose attribute value contains the word in a space-separated list.

**Values:**
- `[class~="highlight"]` — elements with highlight in the class
- `[class~="active"]` — elements with active in the class
- `[class~="primary"]` — elements with primary in the class

**Use Cases:**
- Target elements by a word in a token list
- Style elements that share a class token

**Example:**
```css
[class~="highlight"] {
  background: yellow;
}

[class~="active"] {
  border: 2px solid green;
}
```

---

## [attr|="value"]

**Syntax:** `[attr|="value"]`

Targets elements with an exact value or value followed by a hyphen.

**Values:**
- `[hreflang|="en"]` — hreflang "en" or "en-US"
- `[hreflang|="fr"]` — hreflang "fr" or "fr-CA"
- `[data-lang|="zh"]` — data-lang "zh" or "zh-CN"

**Use Cases:**
- Target language codes with region variants
- Match attribute values by prefix segment

**Example:**
```css
[hreflang|="en"] {
  color: blue;
}

[hreflang|="fr"] {
  color: red;
}
```

---

## [attr^="value"]

**Syntax:** `[attr^="value"]`

Targets elements whose attribute value starts with the specified string.

**Values:**
- `[href^="https"]` — secure links
- `[href^="http"]` — links over HTTP
- `[data-id^="user-"]` — elements with a user- prefixed data-id
- `[src^="/images/"]` — images from the images folder

**Use Cases:**
- Distinguish external and secure links
- Target elements by value prefix

**Example:**
```css
[href^="https"] {
  color: green;
}

[data-id^="user-"] {
  font-weight: bold;
}
```

---

## [attr$="value"]

**Syntax:** `[attr$="value"]`

Targets elements whose attribute value ends with the specified string.

**Values:**
- `[href$=".pdf"]` — links to PDF files
- `[href$=".zip"]` — links to ZIP archives
- `[src$=".jpg"]` — JPG images
- `[data-file$=".png"]` — elements pointing to PNG files

**Use Cases:**
- Style links by file type
- Target images by extension

**Example:**
```css
[href$=".pdf"] {
  color: red;
}

[href$=".zip"] {
  color: orange;
}
```

---

## [attr*="value"]

**Syntax:** `[attr*="value"]`

Targets elements whose attribute value contains the substring.

**Values:**
- `[href*="example"]` — links containing example
- `[data-name*="admin"]` — elements with admin in the name
- `[class*="btn"]` — elements with btn in the class
- `[src*="avatar"]` — images with avatar in the src

**Use Cases:**
- Style links by URL substring
- Target elements by partial values

**Example:**
```css
[href*="example"] {
  color: purple;
}

[class*="btn"] {
  padding: 0.5rem 1rem;
}
```

---

**[View Example](../examples/intermediate/02-attribute-selectors/index.html)**

← **Previous Topic:** [Structural Pseudo Classes](../intermediate/01-structural-pseudo-classes.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Logic Matching Selectors](../intermediate/04-logic-matching-selectors.md) →

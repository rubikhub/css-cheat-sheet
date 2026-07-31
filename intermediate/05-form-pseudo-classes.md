# Form Pseudo Classes

> 7 pseudo-classes

Target form elements based on their state and validation status.

---

## States

---

## :enabled

**Syntax:** `:enabled`

Selects enabled form elements.

**Values:**
- `input:enabled` — enabled inputs
- `button:enabled` — enabled buttons
- `select:enabled` — enabled selects

**Use Cases:**
- Style enabled form controls
- Differentiate enabled and disabled fields

**Example:**
```css
input:enabled {
  background: white;
  border: 1px solid #ccc;
}

button:enabled {
  background: blue;
  color: white;
}
```

---

## :disabled

**Syntax:** `:disabled`

Selects disabled form elements.

**Values:**
- `input:disabled` — disabled inputs
- `button:disabled` — disabled buttons
- `select:disabled` — disabled selects

**Use Cases:**
- Visually disable form fields
- Show that a control cannot be used

**Example:**
```css
input:disabled {
  background: #f5f5f5;
  color: #999;
  cursor: not-allowed;
}

button:disabled {
  background: #ccc;
  color: #666;
}
```

---

## :checked

**Syntax:** `:checked`

Selects checked checkboxes and radio buttons.

**Values:**
- `input:checked` — checked inputs
- `input:checked + label` — label next to a checked input
- `input:checked::before` — marker on a checked input

**Use Cases:**
- Style selected options
- Highlight the label of a checked input

**Example:**
```css
input:checked {
  accent-color: blue;
}

input:checked + label {
  color: blue;
  font-weight: bold;
}
```

---

## :indeterminate

**Syntax:** `:indeterminate`

Selects indeterminate checkboxes, radio groups, and progress bars.

**Values:**
- `input:indeterminate` — indeterminate checkboxes
- `input:indeterminate + label` — label next to an indeterminate input
- `progress:indeterminate` — indeterminate progress bars

**Use Cases:**
- Style tri-state checkboxes
- Style progress bars without a value

**Example:**
```css
input:indeterminate {
  accent-color: orange;
}

progress:indeterminate {
  opacity: 0.7;
}
```

---

## :placeholder-shown

**Syntax:** `:placeholder-shown`

Selects inputs when the placeholder is visible (empty).

**Values:**
- `input:placeholder-shown` — empty inputs showing a placeholder
- `input:placeholder-shown + label` — label next to an empty input
- `textarea:placeholder-shown` — empty textareas

**Use Cases:**
- Style empty inputs differently
- Hide labels until a field has a value

**Example:**
```css
input:placeholder-shown {
  border-color: #ccc;
  font-style: italic;
}

textarea:placeholder-shown {
  color: #999;
}
```

---

## :required

**Syntax:** `:required`

Selects required form elements.

**Values:**
- `input:required` — required inputs
- `input:required + label::after` — add a required marker to the label
- `select:required` — required selects
- `textarea:required` — required textareas

**Use Cases:**
- Highlight mandatory fields
- Add an asterisk to required labels

**Example:**
```css
input:required {
  border-left: 3px solid red;
}

input:required + label::after {
  content: " *";
  color: red;
}
```

---

## :optional

**Syntax:** `:optional`

Selects optional form elements.

**Values:**
- `input:optional` — optional inputs
- `input:optional + label` — label next to an optional input
- `select:optional` — optional selects
- `textarea:optional` — optional textareas

**Use Cases:**
- De-emphasize optional fields
- Mark fields that are not required

**Example:**
```css
input:optional {
  border-left: 3px solid green;
}

select:optional {
  border-color: green;
}
```

---

**[View Example](../examples/intermediate/05-form-pseudo-classes/index.html)**

← **Previous Topic:** [Logic Matching Selectors](../intermediate/04-logic-matching-selectors.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [State Pseudo Classes](../intermediate/06-state-pseudo-classes.md) →
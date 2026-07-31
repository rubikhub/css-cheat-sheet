# Form Pseudo Classes

> 13 pseudo-classes

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

## :valid / :invalid

**Syntax:** `:valid` | `:invalid`

Match form fields that pass or fail constraint validation.

**Values:**
- `input:valid` — value meets its constraints
- `input:invalid` — value violates its constraints
- `:invalid` also matches empty required fields before interaction

**Use Cases:**
- Style valid and invalid inputs
- Show error borders

**Example:**
```css
input:valid {
  border-color: green;
}

input:invalid {
  border-color: red;
}
```

---

## :in-range / :out-of-range

**Syntax:** `:in-range` | `:out-of-range`

Match numeric inputs whose value is inside or outside their min/max range.

**Values:**
- `input:in-range` — value within the allowed range
- `input:out-of-range` — value outside the allowed range

**Use Cases:**
- Highlight out-of-range number inputs

**Example:**
```css
input[type='number']:out-of-range {
  background: #ffe9e9;
}
```

---

## :read-only / :read-write

**Syntax:** `:read-only` | `:read-write`

Match elements based on whether they are editable.

**Values:**
- `input:read-only` — non-editable fields
- `textarea:read-only` — read-only text areas
- `[contenteditable]:read-write` — editable content

**Use Cases:**
- Style read-only form views
- Indicate editable content

**Example:**
```css
input:read-only {
  background: #f3f4f6;
}

[contenteditable]:read-write {
  outline: 1px dashed #999;
}
```

---

## :autofill

**Syntax:** `:autofill`

Matches inputs that the browser has autofilled.

**Values:**
- `input:autofill` — autofilled inputs
- Pair with `-webkit-autofill` for Safari

**Use Cases:**
- Restyle autofilled backgrounds
- Remove the default yellow fill

**Example:**
```css
input:autofill {
  background-color: #eef2ff;
}
```

---

## :default

**Syntax:** `:default`

Matches the default item in a group of choices.

**Values:**
- `button:default` — the default submit button
- `input:default` — the default-checked radio or checkbox

**Use Cases:**
- Emphasize the primary submit button

**Example:**
```css
button:default {
  box-shadow: 0 0 0 3px #2563eb;
}
```

---

**[View Example](../examples/intermediate/10-form-pseudo-classes/index.html)**

← **Previous Topic:** [Structural Pseudo Classes](../intermediate/09-structural-pseudo-classes.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [State Pseudo Classes](../intermediate/11-state-pseudo-classes.md) →

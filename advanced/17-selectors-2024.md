# Selectors 2024+

Cutting-edge selectors and matching functions.

---

## :has() (Deep)

Selects elements containing specific descendants.

```css
/* Parent with specific child */
form:has(input[type="password"]) { /* ... */ }

/* Adjacent sibling state */
label:has(+ input:focus) { color: blue; }

/* Complex matching */
article:has(img):not(:has(video)) { grid-template-rows: 200px 1fr; }
```

---

## :is() (Specificity)

Matches any element in the selector list. Takes the **highest specificity** of its arguments.

```css
/* Specificity = highest argument (h1 = 0,1,0) */
:is(h1, h2, h3) {
  line-height: 1.2;
}

/* Specificity = 0,0,1 (only .card) */
:is(.card) h2 {
  font-size: 1.25rem;
}
```

---

## :where() (Zero Specificity)

Same as `:is()` but always has **zero specificity**.

```css
/* Specificity = 0,0,1 (only h2) — easy to override */
:where(h1, h2, h3) {
  line-height: 1.2;
}

/* Useful for resets */
:where(ul, ol) {
  list-style: none;
  padding: 0;
}
```

---

## :user-valid
**Type:** pseudo-class

Matches input that the browser considers valid **after user interaction**.

```css
input:user-valid {
  border-color: green;
}

input:user-invalid {
  border-color: red;
}
```

---

## :open
**Type:** pseudo-class

Selects elements that are in an "open" state (details, select, dialog).

```css
details:open {
  border: 2px solid blue;
}

details:open::marker {
  content: "▼ ";
}

select:open {
  background: yellow;
}
```

---

## :popover-open
**Type:** pseudo-class

Selects elements currently shown as popovers.

```css
[popover-open] {
  opacity: 1;
  transform: translateY(0);
}
```

---

## @scope (in Selectors context)

```css
/* Scope with limit */
@scope (.card) to (.card-footer) {
  p { color: #333; }
  /* p inside .card-footer won't be affected */
}
```

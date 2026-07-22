# CSS At-Rules — Advanced

Modern at-rules for layers, properties, scope, and view transitions.

---

## @property
**Type:** at-rule

Declares custom properties with type, initial value, and inheritance.

```css
@property --my-color {
  syntax: '<color>';
  initial-value: #333;
  inherits: false;
}

@property --my-size {
  syntax: '<length>';
  initial-value: 1rem;
  inherits: true;
}

@property --my-number {
  syntax: '<number>';
  initial-value: 1;
  inherits: false;
}

/* Usage */
.box {
  color: var(--my-color);
  font-size: var(--my-size);
  opacity: var(--my-number);
}
```

---

## @layer
**Type:** at-rule

Defines cascade layers for explicit specificity ordering.

```css
/* Declare layers */
@layer base, components, utilities;

@layer base {
  body { font-family: sans-serif; }
  p { line-height: 1.5; }
}

@layer components {
  .card { padding: 1rem; border: 1px solid #eee; }
}

@layer utilities {
  .hidden { display: none; }
  .flex { display: flex; }
}
```

---

## @scope
**Type:** at-rule

Scopes styles to a specific DOM subtree with a scoping root and optional limit.

```css
@scope (.card) to (.card-footer) {
  p { color: #333; }
  a { color: blue; }
}

/* Without limit */
@scope (.dropdown) {
  .menu { display: none; }
  .menu.open { display: block; }
}
```

---

## @starting-style
**Type:** at-rule

Defines styles for elements about to be displayed (enter transition).

```css
@starting-style {
  .toast {
    opacity: 0;
    transform: translateY(20px);
  }
}

.toast {
  opacity: 1;
  transform: translateY(0);
  transition: opacity 0.3s, transform 0.3s;
}
```

---

## @view-transition
**Type:** at-rule

Enables view transitions for navigation.

```css
@view-transition {
  navigation: auto;
}
```

---

## @counter-style
**Type:** at-rule

Defines custom counter styles.

```css
@counter-style thumbs {
  system: cyclic;
  symbols: "\1F44D";
  suffix: " ";
}

@counter-style checkmarks {
  system: cyclic;
  symbols: "\2714";
  suffix: " ";
}

ol {
  list-style-type: thumbs;
}
```

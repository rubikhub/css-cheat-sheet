# Inheritance

CSS properties cascade down from parent to child elements. This is called **inheritance**.

> Source: [web.dev/learn/css/inheritance](https://web.dev/learn/css/inheritance)

---

## How Inheritance Works

Properties that are inherited by default pass their value from parent to child. If a parent has `color: blue`, all children will also be blue — unless they override it.

```html
<html>
  <body>
    <article>
      <p>This text inherits color from html.</p>
    </article>
  </body>
</html>
```

```css
html {
  color: lightslategray;
}

/* All elements inherit color: lightslategray */
```

Inheritance only flows **downward** — children inherit from parents, not the other way around.

---

## Which Properties Inherit?

### Inherited by Default

- `color`
- `font-family`, `font-size`, `font-style`, `font-weight`
- `line-height`, `letter-spacing`, `word-spacing`
- `text-align`, `text-indent`, `text-transform`
- `cursor`
- `visibility`
- `white-space`
- `list-style`, `list-style-type`, `list-style-position`
- `border-collapse`, `border-spacing`
- `caption-side`, `empty-cells`
- `direction`, `quotes`
- `orphans`, `widows`

### Not Inherited by Default

- `width`, `height`, `margin`, `padding`, `border`
- `background`, `display`, `position`
- `overflow`, `z-index`, `opacity`
- `box-sizing`, `float`, `clear`

---

## Controlling Inheritance

### `inherit`

Forces a property to use its parent's computed value.

```css
strong {
  font-weight: 900;
}

.component strong {
  font-weight: inherit;
}

/* Now <strong> inside .component matches its parent's weight */
```

### `initial`

Resets a property to its CSS default (initial) value.

```css
aside strong {
  font-weight: initial;
}

/* <strong> inside <aside> reverts to normal weight (400) */
```
---

## Practical Example

```css
/* Global style */
body {
  font-family: Arial, sans-serif;
  font-size: 16px;
  color: #333;
}

/* All elements inherit these from body */
```

```html
<body>
  <div>
    <p>This inherits font-family, font-size, and color from body.</p>
  </div>
</body>
```

---

## Quick Reference

| Keyword | Behavior |
|---------|----------|
| `inherit` | Use parent's value |
| `initial` | Use property's CSS default |

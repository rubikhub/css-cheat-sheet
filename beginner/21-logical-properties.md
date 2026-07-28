# Logical Properties

Logical properties map to the **writing direction** of the document, making layouts work for LTR and RTL languages without changing CSS.

> Source: [web.dev/learn/css/logical-properties](https://web.dev/learn/css/logical-properties)

---

## Physical vs Logical

Physical properties are absolute directions (top, right, bottom, left). Logical properties are relative to text flow (inline, block).

```
Physical:              Logical:

  top                    block-start
   ↑                       ↑
left ← → right      inline-start ← → inline-end
   ↓                       ↓
  bottom                 block-end
```

---

## Writing Modes

```css
/* Left-to-right (default for English) */
direction: ltr;
writing-mode: horizontal-tb;

/* Right-to-left (Arabic, Hebrew) */
direction: rtl;
writing-mode: horizontal-tb;

/* Vertical (Japanese, Chinese) */
writing-mode: vertical-rl;
```

---

## Margin Logical Properties

| Physical | Logical |
|----------|---------|
| `margin-top` | `margin-block-start` |
| `margin-bottom` | `margin-block-end` |
| `margin-left` | `margin-inline-start` |
| `margin-right` | `margin-inline-end` |
| — | `margin-block` (top & bottom) |
| — | `margin-inline` (left & right) |

```css
/* Shorthand */
margin-block: 1rem;         /* top + bottom */
margin-block: 1rem 2rem;    /* top bottom */
margin-inline: 1rem;        /* left + right */
margin-inline: 1rem 2rem;   /* left right */

/* Individual */
margin-block-start: 1rem;
margin-block-end: 0.5rem;
margin-inline-start: 2rem;
margin-inline-end: 0;
```

---

## Padding Logical Properties

| Physical | Logical |
|----------|---------|
| `padding-top` | `padding-block-start` |
| `padding-bottom` | `padding-block-end` |
| `padding-left` | `padding-inline-start` |
| `padding-right` | `padding-inline-end` |
| — | `padding-block` (top & bottom) |
| — | `padding-inline` (left & right) |

```css
.card {
  padding-block: 1rem;
  padding-inline: 1.5rem;
}

/* Individual */
padding-block-start: 2rem;
padding-inline-end: 1rem;
```

---

## Border Logical Properties

| Physical | Logical |
|----------|---------|
| `border-top` | `border-block-start` |
| `border-bottom` | `border-block-end` |
| `border-left` | `border-inline-start` |
| `border-right` | `border-inline-end` |
| — | `border-block` |
| — | `border-inline` |

```css
.card {
  border-block: 2px solid #333;
  border-inline: 1px solid #666;
}

/* Individual sides */
border-block-start: 3px solid blue;
border-inline-end: 1px dashed red;
```

### Border Radius

| Physical | Logical |
|----------|---------|
| `border-top-left-radius` | `border-start-start-radius` |
| `border-top-right-radius` | `border-start-end-radius` |
| `border-bottom-left-radius` | `border-end-start-radius` |
| `border-bottom-right-radius` | `border-end-end-radius` |

```css
.card {
  border-start-start-radius: 8px;
  border-start-end-radius: 8px;
}
```

---

## Size Logical Properties

| Physical | Logical |
|----------|---------|
| `width` | `inline-size` |
| `height` | `block-size` |
| `min-width` | `min-inline-size` |
| `min-height` | `min-block-size` |
| `max-width` | `max-inline-size` |
| `max-height` | `max-block-size` |

```css
.sidebar {
  inline-size: 300px;
  min-block-size: 100vh;
}

.container {
  max-inline-size: 1200px;
  block-size: auto;
}
```

---

## Inset (Positioning) Logical Properties

| Physical | Logical |
|----------|---------|
| `top` | `inset-block-start` |
| `bottom` | `inset-block-end` |
| `left` | `inset-inline-start` |
| `right` | `inset-inline-end` |
| — | `inset-block` (top & bottom) |
| — | `inset-inline` (left & right) |
| — | `inset` (all sides) |

```css
.fixed-header {
  position: fixed;
  inset-block-start: 0;
  inset-inline: 0;
}

.modal {
  position: fixed;
  inset: 0;  /* Centers the modal */
}
```

---

## Text Alignment

| Physical | Logical |
|----------|---------|
| `text-align: left` | `text-align: start` |
| `text-align: right` | `text-align: end` |

```css
[dir="ltr"] p { text-align: start; }  /* Left */
[dir="rtl"] p { text-align: start; }  /* Right */
```

---

## Quick Reference

| Category | Physical | Logical |
|----------|----------|---------|
| Margin | `margin-top` | `margin-block-start` |
| Padding | `padding-left` | `padding-inline-start` |
| Border | `border-right` | `border-inline-end` |
| Size | `width` | `inline-size` |
| Position | `top` | `inset-block-start` |
| Text | `text-align: left` | `text-align: start` |

---

## Why Use Logical Properties?

- **RTL support** — Layouts automatically adapt to right-to-left languages
- **Writing modes** — Works with vertical text
- **Future-proof** — More flexible than physical directions
- **Less code** — No need for separate RTL stylesheets


---

**[View Example](../examples/beginner/21-logical-properties/index.html)**

← **Previous Topic:** [Gradients Basics](../beginner/20-gradients-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Structural Pseudo Classes](../intermediate/01-structural-pseudo-classes.md) →

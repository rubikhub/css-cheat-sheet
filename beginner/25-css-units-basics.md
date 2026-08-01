# CSS Units Basics

> 6 units

The fundamental units for sizing text, spacing, and layout — absolute, relative, and viewport units.

> Source: [web.dev/learn/css/sizing](https://web.dev/learn/css/sizing)

---

## What Is a Unit?

Every CSS length is a number plus a unit. The unit decides how that number is turned into a rendered size.

```
16px      → absolute (fixed on screen)
1.5rem    → relative to root font size
50%       → relative to parent
100vw     → relative to viewport
```

Choose the right unit and your layout stays predictable; mix them carelessly and sizes drift.

---

## Absolute Units

### px — Pixels

**Syntax:** `<length>px`

The basic unit of screen measurement — fixed, predictable, and the most common length unit.

**Values:**
- `1px` — one CSS pixel (not necessarily one physical screen pixel)
- `16px` — typical default font size
- `0.5px` — fractional pixels allowed

**Use Cases:**
- Fixed-width elements
- Border widths and small details
- Fallback sizes in fluid layouts

**Example:**
```css
.box {
  width: 200px;
  padding: 12px;
  border: 1px solid #333;
}
```

### Physical Absolute Units

| Unit | Name | Size |
|------|------|------|
| `in` | inches | 96px |
| `cm` | centimeters | ~37.8px |
| `mm` | millimeters | ~3.78px |
| `pt` | points | 1/72 inch (~1.33px) |
| `pc` | picas | 12pt (~16px) |
| `q` | quarter-millimeters | ~0.94px |

```css
/* Mostly used for print stylesheets */
@page {
  margin: 2cm;
}
```

---

## Relative Units

### em — Relative to Font Size

**Syntax:** `<length>em`

Relative to the **parent** element's font size. Chains of nested `em` values compound.

**Values:**
- `1em` — same as parent font size
- `2em` — twice the parent font size
- `0.5em` — half the parent font size

**Use Cases:**
- Sizing padding that scales with text
- Font-size that follows its container

**Example:**
```css
.container { font-size: 16px; }

.container .child {
  font-size: 1.5em;   /* = 24px */
  padding: 1em;       /* = 24px (scales with child font) */
}
```

---

### rem — Relative to Root

**Syntax:** `<length>rem`

Relative to the **root** (`html`) element's font size. Does not compound through nesting.

**Values:**
- `1rem` — same as root font size
- `2rem` — twice the root font size
- `0.5rem` — half the root font size

**Use Cases:**
- Consistent spacing across the whole site
- Typographic scales that ignore nesting

**Example:**
```css
html { font-size: 16px; }

h1   { font-size: 2rem; }    /* = 32px everywhere */
p    { font-size: 1rem; }    /* = 16px everywhere */
```

---

## Percentage (%)

**Syntax:** `<percentage>%`

Relative to the **parent** — width is relative to the parent's width, font-size is relative to the parent's font-size.

**Values:**
- `100%` — same as parent
- `50%` — half the parent
- `200%` — double the parent

**Use Cases:**
- Fluid widths and layouts
- Image and media responsiveness
- Centering with transforms

**Example:**
```css
.container {
  width: 80%;
  margin-inline: auto;
}

.child {
  width: 50%;   /* half of the container */
}
```

> **Note:** `%` for `padding` and `margin` is always relative to the parent's **width**, not height.

---

## Viewport Units

### vw and vh — Viewport Width / Height

**Syntax:** `<length>vw` | `<length>vh`

Relative to the browser **viewport** (visible window area). `1vw` = 1% of viewport width, `1vh` = 1% of viewport height.

**Values:**
- `100vw` — full viewport width
- `100vh` — full viewport height
- `50vw` — half the viewport width

**Use Cases:**
- Full-screen hero sections
- Viewport-sized layouts
- Fluid type that scales with the window

**Example:**
```css
.hero {
  width: 100vw;
  height: 100vh;
}

.fullscreen {
  height: 100vh;   /* fills the screen */
}
```

> **Note:** `100vw` includes the scrollbar width — prefer `width: 100%` on containers that should fit inside the page.

---

## Unitless Values

Some properties accept numbers **without** a unit.

**Values:**
- `line-height: 1.5` — multiplier of font size
- `z-index: 10` — stacking order
- `opacity: 0.8` — 0 to 1
- `flex: 1` — flex growth factor
- `font-weight: 700` — typeface weight

**Use Cases:**
- Scalable line-height that stays proportional
- Grid and flex proportions

**Example:**
```css
p {
  line-height: 1.5;   /* 1.5 × font-size */
  flex: 1;            /* grow to fill space */
}
```

---

## Quick Reference

| Unit | Type | Relative To |
|------|------|-------------|
| `px` | absolute | device pixels |
| `%` | relative | parent size |
| `em` | relative | parent font-size |
| `rem` | relative | root font-size |
| `vw` | viewport | viewport width |
| `vh` | viewport | viewport height |

---

**[View Example](../examples/beginner/25-css-units-basics/index.html)**

← **Previous Topic:** [Logical Properties](../beginner/24-logical-properties.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Attribute Selectors](../intermediate/01-attribute-selectors.md) →

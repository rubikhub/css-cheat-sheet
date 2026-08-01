# Container & Modern Units

> 12 units

Container query units and modern typographic units for component-scoped, context-aware sizing.

> Source: [web.dev/blog/cq-research](https://web.dev/blog/cq-research)

---

## Container Query Units

Container query units are relative to the **nearest query container** (an element with `container-type`), letting a component size itself to *its own* container instead of the viewport.

### cqw and cqh

**Syntax:** `<length>cqw` | `<length>cqh`

`1cqw` = 1% of the container's **width**; `1cqh` = 1% of the container's **height**.

**Values:**
- `100cqw` — full container width
- `50cqw` — half the container width
- `25cqh` — quarter of the container height

**Use Cases:**
- Card components that scale to their grid slot
- Reusable widgets that adapt to any placement

**Example:**
```css
.card {
  container-type: inline-size;
}

.card-title {
  font-size: 4cqw;   /* 4% of container width */
}
```

---

### cqi and cqb

**Syntax:** `<length>cqi` | `<length>cqb`

`1cqi` = 1% of the container's **inline size**; `1cqb` = 1% of the container's **block size** (writing-direction aware).

**Values:**
- `100cqi` — full inline size
- `10cqi` — 10% of inline size
- `100cqb` — full block size

**Use Cases:**
- Logical (direction-aware) sizing inside containers
- Vertical writing modes

**Example:**
```css
.avatar {
  width: 20cqi;   /* 20% of container inline size */
  height: 20cqi;
}
```

---

### cqmin and cqmax

**Syntax:** `<length>cqmin` | `<length>cqmax`

`cqmin` = the smaller of `cqi`/`cqb`; `cqmax` = the larger. Good for shape-safe scaling.

**Values:**
- `50cqmin` — half the smaller container axis
- `100cqmax` — full larger axis

**Use Cases:**
- Square shapes that fit inside any container
- Uniform margins on varied components

**Example:**
```css
.square {
  width: 40cqmin;
  height: 40cqmin;
}
```

---

## Typographic Units

### ic — Ideographic Character

**Syntax:** `<length>ic`

Relative to the width of the full-width "水" (or "0") glyph — approximates a CJK character's advance width. Two `ic` ≈ one em.

**Values:**
- `1ic` — width of one full-width ideograph
- `2ic` — width of two characters
- `20ic` — readable CJK line length

**Use Cases:**
- Line lengths for Chinese / Japanese text
- CJK-aware column sizing

**Example:**
```css
.cjk {
  max-width: 30ic;   /* readable line of CJK text */
}
```

---

### cap — Cap Height

**Syntax:** `<length>cap`

Relative to the **cap height** of the current font — the height of uppercase letters like "H".

**Values:**
- `1cap` — height of a capital letter
- `2cap` — two cap heights

**Use Cases:**
- Align decorative borders to uppercase text
- Sizing that tracks capital-letter height

**Example:**
```css
.caps-label {
  font-size: 2rem;
  border-bottom: 0.12cap solid #333;
}
```

---

### rem vs em — Quick Recap

| Unit | Relative To | Compounds? |
|------|-------------|------------|
| `rem` | root font-size | no |
| `em` | parent font-size | yes |
| `lh` | element line-height | yes |
| `rlh` | root line-height | no |
| `ic` | ideograph width | yes |
| `cap` | cap height | yes |

```css
html { font-size: 16px; }

.panel {
  font-size: 1.5em;    /* 24px in a 16px parent */
  padding: 1rlh;       /* root line-height based */
}
```

---

## Choosing the Right Unit

| Goal | Unit |
|------|------|
| Scale with the component's container | `cqi`, `cqw` |
| Scale with the viewport | `vw`, `dvh`, `vmin` |
| Scale with the font | `em`, `rem`, `lh` |
| Readable line lengths | `ch`, `ic` |
| Fit any container shape | `cqmin`, `cqmax` |

---

## Browser Support

- Container query units (`cqw` … `cqmax`) — supported in all modern browsers since 2023.
- `ic` and `cap` — supported in all modern browsers.
- Older browser fallback: use `clamp()` with a `rem` or `%` baseline.

```css
.card-title {
  font-size: clamp(1rem, 4cqw, 2rem);   /* safe fallback */
}
```

---

**[View Example](../examples/advanced/33-container-and-modern-units/index.html)**

← **Previous Topic:** [CSS 2026 & Beyond](../advanced/32-css-2026-and-beyond.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** *(This is the last topic)* →

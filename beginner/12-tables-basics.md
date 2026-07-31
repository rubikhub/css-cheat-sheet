# Tables Basics

> 4 properties

Table layout — collapsing borders, cell spacing, and column sizing.

---

## border-collapse

**Syntax:** `border-collapse: separate | collapse`

Border model — separate or collapse adjacent borders.

**Values:**
- `separate` — borders are separate (default)
- `collapse` — borders collapse into one
- `inherit` — inherits from parent
- `initial` — sets to default (separate)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Create clean table borders
- Remove double borders

**Example:**
```css
table {
  border-collapse: collapse;
}
```

---

## border-spacing

**Syntax:** `border-spacing: <length>`

Cell spacing — space between table cells (separate mode only).

**Values:**
- `0` — no spacing (default)
- `4px` — small spacing
- `8px 12px` — vertical horizontal
- `inherit` — inherits from parent
- `initial` — sets to default (0)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Add breathing room between cells
- Create visual separation

**Example:**
```css
table {
  border-spacing: 8px;
}
```

---

## table-layout

**Syntax:** `table-layout: auto | fixed`

Algorithm — automatic or fixed-width columns.

**Values:**
- `auto` — column width based on content (default)
- `fixed` — column width based on first row
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Speed up table rendering
- Create consistent column widths

**Example:**
```css
table {
  table-layout: fixed;
  width: 100%;
}
```

---

## caption-side

**Syntax:** `caption-side: top | bottom`

Caption position — above or below the table.

**Values:**
- `top` — above table (default)
- `bottom` — below table
- `inherit` — inherits from parent
- `initial` — sets to default (top)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Position table titles
- Create accessible table labels

**Example:**
```css
caption {
  caption-side: bottom;
}
```

---

**[View Example](../examples/beginner/12-tables-basics/index.html)**

← **Previous Topic:** [Lists Basics](../beginner/11-lists-basics.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Display Basics](../beginner/13-display-basics.md) →


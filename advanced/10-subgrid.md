# Subgrid & Named Grid Lines

> 3 properties

Advanced grid features for nested grid alignment and named line placement.

---

## Subgrid

---

## grid-template-columns: subgrid

**Syntax:** `grid-template-columns: subgrid`

A child grid inherits its parent's column tracks for perfect alignment.

**Values:**
- `subgrid` — inherit the parent's column tracks
- `none` — no explicit columns (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Align nested grids with parent columns
- Build complex layouts without redefining tracks

**Example:**
```css
.parent {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
}

.child {
  display: grid;
  grid-template-columns: subgrid;
}
```

---

## grid-template-rows: subgrid

**Syntax:** `grid-template-rows: subgrid`

A child grid inherits its parent's row tracks.

**Values:**
- `subgrid` — inherit the parent's row tracks
- `none` — no explicit rows (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Align nested rows with parent grid
- Keep row heights in sync across children

**Example:**
```css
.parent {
  display: grid;
  grid-template-rows: 50px 100px 50px;
}

.child {
  display: grid;
  grid-template-rows: subgrid;
}
```

---

## Named Grid Lines

**Syntax:** `grid-template-columns: [line-name] <track-list>`

Name grid lines for semantic placement.

**Values:**
- `[start] 1fr [content-start] 2fr [content-end] 1fr [end]` — named column lines
- `[header-start] 60px [header-end main-start] 1fr [main-end]` — named row lines
- `grid-column: content-start / content-end` — place items by named lines
- `grid-row: header-start / header-end` — place items by named row lines

**Use Cases:**
- Place items semantically instead of by number
- Keep layouts stable when tracks change

**Example:**
```css
.layout {
  display: grid;
  grid-template-columns: [sidebar-start] 200px [sidebar-end content-start] 1fr [content-end];
  grid-template-rows: [header-start] 60px [header-end main-start] 1fr [main-end footer-start] 40px [footer-end];
}

.header { grid-column: sidebar-start / content-end; }
.sidebar { grid-column: sidebar-start / sidebar-end; }
.main { grid-column: content-start / content-end; }
.footer { grid-column: sidebar-start / content-end; }
```

---

**[View Example](../examples/advanced/10-subgrid/index.html)**

← **Previous Topic:** [CSS Counters — Complex Patterns](../advanced/09-css-counters-complex.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Advanced State Pseudo-classes](../advanced/11-state-pseudo-classes-advanced.md) →

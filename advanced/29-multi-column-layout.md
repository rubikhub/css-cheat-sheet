# Multi-column Layout

> 8 properties

Split content into a flowing set of CSS columns like a newspaper.

---

## columns

**Syntax:** `columns: <column-width> || <column-count>`

Shorthand that sets both column width and count.

**Values:**
- `auto` — browser determines width and count
- `columns: 12em` — aim for columns about 12em wide
- `columns: 3` — exactly three columns
- `columns: 20rem 2` — width and count together

**Use Cases:**
- Lay out long text in multiple columns
- Create responsive column counts

**Example:**
```css
.article {
  columns: 16em;
}
```

---

## column-count

**Syntax:** `column-count: auto | <integer>`

Sets the number of columns.

**Values:**
- `auto` — browser decides the count (default)
- `column-count: 2` — two columns
- `column-count: 3` — three columns

**Use Cases:**
- Force a fixed number of columns
- Balance content across a known column count

**Example:**
```css
.report {
  column-count: 2;
}
```

---

## column-width

**Syntax:** `column-width: auto | <length>`

Sets an optimal column width; the browser creates as many columns as fit.

**Values:**
- `auto` — width based on other properties (default)
- `column-width: 250px` — aim for 250px-wide columns
- `column-width: 15rem` — use rem-based columns

**Use Cases:**
- Responsive multicol without media queries
- Keep lines at a readable length

**Example:**
```css
.story {
  column-width: 280px;
}
```

---

## column-gap

**Syntax:** `column-gap: normal | <length> | <percentage>`

Sets the space between columns.

**Values:**
- `normal` — browser default gap (default)
- `column-gap: 2rem` — fixed gap
- `column-gap: 5%` — percentage of the container width

**Use Cases:**
- Space out columns visually
- Align multicol gutters with grid gutters

**Example:**
```css
.article {
  columns: 3;
  column-gap: 2rem;
}
```

---

## column-rule

**Syntax:** `column-rule: <column-rule-width> || <column-rule-style> || <column-rule-color>`

Draws a divider line between columns.

**Values:**
- `column-rule: 1px solid #ccc` — thin solid divider
- `column-rule: 2px dashed` — dashed divider
- `column-rule-style` / `column-rule-width` / `column-rule-color` — longhands

**Use Cases:**
- Visually separate newspaper columns
- Decorate multicol layouts

**Example:**
```css
.article {
  columns: 3;
  column-gap: 2rem;
  column-rule: 1px solid #ddd;
}
```

---

## column-span

**Syntax:** `column-span: none | all`

Lets an element break out across all columns.

**Values:**
- `none` — stays inside the columns (default)
- `all` — spans every column

**Use Cases:**
- Full-width headings inside a multicol article
- Break a layout into distinct sections

**Example:**
```css
.article {
  columns: 3;
}

.article h2 {
  column-span: all;
}
```

---

## column-fill

**Syntax:** `column-fill: auto | balance`

Controls how content is distributed across the columns.

**Values:**
- `balance` — balance content across columns (default)
- `auto` — fill each column completely in order
- `balance-all` — balance, including the last column

**Use Cases:**
- Even-height columns for short content
- Sequential filling for long continuous text

**Example:**
```css
.story {
  height: 400px;
  columns: 3;
  column-fill: auto;
}
```

---

## break-inside

**Syntax:** `break-inside: auto | avoid | avoid-page | avoid-column`

Prevents elements from being split across columns or pages.

**Values:**
- `auto` — allow breaks (default)
- `avoid` — keep the element on one column/page
- `avoid-page` — avoid page breaks inside
- `avoid-column` — avoid column breaks inside

**Use Cases:**
- Keep cards and images intact in multicol
- Avoid orphaned headers

**Example:**
```css
.article {
  columns: 3;
}

.card {
  break-inside: avoid;
}
```

---

**[View Example](../examples/advanced/29-multi-column-layout/index.html)**

← **Previous Topic:** [Advanced Math Functions](../advanced/28-advanced-math-functions.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Motion Path](../advanced/30-motion-path.md) →


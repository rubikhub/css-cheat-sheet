# Paged Media & Print

> 7 features

Style printed documents with page boxes, breaks, and print-specific adjustments.

---

## @page

**Syntax:** `@page { <descriptors> }`

Defines the page box used when printing.

**Values:**
- `@page { margin: 1in; }` — set printed margins
- `@page { size: A4; }` — set the paper size
- `@page :first { ... }` — style the first page
- `@page :left { ... }` / `@page :right { ... }` — style left/right pages

**Use Cases:**
- Give printed output consistent margins
- Differentiate the cover page

**Example:**
```css
@page {
  margin: 1in;
  size: A4;
}

@page :first {
  margin-top: 2in;
}
```

---

## size

**Syntax:** `@page { size: auto | <length> | <page-size> || portrait | landscape }`

Sets the size and orientation of the printed page.

**Values:**
- `auto` — browser default size (default)
- `size: A4` — ISO A4 paper
- `size: A4 landscape` — landscape orientation
- `size: 8.5in 11in` — explicit dimensions

**Use Cases:**
- Control print paper size from CSS
- Force landscape for wide tables

**Example:**
```css
@page {
  size: A4 landscape;
}
```

---

## break-before / break-after

**Syntax:** `break-before: auto | page | left | right | column`

Controls where content breaks before or after an element.

**Values:**
- `auto` — no forced break (default)
- `page` — start on a new page
- `left` / `right` — start on a left/right page
- `column` — start on a new column

**Use Cases:**
- Start each chapter on a new page
- Push elements to a right-hand page

**Example:**
```css
.chapter {
  break-before: page;
}

.section {
  break-after: page;
}
```

---

## break-inside

**Syntax:** `break-inside: auto | avoid | avoid-page | avoid-column`

Prevents an element from being split across pages or columns.

**Values:**
- `auto` — allow breaks (default)
- `avoid` — keep the element whole
- `avoid-page` — avoid page breaks inside
- `avoid-column` — avoid column breaks inside

**Use Cases:**
- Keep tables and figures intact
- Avoid cutting headings from their content

**Example:**
```css
table {
  break-inside: avoid;
}

h2 {
  break-after: avoid-page;
}
```

---

## orphans / widows

**Syntax:** `orphans: <integer>` | `widows: <integer>`

Control the minimum number of lines at the bottom/top of a page.

**Values:**
- `orphans: 3` — at least 3 lines at the bottom of a page
- `widows: 3` — at least 3 lines at the top of a page
- `orphans: 1` / `widows: 1` — default

**Use Cases:**
- Prevent single dangling lines in print
- Keep paragraphs readable when broken

**Example:**
```css
p {
  orphans: 3;
  widows: 3;
}
```

---

## print-color-adjust

**Syntax:** `print-color-adjust: economy | exact`

Controls whether the browser applies background colors when printing.

**Values:**
- `economy` — browser may drop backgrounds to save ink (default)
- `exact` — always print backgrounds and colors

**Use Cases:**
- Keep dark-mode or colored elements legible on paper
- Ensure branded backgrounds print

**Example:**
```css
.banner {
  background: #111;
  color: white;
  print-color-adjust: exact;
  -webkit-print-color-adjust: exact;
}
```

---

## @media print

**Syntax:** `@media print { ... }`

Conditional styles applied only when the document is printed.

**Values:**
- Hide navigation and interactive elements
- Show print-only content with `display: none` toggling
- Linearize multi-column layouts

**Use Cases:**
- Print-friendly navigation removal
- Expand collapsible content for paper

**Example:**
```css
@media print {
  nav,
  .ads {
    display: none;
  }

  .content {
    width: 100%;
  }
}
```

---

**[View Example](../examples/advanced/27-paged-media/index.html)**

← **Previous Topic:** [Motion Path](../advanced/26-motion-path.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** *(This is the last topic)* →

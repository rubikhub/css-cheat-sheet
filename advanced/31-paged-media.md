# Paged Media & Print

> 12 features

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

## Named Pages

**Syntax:** `page: <page-name>;` + `@page <page-name> { ... }`

Assigns elements to named page boxes with their own @page rules.

**Values:**
- `page: cover` — place the element on a cover page
- `@page cover { size: A4 landscape; }` — style that named page
- `page: auto` — default page (default)

**Use Cases:**
- Apply different paper sizes to sections
- Give the cover and appendix distinct page setups

**Example:**
```css
.cover {
  page: cover;
}

@page cover {
  size: A4 landscape;
  margin: 0;
}
```

---

## Margin Boxes

**Syntax:** `@page { @top-center { content: ...; } }`

Runs headers and footers inside page-margin boxes.

**Values:**
- `@top-left` / `@top-center` / `@top-right` — top margin boxes
- `@bottom-left` / `@bottom-center` / `@bottom-right` — bottom margin boxes
- `content: string(page-title)` — string-set content

**Use Cases:**
- Add page numbers and running headers to print
- Style book-like layouts

**Example:**
```css
@page {
  @top-center {
    content: string(book-title);
  }

  @bottom-center {
    content: counter(page);
  }
}
```

---

## counter(page) & counter(pages)

**Syntax:** `content: counter(page) " / " counter(pages);`

Built-in counters for the current and total number of pages.

**Values:**
- `counter(page)` — the current page number
- `counter(pages)` — the total number of pages
- `counter(page, lower-roman)` — roman page numbers

**Use Cases:**
- Print "3 / 12" style page numbering
- Reset page numbering per named page

**Example:**
```css
@page {
  @bottom-center {
    content: counter(page) " / " counter(pages);
  }
}
```

---

## bleed

**Syntax:** `@page { bleed: <length>; }`

Sets the bleed area beyond the page box for full-bleed printing.

**Values:**
- `bleed: 3mm` — standard print bleed
- `bleed: 0` — no bleed (default)

**Use Cases:**
- Prepare artwork that extends to the paper edge
- Support professional print production

**Example:**
```css
@page {
  bleed: 3mm;
}
```

---

## marks

**Syntax:** `@page { marks: crop cross; }`

Adds crop marks and registration marks for printing.

**Values:**
- `marks: crop` — trim marks at the page corners
- `marks: cross` — registration marks
- `marks: none` — no marks (default)

**Use Cases:**
- Mark trim lines for printed documents
- Align color separations in production

**Example:**
```css
@page {
  marks: crop cross;
}
```

---

**[View Example](../examples/advanced/31-paged-media/index.html)**

← **Previous Topic:** [Motion Path](../advanced/30-motion-path.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [CSS 2026 & Beyond](../advanced/32-css-2026-and-beyond.md) →


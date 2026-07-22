# Grid Advanced
---
## Container Properties
### display
**Type/Initial:** keyword | inline

**Description:** Grid container — enables grid layout on children.

**CSS:**
```css
display: grid;
display: inline-grid;
display: block-grid;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 0.3rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### grid-template-columns
**Type/Initial:** track list | none

**Description:** Columns — defines the column tracks of a grid container.

**CSS:**
```css
/* None */
grid-template-columns: none;

/* Track sizes */
grid-template-columns: 200px;
grid-template-columns: 200px 100px auto;
grid-template-columns: repeat(3, 1fr);
grid-template-columns: repeat(4, 1fr);
grid-template-columns: repeat(2, minmax(100px, 1fr));

/* Auto-fit / auto-fill */
grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
grid-template-columns: repeat(auto-fill, minmax(150px, 1fr));

/* Global values */
grid-template-columns: inherit;
grid-template-columns: initial;
grid-template-columns: revert;
grid-template-columns: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    1
  </div>
  <div class="db style-c">
    2
  </div>
  <div class="db style-d">
    3
  </div>
  <div class="db style-e">
    4
  </div>
  <div class="db style-f">
    5
  </div>
  <div class="db style-g">
    6
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 0.3rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-f {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-g {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### grid-template-rows
**Type/Initial:** track list | none

**Description:** Rows — defines the row tracks of a grid container.

**CSS:**
```css
/* None */
grid-template-rows: none;

/* Track sizes */
grid-template-rows: 100px;
grid-template-rows: 100px 200px auto;
grid-template-rows: repeat(3, 1fr);
grid-template-rows: minmax(50px, auto);

/* Global values */
grid-template-rows: inherit;
grid-template-rows: initial;
grid-template-rows: revert;
grid-template-rows: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    1
  </div>
  <div class="db style-c">
    2
  </div>
  <div class="db style-d">
    3
  </div>
  <div class="db style-e">
    4
  </div>
  <div class="db style-f">
    5
  </div>
  <div class="db style-g">
    6
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-template-rows: 40px auto 40px;
  gap: 0.3rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-f {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-g {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### grid-template-areas
**Type/Initial:** string | none

**Description:** Areas — names grid areas for placement by name.

**CSS:**
```css
/* None */
grid-template-areas: none;

/* Named areas */
grid-template-areas:
  "header header"
  "sidebar main"
  "footer footer";

grid-template-areas:
  "a a a"
  "b b c"
  "d d d";

/* Global values */
grid-template-areas: inherit;
grid-template-areas: initial;
grid-template-areas: revert;
grid-template-areas: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    header
  </div>
  <div class="db style-c">
    side
  </div>
  <div class="db style-d">
    main
  </div>
  <div class="db style-e">
    footer
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 1fr 2fr;
  grid-template-rows: auto auto auto;
  grid-template-areas: 'header header' 'sidebar main' 'footer footer';
  gap: 0.3rem;
  font-size: 0.75rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  grid-area: header;
  text-align: center;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  grid-area: sidebar;
  text-align: center;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  grid-area: main;
  text-align: center;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  grid-area: footer;
  text-align: center;
}
```

### gap
**Type/Initial:** length | 0

**Description:** Gutters — sets spacing between grid rows and columns.

**CSS:**
```css
gap: 10px;
gap: 1rem 2rem;
gap: 5% 10%;

gap: inherit;
gap: initial;
gap: revert;
gap: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    1
  </div>
  <div class="db style-c">
    2
  </div>
  <div class="db style-d">
    3
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 0.8rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### grid-auto-columns
**Type/Initial:** track size | auto

**Description:** Auto columns — sets the size for auto-placed columns.

**CSS:**
```css
grid-auto-columns: auto;
grid-auto-columns: 100px;
grid-auto-columns: 1fr;
grid-auto-columns: min-content;
grid-auto-columns: max-content;
grid-auto-columns: minmax(100px, 1fr);

grid-auto-columns: inherit;
grid-auto-columns: initial;
grid-auto-columns: revert;
grid-auto-columns: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    1
  </div>
  <div class="db style-c">
    2
  </div>
  <div class="db style-d">
    3
  </div>
  <div class="db style-e">
    4
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 80px;
  grid-auto-columns: 1fr;
  grid-auto-flow: column;
  gap: 0.3rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### grid-auto-rows
**Type/Initial:** track size | auto

**Description:** Auto rows — sets the size for auto-placed rows.

**CSS:**
```css
grid-auto-rows: auto;
grid-auto-rows: 100px;
grid-auto-rows: 1fr;
grid-auto-rows: min-content;
grid-auto-rows: max-content;
grid-auto-rows: minmax(50px, auto);

grid-auto-rows: inherit;
grid-auto-rows: initial;
grid-auto-rows: revert;
grid-auto-rows: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    1
  </div>
  <div class="db style-c">
    2
  </div>
  <div class="db style-d">
    3
  </div>
  <div class="db style-e">
    4
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-auto-rows: 40px;
  gap: 0.3rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### grid-auto-flow
**Type/Initial:** keyword | row

**Description:** Auto flow — controls how auto-placed items are inserted.

**CSS:**
```css
grid-auto-flow: row;
grid-auto-flow: column;
grid-auto-flow: dense;
grid-auto-flow: row dense;
grid-auto-flow: column dense;

grid-auto-flow: inherit;
grid-auto-flow: initial;
grid-auto-flow: revert;
grid-auto-flow: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    1
  </div>
  <div class="db style-c">
    2
  </div>
  <div class="db style-d">
    3
  </div>
  <div class="db style-e">
    4
  </div>
  <div class="db style-f">
    5
  </div>
  <div class="db style-g">
    6
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-rows: 1fr 1fr 1fr;
  grid-auto-flow: column;
  gap: 0.3rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-f {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-g {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

## Item Properties
### grid-column
**Type/Initial:** span | auto

**Description:** Column span — makes an item span across grid columns.

**CSS:**
```css
/* Span */
grid-column: 1 / 3;
grid-column: 1 / span 2;
grid-column: span 2;

/* Auto placement */
grid-column: auto;
grid-column: auto / 1;

/* Named lines */
grid-column: header-start / header-end;

/* Global values */
grid-column: inherit;
grid-column: initial;
grid-column: revert;
grid-column: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    span 2
  </div>
  <div class="db style-c">
    1
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 0.3rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  grid-column: span 2;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### grid-row
**Type/Initial:** span | auto

**Description:** Row span — makes an item span across grid rows.

**CSS:**
```css
grid-row: 1 / 3;
grid-row: 1 / span 2;
grid-row: span 2;
grid-row: auto;
grid-row: auto / 1;

grid-row: inherit;
grid-row: initial;
grid-row: revert;
grid-row: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    span 2
  </div>
  <div class="db style-c">
    2
  </div>
  <div class="db style-d">
    3
  </div>
  <div class="db style-e">
    4
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 1fr 1fr;
  grid-auto-rows: 32px;
  gap: 0.3rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  grid-row: span 2;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### grid-area
**Type/Initial:** name / span | auto

**Description:** Area — places an item into a named grid area or by line numbers.

**CSS:**
```css
/* Named areas */
grid-area: header;
grid-area: sidebar;
grid-area: main;
grid-area: footer;

/* Shorthand: row-start / column-start / row-end / column-end */
grid-area: 1 / 1 / 3 / 3;
grid-area: 1 / span 2 / 3 / span 2;

/* Global values */
grid-area: inherit;
grid-area: initial;
grid-area: revert;
grid-area: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
  </div>
  <div class="db style-e">
    D
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows: auto auto;
  gap: 0.3rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  grid-area: 1/1/3/2;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### justify-items
**Type/Initial:** keyword | stretch

**Description:** Justify items — aligns items along the inline (row) axis within their cell.

**CSS:**
```css
justify-items: start;
justify-items: end;
justify-items: center;
justify-items: stretch;
justify-items: left;
justify-items: right;

justify-items: inherit;
justify-items: initial;
justify-items: revert;
justify-items: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  gap: 0.3rem;
  justify-items: center;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### align-items
**Type/Initial:** keyword | stretch

**Description:** Align items — aligns items along the block (column) axis within their cell.

**CSS:**
```css
align-items: start;
align-items: end;
align-items: center;
align-items: stretch;
align-items: baseline;
align-items: self-start;
align-items: self-end;

align-items: inherit;
align-items: initial;
align-items: revert;
align-items: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-auto-rows: 64px;
  gap: 0.3rem;
  align-items: center;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```

### place-items
**Type/Initial:** shorthand | stretch

**Description:** Place items — shorthand for align-items and justify-items together.

**CSS:**
```css
/* Single value */
place-items: center;
place-items: start;
place-items: stretch;

/* Two values */
place-items: center start;
place-items: stretch end;

place-items: inherit;
place-items: initial;
place-items: revert;
place-items: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    A
  </div>
  <div class="db style-c">
    B
  </div>
  <div class="db style-d">
    C
  </div>
</div>
```

**CSS Rendered:**
```css
.db {
  background: #f5f5f5;
  border: 1px solid #e5e5e5;
  padding: .6rem .8rem;
  border-radius: 6px;
}
.style-a {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-auto-rows: 64px;
  gap: 0.3rem;
  place-items: center;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
}
```
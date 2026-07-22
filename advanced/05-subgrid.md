# Subgrid & Named Grid Lines

Advanced grid features for nested grid alignment and named line placement.

---

## Subgrid

### grid-template-columns: subgrid
**Type:** keyword | **Initial:** none

A child grid inherits its parent's column tracks for perfect alignment.

```css
/* Parent defines tracks */
.parent {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
}

/* Child inherits parent columns */
.child {
  display: grid;
  grid-template-columns: subgrid;
}
```

```html
<div class="parent">
  <div class="child">
    <span>A</span>
    <span>B</span>
    <span>C</span>
  </div>
  <div class="child">
    <span>D</span>
    <span>E</span>
    <span>F</span>
  </div>
</div>
```

```css
.parent {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  gap: 8px;
}

.child {
  display: grid;
  grid-template-columns: subgrid;
}
```

### grid-template-rows: subgrid
**Type:** keyword | **Initial:** none

A child grid inherits its parent's row tracks.

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

Name grid lines for semantic placement.

```css
/* Named lines in template */
grid-template-columns: [start] 1fr [content-start] 2fr [content-end] 1fr [end];

/* Place items by named lines */
.item {
  grid-column: content-start / content-end;
}
```

```html
<div class="named-lines">
  <header class="header">Header</header>
  <aside class="sidebar">Sidebar</aside>
  <main class="main">Main</main>
  <footer class="footer">Footer</footer>
</div>
```

```css
.named-lines {
  display: grid;
  grid-template-columns: [sidebar-start] 200px [sidebar-end content-start] 1fr [content-end];
  grid-template-rows: [header-start] 60px [header-end main-start] 1fr [main-end footer-start] 40px [footer-end];
}

.header { grid-column: sidebar-start / content-end; }
.sidebar { grid-column: sidebar-start / sidebar-end; }
.main { grid-column: content-start / content-end; }
.footer { grid-column: sidebar-start / content-end; }
```

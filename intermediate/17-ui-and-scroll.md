# UI & Scroll
---
## Container Properties
### cursor
**Type/Initial:** keyword | auto

**Description:** Cursor — specifies the mouse cursor appearance.

**CSS:**
```css
/* Default */
cursor: auto;

/* Basic */
cursor: default;
cursor: none;
cursor: pointer;
cursor: help;
cursor: wait;
cursor: progress;

/* Selection */
cursor: text;
cursor: crosshair;
cursor: cell;
cursor: vertical-text;

/* Drag & drop */
cursor: move;
cursor: copy;
cursor: no-drop;
cursor: not-allowed;
cursor: grab;
cursor: grabbing;

/* Resize */
cursor: n-resize;
cursor: s-resize;
cursor: e-resize;
cursor: w-resize;
cursor: ne-resize;
cursor: nw-resize;
cursor: se-resize;
cursor: sw-resize;
cursor: ew-resize;
cursor: ns-resize;
cursor: nesw-resize;
cursor: nwse-resize;
cursor: col-resize;
cursor: row-resize;

/* Zoom */
cursor: zoom-in;
cursor: zoom-out;

/* Custom */
cursor: url("cursor.svg"), auto;
cursor: url("cursor.png") 10 10, pointer;

cursor: inherit;
cursor: initial;
cursor: revert;
cursor: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    pointer
  </div>
  <div class="db style-c">
    not-allowed
  </div>
  <div class="db style-d">
    grab
  </div>
  <div class="db style-e">
    zoom-in
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
  display: flex;
  gap: 0.8rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  cursor: pointer;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  cursor: not-allowed;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  cursor: grab;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  cursor: zoom-in;
}
```

### user-select
**Type/Initial:** keyword | auto

**Description:** User select — controls whether user can select text.

**CSS:**
```css
user-select: auto;
user-select: none;
user-select: text;
user-select: contain;
user-select: all;

user-select: inherit;
user-select: initial;
user-select: revert;
user-select: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    auto (select me)
  </div>
  <div class="db style-c">
    none (try to select)
  </div>
  <div class="db style-d">
    all (click me)
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
  display: flex;
  gap: 0.8rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  user-select: auto;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  user-select: none;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  user-select: all;
}
```

### scroll-behavior
**Type/Initial:** keyword | auto

**Description:** Scroll behavior — defines smooth or instant scrolling.

**CSS:**
```css
scroll-behavior: auto;
scroll-behavior: smooth;

scroll-behavior: inherit;
scroll-behavior: initial;
scroll-behavior: revert;
scroll-behavior: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    auto (instant)
  </div>
  <div class="db style-c">
    smooth
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
  display: flex;
  gap: 1rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  scroll-behavior: auto;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  scroll-behavior: smooth;
}
```

### overflow
**Type/Initial:** keyword | visible

**Description:** Overflow — specifies how content is handled when it overflows the element's box.

**CSS:**
```css
overflow: visible;
overflow: hidden;
overflow: clip;
overflow: scroll;
overflow: auto;

overflow-x: visible;
overflow-x: hidden;
overflow-x: clip;
overflow-x: scroll;
overflow-x: auto;

overflow-y: visible;
overflow-y: hidden;
overflow-y: clip;
overflow-y: scroll;
overflow-y: auto;

overflow: inherit;
overflow: initial;
overflow: revert;
overflow: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    visible
  </div>
  <div class="db style-c">
    hidden
  </div>
  <div class="db style-d">
    scroll
  </div>
  <div class="db style-e">
    auto
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
  display: flex;
  gap: 0.8rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  overflow: visible;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  overflow: hidden;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  overflow: scroll;
}
.style-e {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  overflow: auto;
}
```

### scrollbar-width
**Type/Initial:** keyword | auto

**Description:** Scrollbar width — controls the scrollbar thickness.

**CSS:**
```css
scrollbar-width: auto;
scrollbar-width: thin;
scrollbar-width: none;

scrollbar-width: inherit;
scrollbar-width: initial;
scrollbar-width: revert;
scrollbar-width: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    auto
  </div>
  <div class="db style-c">
    thin
  </div>
  <div class="db style-d">
    none
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
  display: flex;
  gap: 0.8rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  scrollbar-width: auto;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  scrollbar-width: thin;
}
.style-d {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  scrollbar-width: none;
}
```

### scrollbar-color
**Type/Initial:** color | auto

**Description:** Scrollbar color — sets the thumb and track colors of the scrollbar.

**CSS:**
```css
scrollbar-color: auto;
scrollbar-color: #888 transparent;
scrollbar-color: #888 #f1f1f1;
scrollbar-color: #333 #e5e5e5;

scrollbar-color: inherit;
scrollbar-color: initial;
scrollbar-color: revert;
scrollbar-color: unset;
```

**HTML:**
```html
<div class="style-a">
  <div class="db style-b">
    custom colors
  </div>
  <div class="db style-c">
    dark theme
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
  display: flex;
  gap: 1rem;
  padding: 1rem;
}
.style-b {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  scrollbar-color: #888 #f1f1f1;
}
.style-c {
  background: #fff;
  padding: 0.4rem 0.8rem;
  border-radius: 4px;
  color: #333;
  scrollbar-color: #333 #e5e5e5;
}
```
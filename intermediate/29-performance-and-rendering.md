# Performance & Rendering

> 4 properties

Containment and hints that make large pages render faster.

---

## contain

**Syntax:** `contain: none | strict | content | size | layout | style | paint`

Tells the browser which parts of an element can be isolated from the rest of the page.

**Values:**
- `none` — no containment (default)
- `size` — the box ignores content size
- `layout` — layout isolation
- `style` — counter and quote isolation
- `paint` — paint clipping to the box
- `strict` — all of size layout style paint
- `content` — layout style paint (not size)

**Use Cases:**
- Isolate expensive subtree updates
- Stop size changes from affecting layout outside

**Example:**
```css
.card {
  contain: layout paint;
}
```

---

## content-visibility

**Syntax:** `content-visibility: visible | auto | hidden`

Skips rendering of off-screen content to improve initial page load.

**Values:**
- `visible` — render normally (default)
- `auto` — skip rendering when off-screen
- `hidden` — never render, like display: none

**Use Cases:**
- Speed up long pages and lists
- Keep scroll behavior smooth

**Example:**
```css
section {
  content-visibility: auto;
  contain-intrinsic-size: 0 500px;
}
```

---

## contain-intrinsic-size

**Syntax:** `contain-intrinsic-size: <length-percentage>` | `auto <length-percentage>`

Sets the intrinsic size used while content-visibility skips rendering.

**Values:**
- `500px` — a fixed reserved height
- `auto 500px` — remember the last rendered size
- `500px 300px` — width and height
- `none` — no reserved size

**Use Cases:**
- Prevent layout shift on long pages
- Keep scrollbars stable while loading

**Example:**
```css
.article {
  content-visibility: auto;
  contain-intrinsic-size: auto 600px;
}
```

---

## will-change

**Syntax:** `will-change: auto | <property> | scroll-position | contents`

Hints which properties will change so the browser can optimize ahead of time.

**Values:**
- `transform` — hint for transform animations
- `opacity` — hint for opacity changes
- `scroll-position` — element will scroll
- `contents` — the element's contents will change
- `auto` — no hint (default)

**Use Cases:**
- Promote layers for smooth animations
- Reduce jank on scroll-driven effects

**Example:**
```css
.card {
  will-change: transform;
}
```

---

**[View Example](../examples/intermediate/29-performance-and-rendering/index.html)**

← **Previous Topic:** [CSS Shapes](../intermediate/28-css-shapes.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Relative & Viewport Units](../intermediate/30-relative-and-viewport-units.md) →

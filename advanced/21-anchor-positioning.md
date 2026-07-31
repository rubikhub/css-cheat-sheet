# Anchor Positioning

> 4 properties & 2 functions

Position elements relative to other anchor elements.

---

## anchor-name

**Syntax:** `anchor-name: <dashed-ident> | none`

Declares an element as an anchor that other elements can reference.

**Values:**
- `--trigger` — the anchor's dashed-ident name
- `none` — no anchor name (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Define a trigger for a tooltip or popover
- Name multiple anchors on a page

**Example:**
```css
.tooltip-trigger {
  anchor-name: --trigger;
}

.popup {
  anchor-name: --popup;
}
```

---

## position-anchor

**Syntax:** `position-anchor: <anchor-name> | auto`

Links an absolutely-positioned element to an anchor.

**Values:**
- `--trigger` — the anchor name to position against
- `auto` — default anchor resolution (default)
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Attach tooltips and popovers to a trigger
- Position dropdowns relative to their buttons

**Example:**
```css
.tooltip {
  position: fixed;
  position-anchor: --trigger;
  top: anchor(bottom);
  left: anchor(center);
}
```

---

## anchor()

**Syntax:** `anchor(<anchor-name>, <side>)`

References a position on the anchor element.

**Values:**
- `anchor(bottom)` — below the anchor
- `anchor(top)` — above the anchor
- `anchor(right)` — right side of the anchor
- `anchor(left)` — left side of the anchor
- `anchor(center)` — center of the anchor
- `anchor(--trigger bottom)` — named anchor, specific side

**Use Cases:**
- Position tooltips against anchor edges
- Align elements to the center of an anchor

**Example:**
```css
.tooltip {
  position: fixed;
  position-anchor: --trigger;
  top: anchor(bottom);
  left: anchor(center);
}
```

---

## anchor-size()

**Syntax:** `anchor-size(<anchor-name> <dimension>)`

References the size of an anchor element.

**Values:**
- `anchor-size(--trigger width)` — the anchor's width
- `anchor-size(--trigger height)` — the anchor's height

**Use Cases:**
- Match a popover's width to its trigger
- Match an element's height to its anchor

**Example:**
```css
.popup {
  width: anchor-size(--trigger width);
}

.full-height {
  height: anchor-size(--trigger height);
}
```

---

## position-area

**Syntax:** `position-area: <area>`

Places the element relative to the anchor using grid notation.

**Values:**
- `top` — above the anchor
- `bottom` — below the anchor
- `left` — to the left of the anchor
- `right` — to the right of the anchor
- `top left` — top-left corner
- `bottom center` — bottom-center
- `auto` — no fixed area (default)
- `inherit` — inherits from parent
- `initial` — sets to default (auto)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Position tooltips on any side of a trigger
- Pin elements to anchor corners

**Example:**
```css
.tooltip {
  position: fixed;
  position-anchor: --trigger;
  position-area: top;
}

.tooltip-bottom {
  position-area: bottom;
}
```

---

## position-try-fallbacks

**Syntax:** `position-try-fallbacks: <try-option>`

Defines fallback positions when the element overflows the viewport.

**Values:**
- `flip-block` — flip across the block axis
- `flip-inline` — flip across the inline axis
- `flip-block flip-inline` — flip on both axes
- `none` — no fallbacks (default)
- `inherit` — inherits from parent
- `initial` — sets to default (none)
- `revert` — reverts to user agent stylesheet value
- `unset` — inherits or initial depending on property

**Use Cases:**
- Keep tooltips inside the viewport
- Handle overflow near screen edges

**Example:**
```css
.tooltip {
  position: fixed;
  position-anchor: --trigger;
  position-area: top;
  position-try-fallbacks: flip-block, flip-inline;
}
```

---

**[View Example](../examples/advanced/21-anchor-positioning/index.html)**

← **Previous Topic:** [Container Queries](../advanced/20-container-queries.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Scroll-Driven Animations](../advanced/22-scroll-animations.md) →

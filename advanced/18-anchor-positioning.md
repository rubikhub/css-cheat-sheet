# Anchor Positioning

Position elements relative to other "anchor" elements.

---

## anchor-name
**Type:** name | **Initial:** none

Declares an element as an anchor that other elements can reference.

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
**Type:** name | **Initial:** auto

Links an absolutely-positioned element to an anchor.

```css
.tooltip {
  position: fixed;
  position-anchor: --trigger;
  top: anchor(bottom);
  left: anchor(center);
  translate: -50% 8px;
}
```

---

## anchor()
**Type:** function

References a position on the anchor element.

```css
/* Anchor edges */
top: anchor(bottom);
bottom: anchor(top);
left: anchor(right);
right: anchor(left);

/* Anchor center */
top: anchor(center);
left: anchor(center);

/* Named anchor */
top: anchor(--trigger bottom);
left: anchor(--trigger center);
```

---

## anchor-size()
**Type:** function

References the size of an anchor element.

```css
/* Match anchor width */
width: anchor-size(--trigger width);

/* Match anchor height */
height: anchor-size(--trigger height);
```

---

## position-area
**Type:** grid-area

Places the element relative to the anchor using a grid notation.

```css
.tooltip {
  position: fixed;
  position-anchor: --trigger;
  position-area: top;
}

/* Other areas */
position-area: bottom;
position-area: left;
position-area: right;
position-area: top left;
position-area: bottom center;
```

---

## position-try-fallbacks
**Type:** list | **Initial:** none

Defines fallback positions when the element overflows.

```css
.tooltip {
  position: fixed;
  position-anchor: --trigger;
  position-area: top;
  position-try-fallbacks:
    flip-block,
    flip-inline,
    flip-block flip-inline;
}
```

```html
<button class="trigger" style="anchor-name: --btn">Hover me</button>
<div class="tooltip" style="position-anchor: --btn">Tooltip content</div>
```

```css
.trigger {
  anchor-name: --btn;
}

.tooltip {
  position: fixed;
  position-anchor: --btn;
  top: anchor(bottom);
  left: anchor(center);
  translate: -50% 8px;
  background: #333;
  color: white;
  padding: 0.5rem 1rem;
  border-radius: 6px;
  position-try-fallbacks: flip-block;
}
```


---

[Example](../examples/advanced/18-anchor-positioning/index.html)

← **Previous Topic:** [Selectors 2024+](../advanced/17-selectors-2024.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Scroll-Driven Animations](../advanced/19-scroll-animations.md) →

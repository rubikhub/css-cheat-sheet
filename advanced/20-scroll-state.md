# Scroll State Queries

> 5 scroll-state conditions

Query the scroll state of elements and the viewport.

---

## @scroll-state

**Syntax:** `@scroll-state(<query>)`

Applies styles based on scroll position and snap state.

**Values:**
- `stuck: top` — element stuck to the top edge
- `snapped: top` — element snapped to the top
- `scrollable: bottom` — content scrollable past the bottom

**Use Cases:**
- Add a shadow to a sticky header once stuck
- Highlight the snapped slide
- Reveal a load-more button at the end

**Example:**
```css
@scroll-state(stuck: top) {
  .header {
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  }
}
```

---

## scroll-state()

**Syntax:** `scroll-state(<query>)`

References the scroll state of a named element.

**Values:**
- `stuck: top` — element stuck to the top
- `not stuck: top` — element not stuck to the top
- `snapped: top` — element snapped to the top
- `scrollable: bottom` — content scrollable past the bottom

**Use Cases:**
- Style based on another element's scroll state
- Respond to sticky and snap positions

**Example:**
```css
@scroll-state(stuck: top) {
  .header {
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
    position: sticky;
    top: 0;
  }
}
```

---

## Scroll State Properties

---

## scroll-state(stuck)

**Syntax:** `@scroll-state(stuck: <edge>)`

Styles an element based on whether it is stuck to a scroll edge.

**Values:**
- `stuck: top` — element stuck to the top
- `not stuck: top` — element not stuck to the top

**Use Cases:**
- Show or hide a sticky header
- Add elevation when the header is stuck

**Example:**
```css
@scroll-state(stuck: top) {
  .header {
    opacity: 1;
    transform: translateY(0);
  }
}

@scroll-state(not stuck: top) {
  .header {
    opacity: 0;
    transform: translateY(-100%);
  }
}
```

---

## scroll-state(snapped)

**Syntax:** `@scroll-state(snapped: <edge>)`

Styles elements based on their scroll-snap alignment.

**Values:**
- `snapped: top` — element snapped to the top

**Use Cases:**
- Highlight the active snap item
- Scale up the currently snapped item

**Example:**
```css
@scroll-state(snapped: top) {
  .snap-item {
    background: lightblue;
    transform: scale(1.05);
  }
}
```

---

## scroll-state(scrollable)

**Syntax:** `@scroll-state(scrollable: <edge>)`

Styles elements based on remaining scrollable content.

**Values:**
- `scrollable: bottom` — content scrollable past the bottom
- `not scrollable: bottom` — content ends at the bottom

**Use Cases:**
- Show a scroll indicator only when more content exists
- Reveal a load-more button at the end of content

**Example:**
```css
@scroll-state(scrollable: bottom) {
  .scroll-indicator {
    display: block;
  }
}

@scroll-state(not scrollable: bottom) {
  .scroll-indicator {
    display: none;
  }
}
```

---

**[View Example](../examples/advanced/20-scroll-state/index.html)**

← **Previous Topic:** [Scroll-Driven Animations](../advanced/19-scroll-animations.md) &nbsp;&nbsp;|&nbsp;&nbsp; **Next Topic:** [Advanced Color Functions](../advanced/21-color-functions-advanced.md) →

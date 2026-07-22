# Scroll State Queries

Query the scroll state of elements and the viewport.

---

## @scroll-state
**Type:** at-rule

Applies styles based on scroll position and snap state.

```css
/* Sticky header when scrolled past */
@scroll-state(stuck: top) {
  .header {
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
  }
}

/* Snapped element */
@scroll-state(snapped: top) {
  .card {
    border: 2px solid blue;
  }
}

/* Scrolled to bottom */
@scroll-state(scrollable: bottom) {
  .load-more {
    display: block;
  }
}
```

---

## scroll-state()

**Type:** function

References the scroll state of a named element.

```css
/* Style based on named element's scroll state */
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

### scroll-state(stuck)
```css
/* Header becomes visible when stuck */
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

### scroll-state(snapped)
```css
/* Highlight snapped item */
@scroll-state(snapped: top) {
  .snap-item {
    background: lightblue;
    transform: scale(1.05);
  }
}
```

### scroll-state(scrollable)
```css
/* Show scroll indicator only when scrollable */
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

```html
<header class="header">Sticky Header</header>
<div class="content">
  <p>Long content...</p>
</div>
```

```css
.header {
  position: sticky;
  top: 0;
  padding: 1rem;
  background: white;
  transition: box-shadow 0.3s, background 0.3s;
}

@scroll-state(stuck: top) {
  .header {
    box-shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    background: rgba(255, 255, 255, 0.95);
    backdrop-filter: blur(10px);
  }
}
```
